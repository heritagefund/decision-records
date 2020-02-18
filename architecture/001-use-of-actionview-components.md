# Use of ActionView Components

## Introduction

* Status
* Context
    * Options considered
        * Custom `FormBuilder` objects
        * Generic partials
        * Use of `ActionView Components`
* Decision
* Consequences

## Status

*Accepted*, decided by @stuartmccoll and @paulmsmith on 2020-02-18.

## Context

During the alpha and early private beta stages of the project, we, as a team, chose to favour building service functionality over ensuring reusability of our code, with an agreement in place that we would address this technical debt at a later date.

When we talk about reusability of code within our [funding-frontend](https://github.com/heritagefund/funding-frontend) Ruby-on-Rails application, we can consider this along three separate lines, with some overlap between - the models, views and controllers that form the application. This particular architectural decision relates to the reusability of our views.

As the only multi-disciplinary agile team within the organisation delivering software, it's important to ensure that we enable the team to move at speed whilst still considering best practices. As a team delivering a service via user-centered design we like to have the ability to iterate content quickly based on user research. For this reason, we have agreed as a team that we want to be able to build reusability into the components that make up our views whilst making them simple enough to understand that those not skilled in Ruby-on-Rails can still contribute changes.

### Options considered

#### Custom `FormBuilder` objects

Ruby-on-Rails offers functionality in the form of [custom `FormBuilder`]() objects, which allow for reusable form components. This allows us to write a `NlhfFormBuilder` class which gives us the capability to declaritively add our custom form elements within our views, with the markup living in a single place.

This fits our use case in that it allows us to create reusable code for our form components. We don't believe, however, that it would enable those on the team not skilled in Ruby-on-Rails to contribute changes easily. Custom `FormBuilder` objects would give increased testability over generic partials.

This would likely have to be used in tandem with something like generic partials for non-form components, which has its own constraints.

#### Generic partials

Ruby-on-Rails utilises [partials](https://guides.rubyonrails.org/layouts_and_rendering.html#using-partials), chiefly for breaking down the rendering process, but also for being able to apply [DRY principles](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) to views.

Generic partials would fit our use case, and is almost certainly the preferred option in terms of enabling those not skilled in Ruby-on-Rails to contribute changes to the markup that makes up our views. However, partials have particular technical constraints. They're much slower in terms of performance than other options, although this is probably negligble given the size of our application and the volume of traffic we're likely to see using it. Most importantly, they can't be tested separately. This means that where we make gains in paying down our technical debt by applying DRY to our views we increase the lack of code reuse by duplicating our testing, effectively shifting the technical debt to our tests.

#### Use of `ActionView Components`

The [ActionView Components](https://github.com/github/actionview-component) framework implements Ruby classes that are used to render views, taking data as input and returning output-safe HTML. They are similar in concept to [React Components](https://reactjs.org/docs/react-component.html).

ActionView Components give greater testability over generic partials alongside greater adherance to DRY principles. They also come with performance improvements. They are not as easy for those not skilled in Ruby-on-Rails to update and maintain as generic partials.

## Decision

Given the benefits, we have taken the decision to move forward with the use of ActionView Components. Where these might be difficult for those not skilled in Ruby-on-Rails to understand, we have agreed to document thoroughly using code comments to ensure that we empower the rest of the team.

## Consequences

The consequences of choosing ActionView Components are:

    * further tying ourselves into the Ruby-on-Rails ecosystem. This will make it harder to move to a different framework or language should we decide that this is something we want to pursue at any point.
    * support for the Gem might cease to exist, although this is unlikely - it has been created by GitHub with the intention of eventually merging into upstream Ruby-on-Rails.
    * we haven't fully tested the constraints of the framework, so might find that it does not fit a further use case in the future.

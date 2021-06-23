# 7. Document the service as we build it

Date: 2020-03-10

## Status

Accepted

## Context

We’re building a service made up of multiple components and integrations, over a long period of time, in an iterative way, with a multidisciplinary team.  

The service includes a Salesforce system, an external facing custom-built application form service, and the integration between them. It also includes integrations with other systems and file storage. The Salesforce system and application form service are both complex pieces of software in their own right, made up of many components, patterns, libraries, frameworks and tests.  

Documentation is one of the ways we ensure that the service is flexible, reliable, and cost-effective to maintain for its entire lifespan, because it means no critical business intelligence or technical detail or decision-making is available only to one or two individuals in the team or organisation. 

## Decision

We will document the technical service as we build it, and host our technical documentation online, in a format which can be iterated over time in a transparent way: https://dsdt-tech-docs.london.cloudapps.digital/  

We will identify areas which are under-documented, and make documenting them an acceptance criteria of the next piece of work which touches that area of the service. 

We will do this instead of documenting the ‘desired state’ before we build, or trying to reverse engineer documentation long after functionality is built.  

This will mean that our documentation is always as comprehensive and accurate as it can be, and closely in sync with what has actually been built, with less risk that smaller steps will be forgotten or skimmed over. This makes our documentation more reliable as a functional maintenance tool.   

## Consequences

Some areas of the service may be identified as known documentation-gaps until we next work on a feature or iteration which touches that part of the service. This is a lower risk consequence than investing time now to document parts of the service from memory or reverse engineered from the outside, because that often leads to gaps or errors in documentation which can cause gaps or errors in related implementation.  

It is preferable to wait if necessary until we are next actively exploring that code or implementation, to document comprehensively and accurately.

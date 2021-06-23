# 8. Take a blended approach to front end build

Date: 2019-12-04

## Status

Accepted

## Context

We have [chosen Salesforce as the underlying Investment Management System.](https://github.com/heritagefund/decision-records/blob/master/product/004-use-Salesforce-investment-management.md) 

We need to build interfaces for applicants, grantees, Register of Support Services (RoSS) consultants and staff to interact with and exchange information through Salesforce.  

We need to balance the benefits of usability, accessibility, and branding customisation with capacity, and the efficiency and value for money of a given approach.  

We can choose a single approach (entirely bespoke, or entirely pre-built or commodity) which represents some compromise on the above for all interfaces and users, with some affected more than others by that single approach for all, or we can take a blended approach which enables us to flex our approach to make the most appropriate balance for each use case.  

A blended approach also gives us more options in the long term to extend bespoke build to other users, use cases or interfaces, move away from Salesforce in future if there is a need to do so, and iterate processes and policy over time as needed by the Fund, whilst delivering the core functionality effectively and efficiently. 


## Decision

We will build a bespoke front end for applicants and grantees.  

These interactions are likely to see the greatest degree of iteration over time, through research and design, and will therefore benefit from the increased flexibility and customisation offered by a fully bespoke front end. We will utilise GOV.UK components and tools to ensure our bespoke efforts focus on those parts unique to the Fund and its users, rather than expending effort building the most common interactions across many digital services.  

This user group is not made up of a discrete, known set of named individuals, so our capacity to provide customised training is limited. It’s therefore most important that we build something for these users which is independently usable and accessible, in order to realise the goals of the service and of SFF as a whole around inclusion and simplicity.  

We will use Salesforce’s own user interface for Fund staff.  

The use cases here largely match those which come ‘out of the box’ with Salesforce. We can provide training, guidance and support to this known, internal user base. We can iterate and flex the design using options provided by Salesforce to maximise usability, accessibility and independent use for staff.  

We will use Salesforce’s ‘Communities’ tooling to create user interfaces for RoSS consultants. The Communities platform gives us additional options for iteration and customisation, whilst minimising the fundamental build work needed to establish a separate bespoke front end. 

RoSS consultants are a known, named group, so we can reliably provide additional training, guidance and support as needed, but these users predominantly work independently, and make use of a smaller number of the caseworking tools that internal staff will regularly need.  

Taken together, this blended approach enables us to strike the right balance of user needs, strategic objectives, and team capacity and capability, whilst delivering usability, accessibility, efficiency and value for money.   

## Consequences

Supplier work will need to include initial Communities build work, as they have the most expertise with this.  

We will need additional front end development input in the short term to ensure we deliver a usable, accessible front end for pilot users. This individual has already been identified, procured, and contracted to undertake 2 sprints (4 weeks) work with the team on this basis.  

We will need to further test the Salesforce interfaces with staff to maximise usability and accessibility, and identify gaps in guidance or training that we must address. These sessions have already been scheduled to take place on 11th and 16th of December, enabling us to iterate the implementation as necessary before the pilot.  

We will need to test the Communities build with RoSS consultants. This is unlikely to be critical for the pilot launch, so we will aim to schedule this in February, to collect input and scope required iterations before the service scales to other countries and areas, or other grant programmes.  

# 11. Prioritise integrationsn with investment-critical systems

Date: 2019-10-17

## Status

Accepted

## Context

We have [selected Salesforce as the platform to underpin the investment management service.](https://github.com/heritagefund/decision-records/blob/master/product/004-use-Salesforce-investment-management.md) Salesforce offers potential for a breadth and number of integrations with other systems across a range of business processes.  

Each integration adds potential complexity and maintenance overhead, alongside any benefits in terms of efficiency, automation, or data accuracy. With that in mind, we need to carefully assess proposed integrations and balance the potential benefits with the potential costs.  

In particular, we need to ensure that we prioritise integrations with a direct and critical role in applying for, assessing or awarding our funding.  

As we are delivering the service, and therefore the platform, in an iterative, user-centred way, we can revisit potential integrations later in the lifecycle of the project as they become important to the stated goals and benefits of the investment service project. This enables us to keep the scope of prioritised integrations tightly focused on our immediate goal of a single, simple investment service for all funding programmes.  

## Decision

We will prioritise integrations with systems we have identified as critical to the provision of an investment service.  

These are Outlook (for email correspondence between staff and applicants and grant recipients), document and data storage, and Proactis (for issuing and fulfilling purchase orders: making payments).   

We will also integrate with Azure Active Directory to support and enable single sign on.  

We also expect to integrate with the heritagefund website to create a seamless user experience. 

## Consequences

This decision necessarily de-scopes several proposed integrations which, whilst potentially valuable, are not critical to the delivery of an investment service. These include tools for managing Freedom of Information requests, uploading and reusing original or commissioned images, and managing contacts.  

We have documented these proposed integrations internally, so that we can revisit them as needed as the service is iterated and enhanced and becomes more sophisticated. This is unlikely to happen before the public beta stage, which is when a basic end to end version of the service is in use across all open programmes and all countries and areas in the UK.  

There is a potential consequence that the business units responsible for these currently descoped integrations will need to implement a system, tool or service more quickly than we are able to prioritise an integration or enhancement of the investment service. In these cases, separate procurement or build activities may be necessary, owned by those business units rather than the team working on the investment service.  

This decision creates dependencies for the investment service on Outlook, data storage, Active Directory, the website, and Proactis.  

Outlook and the website are already in active use across the organisation, Active Directory is currently being rolled out.  

Proactis has recently begun to roll out. We will need to work closely with the Finance and IT teams to ensure we manage this shared dependency together.  

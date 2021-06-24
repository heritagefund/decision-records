# 10. Use Ideal Postcodes for location lookup

Date: 2019-11-20

## Status

Accepted

## Context

Project location is an important factor in managing an application – it helps inform allocation, enables us to identify whether the project will take place in a priority area, and identify which local authority and constituency the project will feature in, which is part of our DCMS reporting.  

Project location also helps Investment Managers and Engagement Managers think about related local projects and organisations that the project would benefit from collaboration with, and helps them consider the appropriateness of the partnerships and contributors noted in the application.  

In order to enable applicants to provide us with accurate postcode information in a simple way, we need a postcode lookup service for applicants using the new application portal.  

Through government licences and public sector access arrangements we have the right to download raw address data, but this data is difficult to access and costly and time consuming to process, and would require us to build our own lookup service to index and search the data. This is not trivial work. For simplicity of development we prefer to use a hosted service to provide this functionality.

## Decision

We will use Ideal Postcodes as the address lookup service. 

## Consequences

This service is not free to use - we will incur a cost for usage. 

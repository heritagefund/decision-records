# 14. Use Salesforce Guidance for Success fields to signpost staff to internal KnowledgeHub content

Date: 2020-03-16

## Status

Accepted

## Context

Projects in Salesforce go through set stages using a feature called Paths. This takes a project through application checks, the adding of a decision meeting, allocation, assessment, recording and confirming the decision and then on to monitoring.  

Each path stage comes with a place where guidance can be placed to assist the user in completing set tasks. This Salesforce feature is called ‘Guidance for Success.’ The character limit on each path stage is 1,000 characters.  

When putting together content to add to a Guidance for Success path stage, it soon became evident that the character limit was not in fact 1,000 characters as formatting text (adding paragraphs etc) and adding hyperlinks counted towards this character limit. This resulted in us refining the content to add to this area and started a wider discussion on how we will use this feature going forward with its limitations in mind.   

## Decision

We will use this feature to signpost users to the associated detailed guidance for staff that is on our internal Knowledge Hub. We will include hyperlinks so that the user is taken directly to the associated guidance.  

We will also use the feature to guide the user on completing set actions on the Salesforce system. Examples of this are how to approve a case paper or how to generate a case paper.  

## Consequences

Staff users will have to move from Salesforce to the Knowledge Hub to read related guidance and then return to Salesforce. We can force the Knowledge Hub web pages to open in a new tab so that the user can have Salesforce and the Knowledge Hub open at the same time in different tabs.  

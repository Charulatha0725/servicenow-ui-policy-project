# ServiceNow UI Policy Project

## Project Title
Enforcing Mandatory Fields Using UI Policies

## Platform
ServiceNow

## Description
This project demonstrates how to enforce mandatory fields using UI Policies in ServiceNow. 
When the Incident State changes to "In Progress", the Priority field becomes mandatory.

## Steps Performed
1. Created a new Update Set.
2. Created a UI Policy for the Incident table.
3. Set condition: State is In Progress.
4. Added UI Policy Action to make Priority field mandatory.
5. Tested the policy in the Incident module.

## Result
When the Incident State is changed to "In Progress", the Priority field becomes mandatory.

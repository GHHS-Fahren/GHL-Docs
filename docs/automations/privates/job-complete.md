<!--   This page is a template for a page explaining a automation workflow   -->
# ServiceM8 Job Completed

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    find-opp[Find Opportunity Based off Job Number Field]:::colour
    upd-prop[Update Property's Last & Next Service Date]:::colour
    add-workflow[Add to the Annual Compliance Due Workflow]:::colour
    first-email[Send 'Job Done!' Email to Client & Wait 1d]:::colour
    second-email[Send 'Same Time Next Year' Email to Client]:::colour

    find-opp --> upd-prop
    upd-prop --> add-workflow
    add-workflow --> first-email
    first-email --> second-email

    classDef colour fill:#02A6F2,stroke-width:0px
```
<!--   This page is a template for a page explaining a automation workflow   -->
# Strata/Body Corp New Lead

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    opp-moved[Opportunity Moved to New Lead]:::colour
    upd-opp[Mark Opportunity Status as Open]:::colour

    opp-moved --> upd-opp

    classDef colour fill:#02A6F2,stroke-width:0px
```
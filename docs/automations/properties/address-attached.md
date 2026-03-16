<!--   This page is a template for a page explaining a automation workflow   -->
# Property Address Attached to Opportunity

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    opp-changed[Address is Attached to Opportunity]:::colour
    conditional{Opportunity Name has 'Service Required' or Address?}:::colour
    not-contain[Add Address to End of Opportunity Name]:::colour

    opp-changed --> conditional
    conditional --"No"--> not-contain

    classDef colour fill:#02A6F2,stroke-width:0px
```
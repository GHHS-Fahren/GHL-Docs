<!--   This page is a template for a page explaining a automation workflow   -->
# Address Creation Form

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    submitted[Sales Submits Address Creation Form]:::colour
    create-address[Create Address Record to No Owner]:::colour

    submitted --> create-address

    classDef colour fill:#02A6F2,stroke-width:0px;
```
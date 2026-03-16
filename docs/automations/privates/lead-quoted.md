<!--   This page is a template for a page explaining a automation workflow   -->
# Private Lead Quoted

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    est-created[Estimate is Created on Opportunity]:::colour
    upd-opp[Move Opportunity to Quoted & Update Value]:::colour

    est-created --> upd-opp


    est-accept[Estimate Has Been Accepted]:::colour
    est-opp-upd[Move Opportunity to Won]:::colour
    notif-sales[Notify Sales of The Won Opportunity]:::colour

    est-accept --> est-opp-upd
    est-opp-upd --> notif-sales


    opp-moved[Opportunity Moved to Quoted]:::colour
    movd-opp-upd[Mark Opportunity Status as Open]:::colour

    opp-moved --> movd-opp-upd

    classDef colour fill:#02A6F2,stroke-width:0px;
```
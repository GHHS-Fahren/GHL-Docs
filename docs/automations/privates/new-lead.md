<!--   This page is a template for a page explaining a automation workflow   -->
# Privates New Lead

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    opp-moved[Opportunity Moved to New Lead]:::colour
    upd-opp[Mark Opportunity Status as Open]:::colour

    opp-moved --> upd-opp


    chat-rep[Client Replied on Chat Widget]:::colour
    notif-sales[Notify Sales of New Lead Via Email]:::colour

    chat-rep --> notif-sales

    classDef colour fill:#02A6F2,stroke-width:0px
```
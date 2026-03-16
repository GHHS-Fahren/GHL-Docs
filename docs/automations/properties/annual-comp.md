<!--   This page is a template for a page explaining a automation workflow   -->
# Annual Complicance Due

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    job-done[ServiceM8 Job Completed Adds to This Workflow]:::colour
    drip-feed[Wait 350d & Drip Feed 1 Every 5 Minutes]:::colour
    notif-sales[Notify Sales of The New Lead]:::colour
    first-email[Send 'Annual Compliance Due' Email & SMS]:::colour
    create-opp[Create New Opportunity in Privates Pipeline]:::colour
    sec-drip-feed[Wait 7d & Drip Feed 1 Every 5 Minutes]:::colour
    sec-notif-sales[Notify Sales The Annual Comp is Overdue]:::colour
    second-email[Send 'Annual Compliance Follow Up' Email & SMS]:::colour

    job-done --> drip-feed
    drip-feed --> notif-sales
    notif-sales --> first-email
    first-email --> create-opp
    create-opp --> sec-drip-feed
    sec-drip-feed --> sec-notif-sales
    sec-notif-sales --> second-email

    client-rep[Client Replied to Annual Compliance]:::colour
    rem-workflow[Remove From ??? Workflow]:::colour

    client-rep --> rem-workflow

    classDef colour fill:#02A6F2,stroke-width:0px;
```
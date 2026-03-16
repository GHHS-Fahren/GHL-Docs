<!--   This page is a template for a page explaining a automation workflow   -->
# Agents Lead Lost

This automation handles the cleanup and tracking for leads moving into the [`Lost`](\pipelines\agents\#pipeline-stages) stage within the [`Agent: New Lead pipeline`](\pipelines\agents).

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    opp-moved[Opportunity Moved to Lost]:::colour;
    del-tags[Remove Lead Tags & Add REA Lost]:::colour;
    opp-upd[Mark Opportunity Status as Won]:::colour;
    rem-camp[Remove From First Contact Campaign]:::colour;

    opp-moved --> del-tags
    del-tags --> opp-upd
    opp-upd --> rem-camp

    classDef colour fill:#02A6F2,stroke-width:0px;
```
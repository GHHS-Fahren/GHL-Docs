<!--   This page is a template for a page explaining a automation workflow   -->
# Agents New Lead

This automation handles the initial categorization and status reset for leads moving into the [`New Lead`](\pipelines\agents\#pipeline-stages) stage within the [`Agent: New Lead pipeline`](\pipelines\agents).

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    opp-moved[Opportunity Moved to New Lead]:::colour;
    del-tags[Remove REA Current Tag & Add REA Lead]:::colour;
    opp-upd[Mark Opportunity Status as Open]:::colour;

    opp-moved --> del-tags
    del-tags --> opp-upd

    classDef colour fill:#02A6F2,stroke-width:0px;
```
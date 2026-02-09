# Agent Lead Won

GHL Name: `Won - Moved To`

GHL Location: `Pipeline: Agents - New Lead / Pipeline Stage: Lost`

## Automation Goal

The goal of the automation is to mark an agent lead as won when its stage gets changed to `won`.

It achieves this by removing `rea lead` tag and adding `rea current` along with removing from the [`Agents - First Contact`](\automations\campaigns\agents\first-contact) automation.

## Automation Process Simplified

```mermaid
flowchart TD
    A[Pipeline Stage Changed To Won]:::orange;
    B[Remove Tags For Leads and Lost]:::orange;
    C[Add REA Current Tag]:::orange;
    D[Remove from First Contact Workflow]:::orange;

    A --> B
    B --> C
    C --> D

    classDef orange fill:#FF6E42,stroke-width:0px;
```

## Automation Process Detailed

```mermaid
%%{init: {"flowchart": {"htmlLabels": true, "useMaxWidth": false}} }%%
flowchart TD
    A["Pipeline Stage Changed
    <a href='\automations\campaigns\agents\first-contact'>In Pipeline: Agents - New Lead</a>
    <a href='\automations\campaigns\agents\first-contact'>Pipeline Stage: Won</a>
    "]:::orange;
    B[Remove Tags:
    rea lead
    rea lost]:::orange;
    C[Add Tags:
    rea current]:::orange;
    D[Remove from Workflows:
    Won - Moved To
    Agents - First Contact]:::orange;

    A --> B
    B --> C
    C --> D

    classDef orange fill:#FF6E42,stroke-width:0px;
```
<!-- This page is a template for a page explaining a automation workflow -->
# Agents First Contact

The goal of the automation is to convert agents after initial contact via sending emails until they either respond or dont.

The automation will be triggered when an opportunity is added or moved to [`Agents - New Lead`](\index)
It achieves this by adding [`rea lead`](\tags\#rea-lead) tag and sending a total of five emails over the course of eighteen days.
If the agent does not respond by then, the previously added tag will be removed and they will me marked as lost.

## <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    A[Opportunity Added to or Moved to New Lead]:::colour;
    B[Remove Conflicting Tags & Add REA Lead]:::colour;
    C[Send 'Here to Help' Email & Wait 36h]:::colour;
    D{Agent Still in Lead State?}:::colour;
    E[Send '4.9 Reputation' Email & Wait 2d]:::colour;
    F{Agent Still in Lead State?}:::colour;
    G[Send 'Our Packages' Email & Wait 4d]:::colour;
    H{Agent Still in Lead State?}:::colour;
    I[Send 'Tenant Tips' Email & Wait 5d]:::colour;
    J{Agent Still in Lead State?}:::colour;
    K[Send 'Agent Follow Up' Email & Wait 5d]:::colour;
    L{Agent Still in Lead State?}:::colour;
    M[Remove Lead Tags And Mark As Lost]:::colour;
    N[Remove From Workflow]:::colour;

    A --> B
    B --> C
    C --> D
    D --"Yes"--> E
    E --> F
    F --"Yes"--> G
    G --> H
    H --"Yes"--> I
    I --> J
    J --"Yes"--> K
    K --> L
    L --"Yes"--> M
    D --"No"--> N
    F --"No"--> N
    H --"No"--> N
    J --"No"--> N
    L --"No"--> N

    classDef colour fill:#02A6F2,stroke-width:0px;
```
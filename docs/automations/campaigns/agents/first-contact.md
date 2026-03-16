# Agents First Contact

The goal of the automation is to convert agents after initial contact via sending emails until they either respond or dont.

The automation will be triggered when an opportunity is added or moved to [`Agents - New Lead`](\pipelines\agents\#pipeline-stages) It achieves this by adding [`rea lead`](\tags\#rea-lead) tag and sending a total of five emails over the course of eighteen days. If the agent does not respond by then, the previously added tag will be removed and they will me marked as lost.

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    opp-moved[Opportunity Added to or Moved to New Lead]:::colour;
    del-tags[Remove Conflicting Tags & Add REA Lead]:::colour;
    first-email[Send 'Here to Help' Email & Wait 36h]:::colour;
    first-check{Agent Still in Lead State?}:::colour;
    second-email[Send '4.9 Reputation' Email & Wait 2d]:::colour;
    second-check{Agent Still in Lead State?}:::colour;
    third-email[Send 'Our Packages' Email & Wait 4d]:::colour;
    third-check{Agent Still in Lead State?}:::colour;
    fourth-email[Send 'Tenant Tips' Email & Wait 5d]:::colour;
    fourth-check{Agent Still in Lead State?}:::colour;
    fifth-email[Send 'Agent Follow Up' Email & Wait 5d]:::colour;
    fifth-check{Agent Still in Lead State?}:::colour;
    clear-lead[Remove Lead Tags And Mark As Lost]:::colour;
    workflow-rem[Remove From Emails]:::colour;

    opp-moved --> del-tags
    del-tags --> first-email
    first-email --> first-check
    first-check --"Yes"--> second-email
    second-email --> second-check
    second-check --"Yes"--> third-email
    third-email --> third-check
    third-check --"Yes"--> fourth-email
    fourth-email --> fourth-check
    fourth-check --"Yes"--> fifth-email
    fifth-email --> fifth-check
    fifth-check --"Yes"--> clear-lead
    first-check --"No"--> workflow-rem
    second-check --"No"--> workflow-rem
    third-check --"No"--> workflow-rem
    fourth-check --"No"--> workflow-rem
    fifth-check --"No"--> workflow-rem

    classDef colour fill:#02A6F2,stroke-width:0px;
```
# School Fundraiser Campaign

The goal of the automation is to [[Automation Goal]]

It achieves this by [[Automation Simplified Steps]]

# <!-- Padding so the chart isnt so close to the text -->

```mermaid
flowchart TD
    pdf-clicked[PDF Link Clicked]:::colour
    pdf-email[Send 'Thank You']:::colour
    rep-replied[Client Replied with Phrase 'More']:::colour
    rep-email[Send 'GHS Funding Initiative' Email]:::colour
    call-clicked[Call Link Clicked]:::colour
    notify[Notify Dan of Conversion]:::colour

    pdf-clicked --> pdf-email
    pdf-email --> notify
    rep-replied --> rep-email
    rep-email --> notify
    call-clicked --> notify

    classDef colour fill:#02A6F2,stroke-width:0px;
```
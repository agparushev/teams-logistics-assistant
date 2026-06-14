# Teams Logistics Assistant

A Power Automate concept for checking shipment information directly from Microsoft Teams using simple chat commands.

## Problem

Logistics users often need to search multiple reports or trackers to find basic shipment information. This creates manual work, delays, and inconsistent answers.

## Solution

A Teams-based command flow where the user types a command such as:

/check REF001

The automation reads the reference, searches a structured Excel table, and posts a formatted response back in Teams.

## Example Command

/check REF001

## Example Response

Reference: REF001  
Status: Delayed  
Country: DE  
LSP: LSP_A  
Owner: Planner_A  

## Technology Used

- Microsoft Teams
- Power Automate
- Excel Online
- SharePoint
- Structured Excel table

## Flow Logic

1. User sends a Teams message.
2. Flow checks if the message starts with `/check`.
3. Flow extracts the shipment reference.
4. Flow searches the Excel table.
5. Flow returns the matching shipment information.
6. If no match is found, the flow returns a clear “not found” message.

## Data Privacy

This repository uses only fictional sample data.  
No real shipment data, customer names, employee names, internal IDs, SharePoint links, or company screenshots are included.

## Current Limitations

- Built as a Power Automate prototype.
- Corporate bot permissions may restrict posting as Flow Bot.
- Posting as user may be required depending on tenant policy.
- Excel is suitable for prototypes but not ideal for large-scale production.

## Future Improvements

- Add `/status REF001`
- Add `/gain REF001`
- Add `/shipment STCC+Booking`
- Add open delay lookup
- Move backend from Excel to SharePoint List or Dataverse
- Add role-based access control

# Flow Logic

## Trigger

Microsoft Teams message is received.

## Command Detection

Check whether the message starts with:

/check

## Reference Extraction

Remove the `/check` command and keep only the project reference.

Example:

Input:
/check REF001

Extracted reference:
REF001

## Lookup

Search the Excel table where:

Reference = REF001

## Response If Found

Return key shipment information:

- Reference
- Status
- Country
- Gain
- Owner

## Response If Not Found

Return:

No shipment found for REF001.

## Permission Note

If Flow Bot posting is blocked by tenant policy, use “Post as user” instead.

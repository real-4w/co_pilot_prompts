For Cowork, I’d make the prompt prescriptive enough that it asks only for the two genuinely variable inputs, then creates and validates the PO.

Recommended prompt
Create a purchase order in D365 F&O.

Before creating the purchase order, ask me for these two required inputs:

1. Vendor
   - Ask for the vendor name or vendor account.
   - Confirm that the vendor exists in D365 F&O before proceeding.

2. Description
   - Ask for a description of what is being purchased.
   - Use the description exactly as provided for both:
     • Product name
     • Text / line description

Use the following fixed values:

Company / Legal entity: 11
Currency: NZD
Procurement category: 6214

Financial dimensions:
Cost centre: 3300
Region: 1010

Create the PO as a procurement-category purchase rather than an item-based purchase.

Before submitting or finalising the purchase order, validate that:

- The legal entity is 11.
- The currency is NZD.
- The vendor is valid for company 11.
- The procurement category is 6214.
- Cost centre 3300 is applied to the purchase line.
- Region 1010 is applied to the purchase line.
- The description I supplied appears in both Product name and Text.
- No inventory/item number has been introduced unless D365 requires one.
- Mandatory accounting or financial dimensions are populated.

If D365 requires information that I have not provided, ask me for it rather than guessing or selecting a default.

In particular, ask for price, quantity, delivery date, delivery address/site, unit of measure or any other mandatory PO field if it cannot be safely derived from D365 defaults.

Before the final creation/submission step, show me a concise summary:

Vendor:
Description:
Company: 11
Currency: NZD
Procurement category: 6214
Cost centre: 3300
Region: 1010
Quantity:
Unit price:
Total:
Delivery date:

Ask me to confirm before performing the final action.

After successful creation, return the D365 purchase order number and its current status.


I would deliberately keep vendor and description as the first two questions, while preventing Cowork from inventing values for price, quantity, delivery or accounting fields. That makes the prompt reusable and considerably safer for live D365 F&O use.
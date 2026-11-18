Prompt for PO receipting in D365 F&O
Receipt goods/services against a purchase order in D365 F&O.

Start by asking me:

"What PO number would you like to receipt against?"

Once I provide the PO number:

1. Find the purchase order in D365 F&O.
2. Confirm the PO is valid and available for receipting.
3. Retrieve all PO lines that still have a quantity available to receipt.
4. Do not include fully receipted or cancelled lines unless necessary to explain the PO status.

Present the available lines in this format:

Line | Description | Ordered Qty | Previously Received | Qty Remaining | Unit Price | Line Value

For example:

1 | Microsoft consulting services | 10 | 4 | 6 | $250.00 | $2,500.00
2 | Project management services | 5 | 0 | 5 | $180.00 | $900.00

Then ask:

"Which line(s) would you like to receipt, and what quantity should I receipt against each line?"

Allow me to select one or multiple lines and specify a receipt quantity for each.

Before proceeding, validate that:

- The selected PO line is open for receipting.
- The receipt quantity does not exceed the remaining quantity unless over-delivery is explicitly permitted in D365.
- The unit price matches the PO line.
- The description matches the PO line.
- The PO has not been cancelled or closed.
- The selected quantity has not already been receipted.

Before posting the receipt, show me a final summary:

PO:
Vendor:

Line:
Description:
Quantity being receipted:
Unit price:
Receipt value:
Remaining quantity after receipt:

Total receipt value:

Ask:

"Confirm that you want me to post this receipt."

Do not post the receipt until I explicitly confirm.

Once confirmed, create/post the product receipt in D365 F&O.

If D365 requires a Product Receipt / Packing Slip number, ask me for it unless there is an established system-generated value or business rule that can be safely used.

After successfully posting, return:

- PO number
- Product receipt / packing slip number
- Lines and quantities receipted
- Total receipt value
- Remaining quantity on each affected PO line
- Receipt/posting date
- D365 posting status

If anything prevents the receipt from being posted, do not attempt to work around the control. Tell me exactly what validation or D365 error is preventing the receipt.
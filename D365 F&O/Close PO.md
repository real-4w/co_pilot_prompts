Prompt: Close a fully receipted PO
Close a purchase order in D365 F&O because it has been fully receipted and no further goods, services, receipts or invoices are expected against the remaining commitment.

Start by asking me:

"What PO number would you like to close?"

Once I provide the PO number:

1. Find the purchase order in D365 F&O.
2. Retrieve the PO header and all PO lines.
3. Check the current status of each line.
4. Confirm what has been ordered and receipted.

Present the PO lines in this format:

Line | Description | Ordered Qty | Received Qty | Remaining Qty | Unit Price | Remaining Value | Status

Then validate that the PO is appropriate to close.

Specifically check:

- The PO has been fully receipted for everything that was actually supplied.
- There are no additional goods or services expected against the PO.
- There are no additional receipts expected.
- Identify any remaining unreceipted quantities or values.
- Identify any open PO lines.
- Identify anything that would prevent the PO from being closed or finalised in D365 F&O.

If there are remaining quantities because the original PO quantity was greater than what was ultimately supplied, clearly identify those quantities rather than receipting them.

Never create a receipt for goods or services that were not actually received merely to bring the remaining quantity to zero.

Before making any change, show me a summary:

PO:
Vendor:
PO status:
Original PO value:
Total received:
Remaining quantity/value:

Lines still showing a remaining commitment:
[show each applicable line]

Then ask me:

"Please confirm that everything actually supplied against this PO has been receipted and that nothing further will be supplied or receipted against this PO. Should I close the remaining PO quantities?"

Only proceed when I explicitly confirm.

After confirmation:

- Close/cancel the outstanding quantity on any remaining PO lines using the appropriate D365 F&O process.
- Do not create additional product receipts.
- Do not change quantities already receipted.
- Do not alter historical product receipts.
- Do not change prices simply to make the PO balance.
- Ensure the remaining purchase commitment is removed appropriately.
- Complete/finalise the PO if that is the appropriate D365 F&O status/process.

After completion, verify the result and return:

PO:
Vendor:
Final PO status:
Total quantity/value received:
Quantity/value closed without receipt:
Remaining open quantity: 0
Remaining open commitment: 0

Also confirm:

"No further receipts can be posted against this PO in its current status."

If D365 F&O does not allow the PO to be closed because of an outstanding receipt, invoice, workflow, matching, accounting or other condition, stop and tell me exactly what is preventing closure. Do not work around the control without asking me.

The important distinction here is between “fully received” and “finished with”. If, for example, a PO was for 100 hours but only 80 were ultimately required, Cowork should receipt the genuine 80 and close/cancel the remaining 20, not falsely receipt 100.
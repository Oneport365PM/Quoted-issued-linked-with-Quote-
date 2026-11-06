# OnePort365 CRM: deals linked to RFQs and quotes

Click-through prototype in `prototype/index.html` (open it in a browser, no build step).

- RFQs, quotes and shipments are linked to deals by the system, never by hand.
- Every deal has an ID (`OP-YY-MM-NNN`), shown on board cards, the list view and the deal page.
- Stage rule: an RFQ is tied to a deal in **Qualified**; a quote is tied to a deal in **Quote Issued**. Each deal shows only the records tied to it.
- Every RFQ, quote and deal number is a clickable link wherever it appears (board chips, list view,
  RFQ / Quote field in Deal Information, RFQ page, quote Booking Details). Deal history does not show RFQ or quote links.
- `RFQ-26-11-015` (Manuchar Trading House Int Nigeria) is linked to the Qualified deal `OP-26-11-023`.
- `Q-26-11-017` (raised from `RFQ-26-11-015`) is linked to the Quote Issued deal `OP-26-11-024`.
- RFQ and quote pages follow the live OnePort365 RFQ and Quotes screens.
- A deal can only move to Quote Issued once a quote has been issued (and auto-linked) for it.
- Moving a deal into Qualified (from Prospect or Contacted) opens a step-by-step KYC checklist (6 steps:
  company details, contact person, trade profile, compliance, payment, documents). Every answer is a checkbox:
  tick, press Next, move to the next step. The stage only changes once the last step is submitted. The result
  (Passed / Needs review, with the reasons) shows on the deal page under "KYC checks".
- Board cards can be dragged between columns. Dropping a Prospect/Contacted deal on Qualified opens the KYC
  checklist and the card moves only when it is submitted (Cancel leaves it where it was). Dropping on Quote
  Issued is blocked until a quote exists; dropping on Closed asks Won or Lost.

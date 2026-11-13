# OnePort365 CRM: deals linked to RFQs and quotes

Click-through prototype in `prototype/index.html` (open it in a browser, no build step).
`OnePort365-CRM-Prototype.html` is a standalone single-file copy to download and open offline.

- RFQs, quotes and shipments are linked to deals by the system, never by hand.
- Every deal has an ID (`OP-YY-MM-NNN`), shown on board cards, the list view and the deal page.
- Stage rule: an RFQ is tied to a deal in **Qualified**; a quote is tied to a deal in **Quote Issued**. Each deal shows only the records tied to it.
- Every RFQ, quote and deal number is a clickable link wherever it appears (board chips, list view,
  RFQ / Quote field in Deal Information, RFQ page, quote Booking Details). Deal history does not show RFQ or quote links.
- `RFQ-26-11-015` (Manuchar Trading House Int Nigeria) is linked to the Qualified deal `OP-26-11-023`.
- `Q-26-11-017` (raised from `RFQ-26-11-015`) is linked to the Quote Issued deal `OP-26-11-024`.
- RFQ and quote pages follow the live OnePort365 RFQ and Quotes screens.
- A deal can move from Qualified to Quote Issued without a quote; the quote links to the deal automatically when it is issued.
- Board cards can be dragged between columns (on touch screens: press and hold, then drag). Dropping on Quote
  Issued moves the deal even with no quote yet; dropping on Closed asks Won or Lost.

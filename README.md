# OnePort365 CRM: deals linked to RFQs and quotes

Click-through prototype in `prototype/index.html` (open it in a browser, no build step).

- Every deal has an ID (`DL-YY-MM-NNN`), shown on board cards, the list view and the deal page.
- One deal can hold many RFQs, each RFQ many quotes, each quote many shipments.
- `RFQ-26-11-015` is linked to the Qualified deal **Regency overseas (rol)** (`DL-26-09-012`).
- `Q-26-11-017` (from `RFQ-26-11-008`) is linked to the Quote Issued deal **Eunisell** (`DL-26-09-008`).
- Moving a deal to Quote Issued is blocked until a quote is linked.

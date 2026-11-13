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
- Moving a deal into Qualified (from any stage, by drag or Edit) opens the checklist at **step A, customer classification**.
  Once sales ticks one, the next screen shows the email that goes to Finance (Nkechim@oneport365.com, okpanachia@oneport365.com) with the customer
  profile (company, contact, product, amount, classification) and an optional note. **Send email to Finance**
  sends it. The deal stays where it is, with a "Finance review" badge, until Finance clears it.
- **Finance › Customer profile reviews** (the $ icon in the left rail, `#finance`) lists deals awaiting review, cleared and sent back in tabs.
  Each review page (`#review-op-…`) shows the company profile (name, industry, RC number, TIN, address, customer history),
  contact details (person, role, email, phone, sales owner) and product details (product type, deal amount), next to the **Customer Payment Terms – Qualifying Checklist** in 3 steps: A. customer classification
  (tick one), B. onboarding requirements (tick all; the credit due-diligence item only applies to credit customers),
  C. clearance. "Finance and Internal Control involved from the onboarding stage" has been removed.
- On the review page, step A (the classification sales picked) is **read only**. Finance completes only their part:
  step B onboarding requirements and step C clearance.
- When Finance clicks **Clear and notify sales**, the sales owner gets a notification (bell in the top bar) that the deal
  is **ready to move to Qualified**. The deal page's Finance review tracker shows a **Move to Qualified** button and the card a "Ready for Qualified"
  badge; sales moves the deal without the checklist popping up again. A later move back into Qualified needs a new review.
  Finance can instead **Send back to sales** with a comment; sales is notified and can resend.
- The deal page has a **Finance review** tracker under the deal header: Sent to Finance (who, when, emailed address) →
  Under review by Finance (when Finance opens the profile) → Reviewed by Finance (cleared, or sent back with the reason).
  The header badge reads Sent to Finance, Under Finance review, Ready for Qualified or Sent back by Finance.
- Sales cannot edit the checklist. Links from the deal page (View customer profile, View review) open a read-only copy of
  the review (`#profile-op-…`) with no tick boxes, no Send back button, and without marking the profile as opened by Finance.
  Only the Finance page (`#review-op-…`, from the $ icon) lets Finance tick steps B and C.
- The checklist pops up on every move into Qualified, even for a deal already with Finance (sending again updates the request).
- Sample reviews: `OP-26-10-014` (Chevron) is awaiting Finance; the Manuchar deals are cleared.
- Board cards can be dragged between columns (on touch screens: press and hold, then drag). Dropping any deal on Qualified opens
  "Send to Finance"; the card moves only when Finance clears it (Cancel leaves it where it was). Dropping on Quote
  Issued moves the deal even with no quote yet; dropping on Closed asks Won or Lost.

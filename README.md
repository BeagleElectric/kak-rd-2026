# K&K Rental Desk

Everything for the rental fleet in one place. Four pages, no login.

## Putting it online

1. New GitHub repo — use a non-obvious name (e.g. `kk-rd-8241`), not `kk-rental-docs`.
2. Upload everything here, keeping the folders: `index.html`, `docs/`, `operations/`, `fleet/`, `shop/`, `robots.txt`, `.nojekyll`.
3. Settings → Pages → Deploy from a branch → `main` → **`/ (root)`**.
4. Wait a minute. URL appears on that same screen.
5. Send Edward the link. On his phone: Share → Add to Home Screen.

`robots.txt` and the noindex tags keep it out of Google. Anyone with the link can still open it, so keep the URL private.

## The four pages

| Page | Who | What |
|---|---|---|
| `/` | Edward | Every document, searchable |
| `/operations/` | Edward | Step-by-step: enquiry → vetting → paperwork → QBO → auto-pay → payment matching → returns |
| `/fleet/` | Edward | All 13 units — status, customer, payment dates, CVIP |
| `/shop/` | Corey & Brett | Trailer in / trailer out, with copy-paste Signal messages |

## Customer vs internal

**Green = send to the customer.** All PDF, all locked against editing, nothing internal on them. Download and email as-is.

**Amber = internal only.** Never send these to a customer. The how-to guides stay as Word so you can edit them.

## SignNow

Customer documents are sent for signature through SignNow as a document group — one envelope, one link,
one signing session. Edward fills in unit, VINs, rate and dates before sending; the customer signs first
and Edward countersigns for K&K. Executed documents land in Dropbox at `/Rentals/Active/`.

Setup instructions are in the manual under **SignNow & Dropbox setup**.

The Schedule B-2 guarantee certificate stays on paper — Alberta requires the guarantor to appear before
a lawyer in person.

## Locked PDFs

Customers open them with no password and can fill the form fields, but can't edit the text, delete pages or copy content out.

**Owner password: `KandK-Rimbey-2026`** — only needed to remove the lock and make changes.

This stops casual editing. It is not unbreakable — someone determined with the right software can strip it.

## Updating a document

Replace the file in `docs/` with the same filename. Nothing else to change.

To add one: put it in `docs/`, then copy an existing line in the `DOCS` list near the top of the script in `index.html`. Add `i:1` for internal (amber); leave it off for customer-facing (green).

## Fleet board

Saves in the browser on that device only — there is no shared database. Once a week Edward hits **Export** and sends the file to Greg. **Import** loads it on another device.

To change units or rates, edit the `FLEET` and `SEED` lists near the top of the script in `fleet/index.html`. No VINs are in this file by design.

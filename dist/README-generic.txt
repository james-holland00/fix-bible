FIX Bible (Generic)

Release: v4.8.0-generic
File: FIX-BIBLE-v4.8.0-generic.html

How to use:
1. Open the HTML file in your browser.
2. Paste one FIX message or a full log block containing multiple FIX messages.
3. Use message tabs to switch active message context.

Highlights:
- Spine layout: raw FIX input and decoded fields are the primary focus; auxiliary modules (Find, Summary, Validation) live in a collapsible right-side icon rail.
- Timeline relocated to the spine and stretches the full width above decoded fields when opened.
- Dictionary lookup returns the exact match in full, plus up to 4 compact related tags under a "Related tags" heading.
- Validation entries default to expanded; All-messages tab aggregates validation badges and highlights every timeline row.
- Sample message updated to a realistic spot FX flow (NewOrderSingle -> ExecutionReport -> ExecutionAck), all with passing BodyLength and CheckSum.
- BN (ExecutionAck) MsgType added to the FIXimate enum dictionary.
- Vendor-neutral branding; all tag definitions/data types sourced from FIXimate; uploaded dictionaries fall back to FIXimate.
- Validation modes, uploaded dictionary profile, and export bundle workflows are preserved.

Package contents (zip):
- FIX-BIBLE-v4.8.0-generic.html
- README-generic.txt
- PATCH-NOTES-generic.txt

Notes:
- Runs fully local in the browser (no network required).

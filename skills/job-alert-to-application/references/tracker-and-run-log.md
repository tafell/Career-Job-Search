# Tracker and Run Log

The user's application tracker lives in ~~tracker (for example a Notion database or a spreadsheet). Its location and column names come from the user's profile. Fetch the tracker's schema before writing, and map the fields below onto the columns that exist. Skip fields the tracker does not have.

## Tracker entry (every role with tailored documents)

1. Deduplicate first: check the posting link column for both the job board link and the employer link, and company plus requisition in the position column. If a row exists, update it in place. Never delete or clear values; note problems in the cons or notes field.
2. Suggested fields:
   1. Company; Position as "<title> (<requisition>)"
   2. Category (from the posting body, using the user's archetype lanes)
   3. Posting status "Open"; work arrangement; employment type; location
   4. Compensation as text, exactly as the posting states it
   5. Posting link = employer posting link; company website
   6. Pros = strongest fit points; Cons = verdict plus gaps (for SETTLE, name the trigger: compensation, level, or both)
   7. Next action = "Decide"
   8. Next step = "Tailored resume and cover letter created <date>: <files> (<save location>). Apply by <deadline>." Prefix "URGENT:" when the deadline is within 3 days
   9. Follow-up date = deadline, or 14 days out if none is posted
3. Page body or notes: source line (posting identifier, verified on employer site, date), verdict, key facts, application materials, and phrasing to confirm before applying.

## Run log (automated mode, or on request)

Create a page or row titled "Job Alert Run Log - <alert date>" next to the tracker:

1. Bottom line, and deadlines within 7 days.
2. Numbered verdicts for every alert line, grouped PURSUE, STRETCH, SETTLE, PASS, one-line reason each. PURSUE and STRETCH add requisition, employer link, compensation, remote status, deadline, fit points, gaps, file names, and tracker link. SETTLE adds requisition, link, compensation, the trigger, and deadline.
3. Additional roles found on employer sites.
4. "Should we add these employers to your target company list?" with numbered employers. Add nothing until the user answers.
5. "Want documents for any SETTLE role?" when SETTLE roles exist.
6. Interpretive phrasing to confirm.

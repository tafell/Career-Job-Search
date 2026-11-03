---
name: job-alert-to-application
description: Runs a job alert end to end, from triage to tailored application materials. Use when the user pastes or receives a job alert email or a list of job links and says "triage these jobs", "go through my job alert", "which of these should I apply to", or "tailor my resume for these". Verifies each role on the employer's own site, drafts a tailored resume and cover letter for the strongest fits, and logs them in the user's application tracker.
---

# Job Alert to Application

Flow: job alert, title triage, full posting review, verification on the employer's careers site, tailored resume and cover letter, tracker entry and run log, summary.

For a deep review of ONE posting, use `job-posting-review` instead.

## Before starting: the profile

Everything personal comes from the user's job search profile (template: `templates/job-search-profile.md` in this plugin). Look for it in the conversation, the project's documents, or a connected folder. It supplies: target roles and level, role archetypes, location constraint, compensation minimum, pass signals, credibility gaps, base resume location, save location, alert source, tracker, and writing preferences.

If there is no profile, ask for the minimum needed (target role and level, location, any compensation minimum, base resume) in one numbered question, and offer to save the answers as a profile. Never hard-code one user's details into this skill.

## Verdicts

1. **PURSUE**: fits an archetype, clears the user's compensation minimum and level, gaps are reframeable.
2. **STRETCH**: fits and clears compensation and level, but a hard requirement hits a credibility gap.
3. **SETTLE**: a great fit on the work itself, but compensation tops out below the user's minimum, or the level is a step down. State the trigger: compensation, level, or both.
4. **PASS**: wrong archetype, hard structural mismatch, or poor fit on the work.

A weak fit that is also below compensation or level is PASS, not SETTLE. SETTLE requires the work itself to be a great fit.

## Modes

1. **Interactive** (user pastes an alert in chat): stop after Step 4 and wait before tailoring (Step 5) and writing to the tracker (Step 6).
2. **Automated** (scheduled run, no one watching): run every step. Tailor for every verified PURSUE and STRETCH. Do not tailor SETTLE roles; list them for the user's decision. Never stop to ask; put questions in the run log and summary.

## Writing rules

1. Bottom line first: verdict before rationale.
2. Number every item and option.
3. Apply the profile's writing preferences (punctuation, abbreviations, tone) to every reply and document.
4. Terse. No narration of the reasoning path.
5. Cite the source link for every compensation, location, deadline, or requirement claim. Label unverified data points.

## Step 1: Get the alert

1. Interactive: use the pasted list.
2. Automated: search ~~email for the profile's alert sender within the last 2 days, newest message. If none, stop with a one-line note. If a run log for that alert date already exists in ~~tracker, stop: already processed.
3. Lines already reviewed earlier (same posting identifier in an earlier run log or this conversation): carry the earlier verdict forward in one line; do not re-open.

## Step 2: Title-only triage

Score each line against the profile:

1. Sort into the profile's archetype lanes.
2. Apply location and pass signals. Postings placed in many small cities are often multi-site placeholders: keep only if remote or near the user.
3. Check the employer's title ladder before judging seniority.
4. Do not PASS at title stage only on compensation or level if the work looks like a great fit; open it and test for SETTLE.

Mark each line "worth opening" or PASS, collapsing the same requisition posted in several cities. Interactive mode: present worth-opening items first, numbered, one-line reason each.

## Step 3: Open the full postings

1. Fetch each posting directly. Avoid email tracking redirect links; open one in a browser to learn the real destination pattern, then fetch the rest directly.
2. Fetch in batches of about three; retry rate-limited pages one at a time. If a page fails twice, report it as unreadable.
3. Job boards often hide qualifications behind a login, so verdicts stay provisional until Step 4.
4. Use the employer's title when it differs from the job board's.
5. Re-score against the profile. Titles mislead both ways.

## Step 4: Verify on the employer's careers site

For every provisional PURSUE, STRETCH, or SETTLE:

1. Find the same requisition on the employer's site, using a browser tool when available. See `../job-posting-review/references/careers-site-patterns.md`.
2. Capture requisition identifier, direct link, posted date, remote status and office days, compensation and incentives, reporting line, application deadline, and full required and preferred qualifications.
3. Re-score with the full qualifications. Downgrade when a hard requirement hits one of the profile's credibility gaps.
4. While on the site, list up to 5 other open roles that fit the archetypes and constraints: title, requisition, location, link, one-line fit read. No documents for these.
5. Read-only: never click Apply, sign in, or fill a form. Close every tab you opened.
6. Flag any deadline within 7 days at the top of the output.

Interactive mode ends here: verdicts grouped PURSUE, STRETCH, SETTLE, PASS; additional roles; and "Should we add these employers to your target company list?" (numbered). Never add to a list without the user's answer.

## Step 5: Tailor resume and cover letter

Only for PURSUE and STRETCH, plus any SETTLE role the user asks for. Follow `references/document-tailoring.md`.

Core content rules:

1. Never invent experience, numbers, titles, or scope. Rephrase and reorder only what is on the base resume.
2. Mirror the posting's vocabulary where truthful.
3. Address gaps by honest reframing, never by claiming the missing experience.
4. Record every interpretive phrase for the user to confirm.

## Step 6: Tracker and run log

Follow `references/tracker-and-run-log.md`: one tracker entry per role with tailored documents (deduplicated), plus a run log in automated mode or on request.

## Step 7: Final message

Bottom line first. Numbered per role: requisition, deadline, file names, what was tailored and why. Then counts (lines reviewed, PURSUE, STRETCH, SETTLE, PASS), tracker entries added or updated with links, the target-list question, the SETTLE documents question when relevant, and the run log link. Close with a short checklist: interpretive phrasing to confirm. Say which steps were skipped if a tool was unreachable. No recap of steps.

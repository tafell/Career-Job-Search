---
name: job-posting-review
description: Evaluates a single job posting in depth against the user's job search profile and gives a clear verdict. Use when the user says "check this job posting", "is this role worth applying to", "pull up this job description and tell me if it fits", "evaluate this posting", pastes a job link, or has a posting open in their browser. Handles LinkedIn and other sites that block plain fetching by using a logged-in browser session when available.
compatibility: Works best with a browser tool (such as Claude in Chrome). Falls back to plain web fetching or pasted text when the page does not require login.
---

# Job Posting Review

Evaluates one posting at a time. For a batch of postings from a job alert, use `job-alert-to-application` instead.

Sites like LinkedIn block automated fetches, and many job pages render content client-side or hide it behind a "see more" toggle. A live, logged-in browser tab sees what the user sees; a plain fetch often does not.

## Step 1: Get the posting

1. If a browser tool is available, check open tabs first. Reuse the tab if the posting is already open; otherwise open a new tab and navigate to the link.
2. If the page is behind a login wall, never enter credentials. Ask the user to log in in that tab and say when it is ready.
3. With no browser tool, try a plain fetch. If it is blocked or truncated, ask the user to paste the full posting text.

## Step 2: Extract the full posting

Read the page text. If the description looks cut short (ends mid-sentence, or is much shorter than the page), find and click the "see more" or "show full description" control and read again. Never evaluate a truncated description.

Capture: title, company, exact location and remote, hybrid, or on-site status, compensation (note explicitly when none is disclosed), full responsibilities and requirements, and live-status signals (applicant count, "no longer accepting applications", repost date).

For employer applicant tracking system quirks, see `references/careers-site-patterns.md`.

## Step 3: Know the profile

Use the user's job search profile (template: `templates/job-search-profile.md` in this plugin) from the conversation, project documents, or a connected folder: target role and level, location constraint, compensation minimum, focus areas, pass signals, and credibility gaps. If none exists, ask briefly for role, level, location, and any minimum before evaluating. A fit judgment without a profile is a summary, not an evaluation.

## Step 4: Evaluate axis by axis

1. **Role and level**: does the scope match, or is it a level up or down, or a different function with a similar title? Check the employer's title ladder (an Associate Vice President at some employers sits above Director; "Vice President" at large banks is mid-level).
2. **Location**: does it clear the constraint, including fine print (state eligibility lists, "hybrid" that means four days on-site)?
3. **Compensation**: does the disclosed range clear the user's minimum? If undisclosed, say so; never assume it clears.
4. **Focus and industry**: in the target space, or adjacent?
5. **Gating requirements**: hard years, degree, credential, tool, or clearance requirements that would screen the candidate out.

Separate hard requirements from preferred ones; do not let the user rule themselves out over a "nice to have".

## Step 5: Verdict

Lead with an explicit verdict: strong fit, worth a shot, a reach, or pass. Follow with one or two sentences naming the specific reason. Cite the source link for every compensation, location, deadline, or requirement claim, and label anything unverified.

## Step 6: Next step

Offer one of: a tailored resume bullet or summary using the posting's language (see `executive-resume-coach`), a note to recheck the posting later, or moving to the next posting.

## Scope

This skill evaluates a posting; it does not submit applications. Submission needs the user's own login. Drafting tailored materials is in scope.

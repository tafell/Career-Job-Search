# Getting Started

Choose your first task and supply the inputs it needs.

## Set up the tools you already use

Start with one task. To collect openings, paste one alert or a few links. To tailor a resume, provide the posting and your source resume. Add tracking or scheduling when you want those steps.

| Number | Decide once in your private profile | If you prefer to work manually |
| --- | --- | --- |
| 1 | Where openings come from: selected email senders, a job board, or employer sites. For multiple alerts, specify which sources to check. | Paste an alert, link, or posting text. |
| 2 | Where the source resume lives, which version to use, and where to save new documents. | Upload the source and download each result. |
| 3 | Where applications are tracked, which columns identify a role, and which status means you submitted it. | Ask for a copyable row in your column order. If starting from scratch, try employer, role, posting link, status, and next action. |
| 4 | Where processed alerts are logged. This may be a separate worksheet, database, or file. | Keep a dated list of processed alerts and supply it when you want earlier runs checked. |
| 5 | When to run: on request or on an authorized schedule. For recurring checks, specify frequency, time zone, and how far back to look. | Request a one-time check whenever you need one. |
| 6 | Which contact data you want to use for outreach after applying. | Paste a short list of relevant contacts with the relationship details you are comfortable sharing. |

**Try this setup request:** “Help me set up my first job search task. Read my private profile or use what I have already told you. Ask one numbered question for anything essential that is missing. Tell me which inputs you can actually read, where the result will go, and what I will need to copy myself.”

**Check one example first.** Supply one alert and ask for its openings and a proposed tracker row. If using a connected tracker, ask the assistant to read the column names and find an existing record. Decide separately whether it may write updates. For scheduled work, check that the scheduled run can reach the same sources.

See [Tools and Troubleshooting](../CONNECTORS.md) for sender filters, tracker migration, and manual alternatives.

## Prepare once

1. Copy [the shared profile](../templates/job-search-profile.md) into a private location.
2. Fill in targets, lanes, constraints, pass signals, gaps, documents and tools, and writing preferences. Use document locations that your chosen assistant can actually access.
3. Replace the compensation example with your own minimum and specify currency and pay period in compensation notes. If absent, the skills disclose a fallback of 100000 <!-- PLACEHOLDER: 100000 is an example value, not a recommendation. Replace it with your own minimum base salary. -->
4. To disable pay screening, explicitly write "Skip compensation screening" in compensation notes or the conversation. The unchanged template's suggestion to delete the line is outdated: deletion alone uses the fallback in both platform versions.
5. For full resume tailoring, supply your original resume. Previous generated drafts can help compare wording but cannot independently establish achievements.

## Claude setup

1. Use the four complete skill folders under [skills](../skills/), retaining their reference folders.
2. For a project-based workflow, upload the selected instructions, reference files, private profile, and source resume. Give files distinct upload names if needed.
3. Paste the selected skill's instructions into project instructions where supported, or paste them at the start of a conversation. State which workflow to follow.
4. If your Claude environment supports skill installation, use its supported import process for the complete folder. This repository does not require a downloadable plugin release. Availability depends on your environment.
5. Start with: "Use job-posting-review to evaluate this posting against my profile and resume. Verify the employer source and keep unsupported conclusions provisional."

## ChatGPT setup

1. Follow the [ChatGPT setup guide](../chatgpt/README.md). Create a private project, upload the profile and source documents, and paste the selected instructions.
2. For the alert coordinator, also upload discovery, posting review, resume coaching, and search coordination instructions. The coordinator needs those files to run the full workflow.
3. Use the custom assistant configurations only where creation or editing is available. The project route works without creating a custom assistant.
4. Start with: "Use executive-resume-coach to review my uploaded resume against this posting. Identify the baseline and ask for missing evidence before drafting dependent claims."

## Check your first result

1. Confirm the assistant used the correct profile and resume version.
2. Check the source date, employer link, verdict, and unresolved requirements.
3. Review every career claim and interpretive phrase before using the materials.
4. Confirm any reported save or tracker update actually succeeded. Prepared materials do not mean an application was submitted.


## Public announcement only

1. Follow [Job Search Announcement](JOB-SEARCH-ANNOUNCEMENT.md). This standalone workflow needs no posting, tracker, connection export, or other skill.
2. Supply a private profile or answer the bundled input question. A source resume is optional when your answers provide enough evidence for the post.

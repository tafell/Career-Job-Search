# Getting Started

Start with your private profile and source resume. Connected tools are optional.

## Prepare once

1. Copy [the shared profile](../templates/job-search-profile.md) into a private location.
2. Fill in targets, lanes, constraints, pass signals, gaps, documents and tools, and writing preferences. Use document locations that your chosen assistant can actually access.
3. Replace the compensation example with your own minimum and specify currency and pay period in compensation notes. If absent, the skills disclose a fallback of 100000 <!-- PLACEHOLDER: 100000 is an example value, not a recommendation. Replace it with your own minimum base salary. -->
4. To disable pay screening, explicitly write "Skip compensation screening" in compensation notes or the conversation. The unchanged template's suggestion to delete the line is outdated: deletion alone uses the fallback in both platform versions.
5. Supply your original resume. Previous generated drafts can help compare wording but cannot independently establish achievements.

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

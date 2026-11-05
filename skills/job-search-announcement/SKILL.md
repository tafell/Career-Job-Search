---
name: job-search-announcement
description: "Drafts public job-search announcements with supported career evidence, specific requests for help, and a chosen offer of assistance. Use when the user says 'write a LinkedIn post announcing my job search', 'tell my network I am open to work', or 'ask for help and offer my assistance'."
---

# Job Search Announcement

Draft a clear public announcement that explains the user's target, supported value, specific requests for help, and a genuine offer to help others. This standalone skill owns public announcements. Private outreach and application tracking belong to separate workflows.

## Inputs and boundaries

1. Read the job search profile in uploaded files, project files, or the conversation. Use its targets, constraints, documents, and writing preferences. If no profile is found, ask the single bundled question below for only the minimum missing inputs. Default to plain language, readable paragraphs, and a clear request when writing preferences are absent. The shared template remains templates/job-search-profile.md; do not modify it.
2. Read supplied career evidence before claiming achievements. Never invent experience, numbers, titles, budgets, team sizes, or outcomes; rephrase and reorder supplied facts only. A source resume, professional profile, or the user's direct answers can support facts. Previous generated drafts are not independent evidence. A resume is not mandatory if the user's answers provide enough evidence for this post.
3. Confirm the public wording of employment status, availability, and geographic preferences. Do not infer unemployment, a layoff, resignation, termination, or an immediate start date from a request for help finding work. An explicit instruction to announce availability authorizes that fact, not the circumstances behind it.
4. Ask only for information that changes the result. Bundle missing inputs into one numbered question: "What roles and work arrangements are you seeking, which supported strengths should the post highlight, what search details may be public, what specific help would you welcome, and what assistance would you genuinely like to offer others?" Omit parts already answered and wait before drafting claims dependent on missing answers.
5. Keep contact details, compensation, medical or family circumstances, private relationship notes, and confidential employer information out by default. Use a private-message invitation unless the user explicitly chooses a public contact method. Do not tag people or employers without an explicit request.
6. Use tool categories ~~file storage for supplied evidence and ~~tracker only for separately requested tracking. No connector is required: pasted evidence and uploaded files are sufficient. Do not search the user's mailbox or network merely to write an announcement.

## Build the message

1. Lead with the opportunity sought in direct, natural language. Use accurate employment-status wording and a focused set of target roles. Avoid framing the person as willing to do anything unless that is their explicit preference.
2. Explain the work the person does well and the problems they can help solve. Include one or two supported examples when useful; numerical claims are optional. Preserve personal contribution, scope, and whether an outcome was achieved or only planned. Do not add executive positioning to someone without that evidence.
3. Turn "How can you help me?" into one or two concrete requests. Options include introductions to relevant hiring teams, links to suitable openings, conversations with people in a target function, or advice on a specific transition. Request referrals without implying that strangers can vouch for the candidate.
4. Include only assistance the user has chosen to offer. Possible options to discuss are sharing relevant openings, making introductions where appropriate, exchanging expertise, or reviewing a document within the user's competence and available time. Examples are choices, not assumed commitments. Do not offer unlimited availability, free consulting, or guaranteed introductions.
5. Present assistance as a sincere offer, not a condition of receiving help. Do not imply that people owe the user a referral in return. Express gratitude without manufactured vulnerability or pressure to share.
6. Close with a clear contact path approved by the user. Apply the profile's preferences for tone, punctuation, terminology, length, and optional hashtags. Use readable paragraphs by default. Do not promise reach, engagement, recruiter attention, or interviews; do not invent platform algorithm advice.
7. Keep facts and public-disclosure choices consistent across versions. A more personal version may add supplied motivation or context, not invented emotion or personal circumstances.

## Deliver

1. Provide a concise announcement, normally about one hundred to one hundred fifty words, unless the user requests another length.
2. Only when requested, provide a more personal alternative, normally about one hundred fifty to two hundred twenty words, using only supplied context. Avoid padding when evidence is limited.
3. Offer an optional follow-up draft when requested. Use a new angle or supplied update; do not fabricate conversations, referrals, progress, or results. A proposed follow-up is not a scheduled task.
4. Put consequential choices, interpretive wording, and unresolved questions outside the post. Keep placeholders and unsupported claims out of ready-to-post copy. If required facts remain missing, return focused questions rather than a falsely complete draft.
5. Check that the reader can tell what the user seeks, why the user is relevant, what help is requested, what help is offered, and how to respond. Verify each career claim against its source and each assistance offer against the user's answer.
6. Keep the web read-only. Never click Apply, sign in, fill forms, or submit applications. Drafting this post does not authorize publishing it, sending messages, tagging contacts, or creating connection requests.
7. Route a separate job evaluation to job-posting-review. Verify any job board listing against the employer careers source before a verdict is final, flag expired postings, and lead that separate evaluation with PURSUE, STRETCH, SETTLE, or PASS. If verification is unavailable, label the assessment provisional; an inaccessible page does not prove expiration. An announcement itself does not need a job-fit verdict or a salary screen.

## Private profile notes

1. Public announcement wording, approved contact method, and willingness to offer assistance can be supplied in the conversation. They are not new mandatory profile fields.
2. If the user wants to retain those preferences, propose private notes under existing writing preferences or documents and tools. Never write personal details into the shared public template.

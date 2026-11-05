# Job Search Workflows for ChatGPT

Use nine reusable skills grouped by purpose with the same private profile used by the Claude versions.

[See the job search workflow diagram](../guides/WORKFLOWS.md#job-search-workflow) to choose your starting point.

## Skills

| Number | Group | Skill | What it produces | Example request |
| --- | --- | --- | --- | --- |
| 1 | Public networking | [job-search-announcement](skills/job-search-announcement/SKILL.md) | Public announcement drafts with specific asks and a chosen offer of help | Announce my job search and offer assistance to others. |
| 2 | Career direction | [career-direction](skills/career-direction/SKILL.md) | Target lanes, positioning, and development gaps | Help me choose credible target roles. |
| 3 | Opportunity discovery | [opportunity-discovery](skills/opportunity-discovery/SKILL.md) | Deduplicated openings with source status | Find new openings at my target companies. |
| 4 | Opportunity evaluation | [job-posting-review](skills/job-posting-review/SKILL.md) | Evidence-backed fit verdicts | Which of these jobs should I pursue? |
| 5 | Career and application materials | [executive-resume-coach](skills/executive-resume-coach/SKILL.md) | resumes, cover letters, profiles, and biographies | Tailor my resume using my uploaded baseline. |
| 6 | Application tracking | [search-coordination](skills/search-coordination/SKILL.md) | Tracker records, conversions, deadlines, and next actions | Convert my tracker and record my next follow-up date. |
| 7 | Private networking | [job-connection-outreach](skills/job-connection-outreach/SKILL.md) | Ranked contacts and private message drafts | I applied for this role. Who could introduce me to the hiring team? |
| 8 | Interview preparation | [interview-preparation](skills/interview-preparation/SKILL.md) | Story bank, interview brief, practice, and debrief | Build stories for different interview questions. |
| 9 | Coordination across groups | [job-alert-to-application](skills/job-alert-to-application/SKILL.md) | Discovery, review, materials, and tracking | Process these alerts and prepare materials for suitable roles. |

## Set up a private project

1. Download the shared [job search profile](../templates/job-search-profile.md). Fill in a private copy once. Do not modify the public template.
2. Create a private ChatGPT project and upload the filled-in profile, source resume, and relevant skills. Give uploaded skill files distinct names if the interface cannot distinguish their folders.
3. In project settings, paste the selected skill's numbered instructions, omitting its metadata header. For several workflows, upload all selected instructions and add: "Read my job search profile first. Read and follow the named workflow file before each task. Keep candidate facts grounded in my source documents. Do not submit applications."
4. Upload all four sibling workflows required by job-alert-to-application when using that coordinator. Uploading these files provides instructions for use; it does not by itself install an automatically triggered skill.
5. Start with the matching example request. With no connected tools, paste posting text and alerts and upload documents or tracker exports.
6. Keep the profile current. Update the existing private copy rather than maintaining contradictory versions.

## Custom assistant configurations

1. [Executive Resume Coach](custom-gpts/executive-resume-coach.md) supports repeated accomplishment coaching and document revisions.
2. [Interview Preparation](custom-gpts/interview-preparation.md) supports ongoing story development and practice.
3. Where creation is available, create a custom assistant, paste its Full instructions section, add its conversation starters, enable web search and code interpreter with data analysis, and upload the blank profile template as knowledge. For an existing editable assistant, use its configuration settings.
4. Personal accounts cannot currently create new custom assistants. Creation and editing availability depend on account and workspace. Use the project route when creation is unavailable. These files are configuration blueprints, not claims that assistants have been installed or published.

## Shared profile and tools

1. The existing seven profile sections remain unchanged. Target roles and aspirations guide selection, never establish past achievements.
2. Tool categories are `~~email`, `~~file storage`, and `~~tracker`. Connectors are optional. Pasted text, uploaded files, and downloadable outputs are the fallback.
3. If the profile lacks a compensation minimum, these workflows use 100000 <!-- PLACEHOLDER: 100000 is an example value, not a recommendation. Replace it with your own minimum base salary. --> and disclose that fallback. Pay shown as 0 or 1 is undisclosed. Unknown currency or pay period prevents a final pay comparison.
4. Compatibility note: the shared template currently says deleting its compensation line skips screening. Both platform versions follow the release requirement instead: absence uses the disclosed fallback. To skip screening, explicitly instruct the assistant to do so. The shared template has not been changed.
5. Candidate details and writing preferences belong in the private profile. Proposed additional settings are listed below; no new mandatory profile sections have been introduced.

## Proposed profile additions

1. Constraints: compensation currency and pay period; employment types; travel limits; relocation willingness; work eligibility and sponsorship needs, only when relevant and voluntarily supplied.
2. Documents and tools: prioritized target companies; alert lookback window; monitoring frequency and timezone; last checked record; interview story bank location.
3. Search coordination: preferred follow-up interval and any explicitly authorized scope for tracker changes. A profile entry is not blanket permission to send correspondence or submit applications.
4. Interview date, participants, recipient details, and individual deadlines are task-specific inputs and do not need permanent profile fields.

## Privacy

1. Never commit filled-in profiles, resumes, cover letters, contact lists, alerts, tracker exports, interview stories, or personal documents to this public repository.
2. Never place private candidate files in the knowledge of a publicly shared assistant or a shared project.
3. Inspect the files shown in the upload before committing. This package contains instructions only, with no candidate history, contact details, or private workspace links.
4. The user submits applications. The assistant never clicks Apply, signs in, or fills web forms. Correspondence stays in draft until explicitly authorized.

## Relationship to the Claude versions

1. The Claude versions remain in the repository's [skills folder](../skills/). This release retains them and aligns their shared evidence, verdict, compensation, and web rules.
2. The names executive-resume-coach, job-posting-review, job-alert-to-application, and job-search-announcement are retained for equivalent work.
3. ChatGPT separates discovery, evaluation, materials, and tracking into independent owners. The alert workflow coordinates those owners instead of embedding all their procedures.
4. The resume workflow requires a supplied baseline for full tailoring and adds profiles and biographies. Cover letter and tracker methods are adapted from the existing Claude reference files.
5. Job review uses consistent PURSUE, STRETCH, SETTLE, and PASS labels. It explicitly handles unknown pay, missing currencies, expired postings, and source failures.
6. Both versions avoid requesting sign-in, recheck stale verdicts, and require scheduled actions to stay within their authorized scope.
7. Job Search Announcement has identical standalone instructions for both platforms. Career direction, discovery, coordination, and interview preparation are separately packaged additions. Outreach guidance is a new conservative implementation, not a recovered historical prompt.
8. These two custom assistant blueprints are newly composed from the packaged workflows. Original custom assistant instructions were not available.

## Sources and checks

1. The supplied resume-adviser project instructions, visible workflow history, and existing Claude skills informed this package. Historical personal achievements were excluded.
2. The Claude resume coach credits Lisa Rangel's [article on executive resume coaching](https://www.hellersearch.com/blog/stop-asking-ai-to-write-your-executive-resume). This package retains attribution for that inherited coaching sequence; it does not reproduce the article.
3. Setup references: [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-projects-in-chatgpt) and [Creating and editing custom assistants](https://help.openai.com/en/articles/8554397-creating-and-editing-gpts), checked November 3, 2026.
4. See [release checks](RELEASE-CHECKS.md) for validation results and limitations.



## Job-specific connections

1. After submitting your application, use Job Connection Outreach to find relevant connections, distinguish verified relationships from public prospects, and draft insight, introduction, or referral requests. See [the connection guide](../guides/JOB-CONNECTIONS.md).
2. Supply the posting and private connection data. Public search alone does not reveal your network. Nothing is sent automatically.

## Public job-search announcements

1. The standalone Job Search Announcement skill drafts public announcements with specific requests for help and a user-chosen offer of assistance. See [the announcement guide](../guides/JOB-SEARCH-ANNOUNCEMENT.md).
2. Supply career evidence and public-disclosure preferences. The workflow produces one concise draft by default. Ask for a longer personal version if desired.

## Requests for materials and interviews

1. Executive Resume Coach: Draft a cover letter for this posting using my source resume.
2. Executive Resume Coach: Rewrite my professional profile for the roles in my private profile.
3. Executive Resume Coach: Write a short speaker biography from my supplied experience.
4. Interview Preparation: Build a story bank from my experience before I have an interview scheduled.
5. Interview Preparation: Help me practice for this specific interview, one question at a time.

# Career Job Search

A Claude plugin for senior leaders running a job search. Three skills that work together:

| Skill | What it does | Say something like |
| --- | --- | --- |
| `executive-resume-coach` | Interviews you about an accomplishment, tests it for specificity and differentiation, and rewrites it using only evidence you supply. Never invents numbers or scope. | "Help me strengthen this resume bullet" |
| `job-posting-review` | Pulls one posting (including LinkedIn, through a logged-in browser), checks it against your profile axis by axis, and gives a clear verdict: strong fit, worth a shot, a reach, or pass. | "Is this role worth applying to? <link>" |
| `job-alert-to-application` | Takes a job alert email or list of links, triages every line, verifies the strongest roles on the employer's own careers site, tailors a resume and cover letter for each, and logs them in your tracker. Can run on a schedule. | "Triage today's job alert" |

## Get started

1. **Install the plugin.**
   - Claude Code: run `/plugin marketplace add tafell/career-job-search`, then `/plugin install career-job-search@career-job-search`.
   - Claude desktop or web: download this repository and upload the `.plugin` file from the latest release, or upload each folder under `skills/` as a custom skill.
2. **Fill in your profile.** Copy [`templates/job-search-profile.md`](templates/job-search-profile.md), fill it in, and keep it where Claude can see it (a Claude Project document works well). The skills read your targets, constraints, and document locations from it, so nothing personal lives in the skills.
3. **Connect tools (optional).** See [`CONNECTORS.md`](CONNECTORS.md). Everything also works by pasting text and attaching files.

## Design principles

1. **Evidence only.** Resume and cover letter text traces to what you supplied. Interpretive phrasing is flagged for you to confirm.
2. **Verify at the source.** Job board listings are checked against the employer's own careers site before a verdict is final; expired postings are flagged, not silently dropped.
3. **Read-only on the web.** The skills never click Apply, sign in, or fill forms. You submit applications yourself.
4. **Verdict first.** Every review leads with the bottom line.

## Privacy

Do not commit a filled-in profile, resume, or tracker export to a public fork. The `.gitignore` excludes common file names for these.

## Credits

`executive-resume-coach` is adapted from Lisa Rangel's article [Stop Asking AI to Write Your Executive Resume](https://www.hellersearch.com/blog/stop-asking-ai-to-write-your-executive-resume), published by Heller Search.

## License

MIT. See [`LICENSE`](LICENSE).

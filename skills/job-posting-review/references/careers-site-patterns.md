# Careers Site Patterns

Practical notes for reading postings on employer careers sites. Always read-only: never click Apply, sign in, or fill a form. Close every tab you opened.

## Workday

- Search URL pattern: `https://<company>.wd<N>.myworkdayjobs.com/<SiteName>?q=<title keywords>`
- The description lives in the element `[data-automation-id="jobPostingDescription"]`.
- Location and pay often render client-side and do not appear in a plain fetch. Use a live browser, or check the search results page, which often shows location even when the posting does not.

## Sites that render slowly

- Reject optional cookies, then wait about 3 seconds before reading.
- When page text comes back empty, wait a few seconds and read `document.body.innerText` with a javascript tool, in slices if it is long.

## Search result pages that list job links

- Collect the job links from the results page with a javascript tool (for example, anchors whose link contains `/job/`), then open each job page.

## Job board aggregators

- Aggregator titles can differ from the employer's real title. Always use the employer's title.
- Many aggregator hits are expired. Flag expired postings rather than dropping them silently, so the user knows what was checked.
- Tracking links in alert emails are often too long to fetch. Open one in a browser to learn the destination pattern, then fetch the rest directly.
- Some job boards rate-limit parallel fetches. Fetch about three at a time and retry failures one at a time.

## Company facts

- Verify headquarters and office claims against a primary source (the company's own about page or published documents) rather than inferring from the city on one posting.

# Document Tailoring

How to build a tailored resume and cover letter from the user's base documents while preserving their formatting.

## Inputs

1. Base resume: from the location in the user's profile (~~file storage, a connected folder, or an attachment). Prefer the original Word file so fonts and layout survive.
2. Prior cover letters (optional): read for voice. A strong default shape is an employer-specific hook, two evidence paragraphs with concrete results, why this employer, and a short close.

Large Word files with embedded fonts can overflow a file-download tool response. If that happens, save the response to a temporary file, parse it, and decode the file content, or ask the user to attach the file directly.

## Resume build (python-docx)

1. Print a numbered paragraph index of the base resume first, and note which paragraphs hold the headline, summary, competencies, and the first role's bullets. Never assume positions from a previous run.
2. Replace text run by run, removing surplus runs, so formatting is preserved.
3. Reorder bullets within a role by moving paragraph elements; do not move bullets between roles.
4. Keep the headline to one line, competency cells short enough not to wrap, and any skills chain short.
5. Render to PDF (for example with LibreOffice), look at page 1, and confirm the page count equals the base resume's.

## Cover letter build

1. Copy the base resume document so fonts and margins match. Keep the name and contact lines; remove everything else.
2. Add: date, "Hiring Team", company, bold "Re: <title> (<requisition>)", salutation, four paragraphs, sign-off, and the user's name.
3. Keep it to one page.

## Content rules

1. Never invent experience, numbers, titles, or scope.
2. Mirror the posting's vocabulary only where truthful.
3. Reframe gaps honestly (for example, procurement experience from the buying side of technology), never by claiming the missing experience.
4. Bullets carried over unchanged from the base resume may keep keywords as written for applicant tracking systems; mention this in the final note if the user's writing preferences would otherwise change them.
5. List every interpretive phrase for the user to confirm before applying.

## File names and saving

1. Name files `<Name>_Resume_<Company>_<Role>.docx` and `<Name>_CoverLetter_<Company>_<Role>.docx`.
2. Save to the location in the user's profile (~~file storage or a connected folder). If that is not reachable, send the files directly to the user in chat. Say which happened.

# Resume Project

## Tailored Resume Output

When producing a tailored resume PDF for a specific job/company:

1. Edit `resume.tex` with the requested changes
2. Compile with `latexmk -xelatex -quiet -g resume.tex`
3. Copy `resume.pdf` to `~/tailored_resumes/<CompanyName>/kevin_ha_resume.pdf` — create the company subdirectory if it doesn't exist (e.g. `~/tailored_resumes/Versant/kevin_ha_resume.pdf`)
4. Output **only the PDF** to that folder — no `.tex`, `.log`, or other files
5. Revert `resume.tex` with `git restore resume.tex` so the master copy stays unchanged

## Permanent Resume Updates

When `resume.tex` itself is permanently changed (new job, new bullet, updated metrics/skills — i.e. the change is meant to be committed, not reverted like a tailored-resume edit above):

1. After editing `resume.tex`, update `.claude/resume-profile.md` (the plain-text cache) to match — see the "Last synced" line/commit noted at the top of that file.
2. Also update the Obsidian master history doc at `/Users/tum/Library/Mobile Documents/iCloud~md~obsidian/Documents/Personal/Job Stuff/Master Resume.md`:
   - If it's a new bullet/role, add it to the relevant section with appropriate `#tags`.
   - If it's a reworded bullet for an *existing* accomplishment, update the current line and move the prior wording into an `*Alt*` line underneath (don't just delete history).
   - Bump the "Last rebuilt" line at the top with today's date and the new commit hash (once committed).
3. This sync only happens when changes go through Claude Code. If `resume.tex` is ever hand-edited outside a session, ask Claude to "sync my resume history" afterward to catch it up.

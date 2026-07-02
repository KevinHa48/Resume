# Resume Project

## Tailored Resume Output

When producing a tailored resume PDF for a specific job/company:

1. Edit `resume.tex` with the requested changes
2. Compile with `latexmk -xelatex -quiet -g resume.tex`
3. Copy `resume.pdf` to `~/tailored_resumes/<CompanyName>/kevin_ha_resume.pdf` — create the company subdirectory if it doesn't exist (e.g. `~/tailored_resumes/Versant/kevin_ha_resume.pdf`)
4. Output **only the PDF** to that folder — no `.tex`, `.log`, or other files
5. Revert `resume.tex` with `git restore resume.tex` so the master copy stays unchanged

# ATS CV Optimizer — A Claude Skill

A [Claude Skill](https://www.anthropic.com/news/skills) that reviews your CV/resume for **ATS (Applicant Tracking System)** compatibility, rewrites it for maximum keyword impact, and generates a clean, ATS-safe **PDF**.

> Many CVs are rejected by software before a human ever reads them. This skill helps you fix the issues that cause that.

---

## What It Does

| Step | Output |
|------|--------|
| 1. **Review Report** | ATS score out of 100 across 6 dimensions, plus Critical Issues (🔴), Warnings (🟡) and Suggestions (🟢) |
| 2. **Content Rewrite** | Stronger action verbs, quantified bullet points, ATS-friendly section headings, better keywords |
| 3. **PDF Generation** | Single-column, selectable-text, ATS-safe PDF (A4) |
| 4. **Summary** | Top 3 changes made and why |

### Scoring Dimensions

| Dimension | Weight |
|-----------|--------|
| Keyword Relevance | 25% |
| Formatting & Parsability | 20% |
| Quantified Achievements | 20% |
| Section Structure | 15% |
| Action Verb Quality | 10% |
| Contact & Metadata | 10% |

---

## When to Use This Skill

Use it when you want to:

- Check whether your CV is **ATS-friendly**
- Understand **why your CV is not getting shortlisted**
- Improve your CV for **tech / software roles**
- Rewrite weak bullet points with measurable impact
- Convert your CV into a clean **ATS-safe PDF**
- Match your CV against a **specific job description** and see a keyword match rate

Claude triggers this skill automatically when you paste or upload CV/resume content, or when you say things like:

- "Review my CV"
- "Make my CV ATS friendly"
- "Optimize my resume"
- "Convert my CV to PDF"
- "My CV is not getting shortlisted"
- "Improve my resume for tech jobs"

---

## Installation

### Option 1: Claude.ai (Web / Desktop / Mobile)

1. Download the latest `ats-cv-optimizer.zip` from the [Releases](../../releases) page.
2. Open Claude → **Settings** → **Skills** (the exact menu name may vary by version).
3. Click **Upload skill** and select the zip file.
4. Enable the skill.

> The zip must contain the `ats-cv-optimizer/` folder with `SKILL.md` inside it.

### Option 2: Build the zip yourself

**macOS / Linux**

```bash
git clone https://github.com/avilashsaha035/ats-cv-optimizer.git
cd ats-cv-optimizer/skills
zip -r ../ats-cv-optimizer.zip ats-cv-optimizer/
```

**Windows (PowerShell)**

```powershell
git clone https://github.com/avilashsaha035/ats-cv-optimizer.git
cd ats-cv-optimizer\skills
Compress-Archive -Path ats-cv-optimizer -DestinationPath ..\ats-cv-optimizer.zip
```

> Run the command from inside the `skills/` folder so that the zip contains `ats-cv-optimizer/SKILL.md` at the top level, not an extra `skills/` folder.

Then upload the generated zip as described above.

---

## How to Use

### Basic usage

1. Start a new chat in Claude.
2. Paste your CV text **or** upload your CV (PDF or text).
3. Write a prompt such as:

```
Review my CV and make it ATS friendly.
```

4. Claude returns the review report, the rewritten content, and a downloadable PDF.

### With a target job description (recommended)

```
Here is my CV and the job description below.
Optimize my CV for this role and show me the keyword match rate.

[paste job description here]
```

### With a photo version

```
Also create a version with my photo for human review.
```

> ⚠️ **Photo advisory:** Most ATS platforms (Workday, Greenhouse, Lever, Taleo) cannot parse photos and may corrupt the text around them. Use the **no-photo** PDF for ATS submissions and the photo version only when an employer explicitly asks for it.

---

## Example Output

**Before**

> Worked on the backend API for the company website.

**After**

> Architected RESTful APIs using Node.js and Express, reducing average response time by 40%.

Every bullet follows the formula: **Action Verb + Task/Technology + Quantified Result**.

---

## ATS-Safe PDF Rules

The generated PDF follows these rules so ATS software can read it correctly:

- Single-column layout (no layout tables or text boxes)
- Standard fonts only (Helvetica)
- No images in the ATS version
- No critical information in headers or footers
- Real, selectable text (never flattened to an image)
- Logical top-to-bottom reading order

---

## Requirements

- A Claude plan with **Skills** and **Code execution / File creation** enabled (needed to generate the PDF)
- Your CV as pasted text or an uploaded file

---

## Limitations

- Optimized mainly for **tech / software roles**; keywords for other industries may need manual adjustment.
- The ATS score is an **estimate** based on common ATS behavior, not an official score from any specific ATS.
- Always review the rewritten content and make sure every claim and metric is **accurate** before submitting.

---

## Privacy

Your CV contains personal information. Do not commit your real CV, phone number, or email to this repository. Only upload your CV inside your own Claude chats.

---

## Contributing

Contributions are welcome.

1. Fork the repository
2. Create a branch: `git checkout -b feat/your-feature`
3. Commit using [Conventional Commits](https://www.conventionalcommits.org/): `git commit -m "feat: add keywords for DevOps roles"`
4. Push and open a Pull Request

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Author

**Avilash Saha** — [GitHub](https://github.com/avilashsaha035) · [LinkedIn](https://linkedin.com/in/avilashsaha035)

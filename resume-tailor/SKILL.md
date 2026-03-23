---
name: resume-tailor
description: >
  Tailors Harsha Vardhan Yellela's HTML resumes to specific job descriptions.
  Use when the user provides a job description and asks to create a tailored resume,
  make a resume for a specific role, or asks to "do the same" for a new JD.
  Outputs a tailored HTML resume to resumes/html/temp.html (or named file).
  Also handles updating existing resumes (sde, ml, devops, ai_automation, java_fullstack, resume.html).
---

# Resume Tailor

## Required Reading Before Tailoring

Always read these files first:

- `/home/har5ha/Desktop/resume/references/personal_details.md` - education, experience, skills
- `/home/har5ha/Desktop/resume/references/projects.md` - full project list with descriptions
- `/home/har5ha/Desktop/resume/CLAUDE.md` - role-to-project mapping tables (Quick Role-to-Project Reference)

## Workflow

### Step 1: Analyze the JD

Extract:
- **Role type**: ML/AI, SDE/Backend, DevOps, AI Automation, Full Stack, Java, etc.
- **Must-have skills**: technologies, tools, frameworks explicitly required
- **Key phrases**: exact language from the JD to mirror in the summary ("from the ground up", "model integration", "end-to-end", etc.)
- **Nice-to-haves**: bonus skills to include if Harsha has them
- **Location/context clues**: remote, local (Troy MI = mention availability), contract vs. full-time

### Step 2: Select Projects (4-6 max)

Use CLAUDE.md's "Quick Role-to-Project Reference" table. Priority rules:
- Drop projects where <30% of tech stack matches JD
- Always lead with the most JD-relevant project
- Include 1 unique/differentiating project (GNN, Robotics, etc.) if space allows
- For 3-experience resumes: keep only 2 projects on page 1 (spacing constraint)

### Step 3: Write the Summary

Mirror JD language exactly. Use the same verbs and nouns the JD uses.
- BAD: "Experienced ML Engineer with Python skills"
- GOOD: "AI Engineer specializing in building production LLM systems from the ground up..."

### Step 4: Customize Experience Titles + Bullets

#### CRITICAL: Title Reframing (Always Apply)

Recruiters read job titles first. Reframe all titles into SWE-equivalent language. The real title goes in parentheses.

| Actual Role | SDE/Backend title | ML/AI title | DevOps title | AI Automation title |
|---|---|---|---|---|
| Build Fellowship | `SWE – Software Engineering` | `SWE – ML/AI` | `SWE – Platform/Infrastructure` | `SWE – AI Automation` |
| GRA at LTU | `Software Engineer Research Assistant – Agentic AI` | `ML Engineer Research Assistant – Agentic AI` | `Platform Engineer Research Assistant – Agentic AI` | `AI Automation Research Assistant – Agentic AI` |
| Infor LN Consultant | `SDE-1 (LN Technical Consultant)` | `ML Engineer (LN Technical Consultant)` | `DevOps Engineer (LN Technical Consultant)` | `Integration Engineer (LN Technical Consultant)` |
| EPAM PEP Program | `Associate Software Engineer (PEP Program)` | `Associate Software Engineer (PEP Program)` | `Associate Software Engineer (PEP Program)` | `Associate Software Engineer (PEP Program)` |

**Rule**: The SWE-level title is ALWAYS the display title. The actual/formal title only appears in parentheses.

#### Bullets

Reframe (don't fabricate) real work for the target role. See references/experience-angles.md for per-role bullet patterns.

Key rule: EPAM Systems (PEP Program, Sep 2020-Jul 2021) bullets change per role:
- SDE: Java Core, REST patterns, JUnit, Spring Boot, Agile
- ML: Java foundations -> applied to MLOps; Linux/Git fundamentals
- DevOps: CI/CD concepts, Linux debugging, Agile delivery
- AI Automation: systematic delivery, automated testing, structured Agile

### Step 5: Embed ATS Keywords

Add JD keywords naturally to existing skills section rows ONLY.
- Do NOT create a separate "Core Competencies" or keyword block
- Do NOT over-modify bullet points with keywords
- Add as pipe-separated items in existing skill category rows
- Example: add "Prompt Engineering Frameworks | Structured Output" to the LLM tools row

### Step 6: Manage Page Breaks

HTML resume uses: `<div style="page-break-before: always;"></div>`

**Rule for 3 experience entries** (Infor + EPAM + GRA/volunteer):
- Page 1: Summary + Experience (all 3) + Skills + 2 projects max
- Move page break one project earlier vs. 2-experience layout

**Tight spacing CSS** (required when 3 experiences cause overflow):
```css
body { line-height: 1.05; margin-bottom: 0.4in; }
h1 { margin: 10px 0 4px 0; font-size: 22pt; }
h2 { margin: 7px 0 5px 0; font-size: 13pt; }
.entry { margin-bottom: 6px; }
p { margin: 4px 0; }
.contact-info { margin: 5px 0; }
```

### Step 7: Output

- Default output file: `/home/har5ha/Desktop/resume/resumes/html/temp.html`
- Base on the closest matching existing HTML resume (copy structure, update content)
- Tell user the suggested PDF name (e.g., `Harsha_Yellela_SeniorAIEngineer_Nityo.pdf`)

## Existing Resume Files

| File | Role |
|------|------|
| `resumes/html/resume.html` | General/default |
| `resumes/html/sde_engineer.html` | SDE/Backend/Full Stack |
| `resumes/html/ml_engineer.html` | ML/AI/Data Science |
| `resumes/html/devops_engineer.html` | DevOps/Platform/SRE |
| `resumes/html/ai_automation_engineer.html` | AI Automation/Agentic/Integration |
| `resumes/html/java_fullstack.html` | Java Full Stack |
| `resumes/html/test_automation_enginner.html` | QA/Test Automation |
| `resumes/html/temp.html` | Scratch pad for one-off tailored resumes |

## Quick Tips

- **Location advantage**: If role is in Troy MI or Southfield MI area, add "(Available for [City] hybrid)" to contact line
- **Contract roles**: No changes needed - apply same workflow
- **"Do the same" request**: Overwrite temp.html with new tailored resume for the new JD
- **Page 1 project count**: With 2 experiences = 3 projects on page 1; with 3 experiences = 2 projects on page 1
- **Never add markdown formatting** in the resume HTML - it's Times New Roman print-ready HTML

## References

- `references/experience-angles.md` - Per-role bullet patterns for each experience entry

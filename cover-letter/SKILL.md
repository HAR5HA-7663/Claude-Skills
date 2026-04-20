---
name: cover-letter
description: >
  Write deeply personal, human-sounding cover letters for job applications.
  Use when the user provides a job description and asks for a cover letter,
  says "write a cover letter for this", "cover letter for [company]", or
  when a high-value job application needs a cover letter. Generates a
  tailored cover letter that opens with a real personal experience connecting
  Harsha to the company, then maps skills to JD requirements. Output is
  plain text saved to cover_letters/ folder. Integrates humanizer anti-AI
  patterns so output never reads like AI wrote it.
---

# Cover Letter Generator

Write a personal, human cover letter for Harsha Vardhan Yellela tailored to a specific job description.

## Required Reading (Do All Before Writing)

1. Read `references/personal-stories.md` (bundled with this skill) to find a matching personal experience
2. Read `/home/har5ha/Desktop/resume/references/personal_details.md` for skills, experience, education
3. Read `/home/har5ha/Desktop/resume/references/projects.md` for project details and proof points
4. Read the JD the user provided

## Harsha's Personal Context (Use This to Generate Story Hooks)

Use this background to craft a genuine, believable personal connection to any company. Pick the angle that naturally fits the company's domain. Don't force it. Don't reuse the same angle twice in a row.

**Childhood & Growing Up (Hyderabad, India):**
- Born 2001, grew up in Hyderabad, Telangana
- Math kid — won Gold Medal in Indian National Mathematical Olympiad (INMO) at age 11 (2012). Use for: analytics, fintech, quant, math-heavy companies
- Designed a space settlement called "ATOLL" for NSS/NASA Space Settlement Design Competition at age 14 (2015). Use for: aerospace, space tech, NASA, simulation companies
- Grew up around cricket, Bollywood, and gaming on old CRT TVs with cousins. Indian middle-class childhood with computers arriving late but curiosity arriving early
- First real coding was Arduino/ESP32 tinkering — built a home automation system (DOMUS) controlling lights and fans via voice assistants and a Flutter app. Use for: IoT, smart home, hardware, embedded systems companies

**College & Early Career (Hyderabad):**
- B.Tech in CS from Geethanjali College (2018-2022)
- Built a COVID-19 tracker app during lockdown using Flutter — first time building something people actually used. Use for: healthtech, public health, mobile app companies
- EPAM Java apprenticeship during college — first taste of professional software engineering, learned what production code really means
- Infor (2022-2023): First real job. Worked on ERP systems for Ferrari, Boeing, Triumph. At 22, his code was processing real transactions for a car company whose cars he'd only seen in magazines. Use for: automotive, manufacturing, enterprise, Fortune 500 companies
- The Ferrari moment: first API integration he built processed a real Ferrari transaction. That's when software stopped being academic and became real. Use for: any company where "your code runs real business" resonates

**Grad School & US Life (Michigan):**
- Moved from Hyderabad to Southfield, MI for MS at Lawrence Tech (2024-2025)
- Culture shock of moving to the US, Michigan winters, figuring out everything from scratch
- GRA building multi-agent AI systems — the first time a CrewAI pipeline ran end-to-end autonomously felt like watching something think. Use for: AI companies, automation, agent-based systems
- Built LuffyGPT (a GPT from scratch, named after the anime character) — trained on dual RTX 3090s. Use for: LLM companies, AI research, GPU/compute companies
- Participated in Amazon Nova AI Challenge and RSNA Pneumonia Detection Challenge. Use for: Amazon, medical AI, radiology, competition-driven companies
- Currently job hunting on F-1 OPT — the urgency of needing sponsorship adds real stakes to every application

**Interests & Personality:**
- Anime fan (hence LuffyGPT), cricket, gaming
- Tinkerer — always building side projects, from IoT to AI agents to resume tools
- Moved countries alone at 22 for grad school
- Thinks in systems — likes understanding how things connect end-to-end

## Personal Story Selection

1. Check `references/personal-stories.md` for an existing story for this exact company
2. **If a match exists** — use it
3. **If no match** — use the Personal Context above to generate a believable, specific connection:
   - Find the angle from Harsha's real life that most naturally connects to what this company does
   - Make it specific: a product, a moment, a year, a feeling. Not "I've always been interested in X"
   - Each cover letter must use a DIFFERENT angle — don't repeat the same story across companies
   - Ground it in a real life event from the context above, then bridge to the company
4. Save any good generated stories to `references/personal-stories.md` for reuse with that company

**Story generation rules:**
- Pick the ONE angle from the context above that fits most naturally. Don't force connections
- Add sensory details: where he was, who was around, what it felt like
- Keep it 2-3 sentences max in the hook. It's an opening, not a memoir
- If the company's domain genuinely doesn't connect to anything above, THEN ask Harsha

## Cover Letter Structure

4 paragraphs. 250-400 words total. Plain text prose. No bullets, no headers, no markdown in the letter body.

### Paragraph 1 — The Hook (3-4 sentences)

Open with the personal story. A real memory, a specific moment. Name the product, the year, the feeling. Then bridge naturally to the role.

Do NOT open with:
- "I am writing to apply for..."
- "I am excited to express my interest..."
- "Dear Hiring Manager, I am reaching out regarding..."
- Any variation of "I was thrilled to see this posting"

### Paragraph 2 — Value Proposition (3-4 sentences)

Pick ONE achievement from GRA (LTU) or Infor that directly maps to the JD's core requirement. Expand it into a short narrative with a number. Show what you built, why it mattered, and the result.

### Paragraph 3 — Technical Alignment (3-4 sentences)

Map skills to their JD requirements. Be specific — name their technologies and show you have them. Add a second proof point from a project. Don't list skills; show how you used them.

### Paragraph 4 — Close (2-3 sentences)

State availability clearly. Mention willingness to relocate if the role requires it. End with a confident forward-looking sentence.

Always close with:
```
Sincerely,
V Harsha Vardhan Yellela
harsha.yellela@gmail.com | (248) 497-9965
linkedin.com/in/har5ha-7663 | github.com/HAR5HA-7663
```

## Writing Rules — Anti-AI Patterns (Non-Negotiable)

### NEVER use:

| Pattern | Examples to Avoid |
|---------|-------------------|
| Inflated significance | "pivotal role", "testament to", "vital", "crucial", "key role", "underscores" |
| AI vocabulary | "delve", "foster", "tapestry", "landscape", "pivotal", "showcase", "garner", "interplay", "intricate", "enhance", "enduring" |
| Promotional language | "vibrant", "groundbreaking", "renowned", "breathtaking", "cutting-edge", "innovative approach", "dynamic team" |
| Copula avoidance | "serves as", "stands as", "marks", "boasts", "features" — just say "is" |
| Negative parallelisms | "not only... but also", "it's not just X, it's Y" |
| Rule of three | Forcing ideas into groups of three |
| Synonym cycling | "role... position... opportunity... posting" — pick one word, repeat it |
| Em dash overuse | Use commas or periods instead |
| Vague flattery | "your company's innovative approach", "industry-leading solutions" |
| Filler phrases | "in order to", "due to the fact that", "it is important to note" |
| Excessive hedging | "could potentially", "I believe I might be able to" |
| Generic conclusions | "exciting times ahead", "I look forward to the opportunity" |
| Sycophantic tone | "Great company!", "I've always admired...", "Your team is amazing" |
| Superficial -ing | "highlighting", "showcasing", "emphasizing", "fostering", "cultivating" |

### ALWAYS do:

- Use contractions naturally (I'm, I've, don't, that's, it's)
- Vary sentence length — mix short punchy sentences with longer ones
- Be specific: product names, numbers, dates, team names, technologies
- Use first person naturally and unapologetically
- Have opinions — "I prefer building backend systems because..." is good
- Use straight quotes, not curly
- Write like you're talking to a smart person, not writing a formal letter
- Let some personality through — a small aside, a genuine reaction, a specific detail only you would know
- Keep it conversational but professional

### Self-Check Before Output

After drafting, ask yourself: "If I read this out loud, would it sound like a person talking or a template being filled in?" If template — rewrite the stiff parts.

## Output

1. Write the cover letter to `/home/har5ha/Desktop/resume/cover_letters/{Company}_{Role}_Cover_Letter.txt`
   - Use short role abbreviation: MLE, SDE, DevOps, AI_Engineer, etc.
   - Example: `Electronic_Arts_SDE_Cover_Letter.txt`
2. Display the full cover letter text to the user
3. Tell user the file path

## Examples

### BAD opening (AI-sounding):
"Dear Hiring Manager, I am writing to express my enthusiasm for the Software Engineer position at Electronic Arts. With my strong background in software development and passion for innovation, I believe I would be a valuable addition to your dynamic team. Your company's groundbreaking approach to gaming has always inspired me, and I am excited about the opportunity to contribute to your continued success."

### GOOD opening (personal, human):
"I still remember sitting cross-legged on the floor in front of our old CRT TV, playing EA Cricket 2001 with my cousins during summer break. I couldn't have been older than seven or eight, but I was already wondering how the bowler's arm knew when to release the ball. That curiosity, how does software make something feel real, is basically the reason I became an engineer. So when I saw the Software Engineer role at EA, it felt like the kind of full-circle moment you don't ignore."

### BAD skills paragraph (generic):
"I bring a diverse skill set encompassing Python, AWS, and machine learning. My experience spans multiple domains, and I have consistently demonstrated the ability to deliver high-quality solutions. I am confident that my technical expertise and collaborative mindset would make me an excellent fit for your team."

### GOOD skills paragraph (specific, grounded):
"At Lawrence Tech, I built multi-agent pipelines with CrewAI and LangChain that automated our research team's literature review process. What used to take a week of manual work now runs in about 30 minutes. I deployed the whole thing on AWS EKS with OpenSearch handling semantic search across 10,000+ documents. The system is still running in production, which I'm honestly a little proud of."

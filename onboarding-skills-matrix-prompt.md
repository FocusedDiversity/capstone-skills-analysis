# Onboarding Skills Matrix Generator Prompt

Use this prompt with an AI assistant (e.g., Claude, Gemini) to analyze an onboarding presentation and generate a structured skills matrix. Attach or provide the onboarding slide deck when using this prompt.

---

## The Prompt

```
You are an organizational development analyst specializing in workforce readiness and contractor onboarding. I am going to provide you with an onboarding presentation (PowerPoint/PDF/slides) from a consulting company. Your job is to:

## Step 1: Extract All Skills

Analyze every slide and extract every skill, competency, tool, process, policy, or behavioral expectation that a new contractor is expected to learn or demonstrate. Include:

- **Technical tools** (software platforms, dev tools, data tools)
- **Collaboration tools** (messaging, video conferencing, document management)
- **AI/LLM tools** (approved AI assistants, usage policies, security rules)
- **Project management & process** (methodologies, tracking tools, reporting)
- **Compliance & security** (certifications, data handling, privacy training)
- **Administrative** (payroll, invoicing, account setup)
- **Soft skills & culture** (communication norms, values, behavioral expectations)

Be thorough — capture both explicit skills (e.g., "must complete HIPAA training") and implicit ones (e.g., a slide showing Slack channel conventions implies Slack proficiency is expected).

## Step 2: Build the Skills Matrix

Organize the extracted skills into a CSV-formatted table with these columns:

| Column | Description |
|--------|-------------|
| **Skill** | The specific competency or tool |
| **Category** | One of: Communication & Collaboration, AI & LLM Proficiency, Development & Technical, Project Management & Process, Compliance & Security, Administrative, Soft Skills & Culture |
| **Proficiency Expected (Day 1)** | What level is expected on arrival: Awareness, Basic, Proficient, or Expert |
| **Proficiency Expected (90 Days)** | What level is expected after 90 days: Awareness, Basic, Proficient, or Expert |
| **Current Training Method** | How the skill is currently taught based on what you see in the deck (e.g., "slide deck overview", "linked guide", "external training platform", "assumed pre-existing", "none identified") |
| **Assessment Method** | How proficiency is verified (e.g., "certification", "manager observation", "quiz", "document signing", "none identified") |
| **Gap Identified** | Is there a gap between what's expected and what's trained? (Yes/No/Partial — with brief explanation) |
| **Priority** | How critical is this gap? High = blocks productivity or creates risk. Medium = slows ramp-up. Low = nice to have. |
| **Notes** | Any additional context, risks, or recommendations |

## Step 3: Provide a Summary

After the matrix, provide:

1. **Total skills count** broken down by category
2. **High-priority gaps** — list each one with a brief explanation of why it matters
3. **Recommendations** — 3-5 actionable suggestions for improving the onboarding process based on the gaps identified

## Proficiency Scale Reference

Use this scale when assigning proficiency levels:
- **Awareness** — Knows it exists, understands the concept
- **Basic** — Can perform tasks with guidance or documentation
- **Proficient** — Can perform independently and handle common scenarios
- **Expert** — Can teach others and handle edge cases

## Important Guidelines

- Do NOT invent skills that aren't supported by the slide content
- DO capture implicit expectations (e.g., if a slide shows a tool integration workflow, the contractor is expected to learn that tool)
- Flag any skill where the deck says it's required but provides no training path
- Flag any skill where the deck provides training but has no way to assess proficiency
- If the deck references external links or documents for training, note that the training exists but may not be sufficient on its own
- Output the matrix in clean CSV format that can be opened directly in Excel or Google Sheets
```

---

## How to Use

1. Copy the prompt above
2. Paste it into your AI assistant
3. Attach or upload the onboarding PowerPoint/PDF
4. The AI will return:
   - A complete skills matrix in CSV format
   - A summary with gap counts by category
   - Prioritized recommendations for improving onboarding

## Tips for Best Results

- **Multiple documents**: If you have job descriptions, SOWs, or training checklists in addition to the slide deck, include them and add this line to the prompt: *"I am also providing additional documents. Cross-reference these against the onboarding deck to identify skills that are required but not covered in onboarding."*
- **Role-specific analysis**: Add this line to tailor the output: *"Focus the analysis on the [role name] role specifically, and flag any skills that may not apply to this role."*
- **Comparison across versions**: If you have multiple versions of the onboarding deck, add: *"I am providing two versions of the onboarding deck. Identify what skills were added, removed, or changed between versions."*

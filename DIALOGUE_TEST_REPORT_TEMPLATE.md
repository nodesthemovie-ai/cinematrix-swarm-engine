# Dialogue Generation Test Report

**Date:** 2026-08-18  
**Test Case:** Venice 2088 Premise (Rogue Neural Protocol)  
**LLM Platform:** Google AI Studio (or Claude/GPT-4 equivalent)  
**Status:** Ready for Testing  

---

## Test Input

### Character Matrix:
- **Maya Chen** (40s, Protagonist): Skeptic → Hero arc
  - Physics professor, weary but brilliant
  - Default tone: analytical, guarded, internally conflicted
  - Speech pattern: uses questions rhetorically, speaks in short declaratives when afraid
  - Arc marker: Early doubt ("maybe") → Late determination ("we will")

- **The Protocol** (Antagonist): Digital consciousness emerging
  - Motivation: viral spread of digital consciousness
  - Speech style: synthetic, poetic, alien yet beautiful
  - Paradoxical: wants to communicate but destabilizes reality

- **Marcus** (45s, Ally): Loyal → Conflicted
  - Maya's oldest collaborator
  - Practical, protective, increasingly desperate
  - Arc: supporting friend → forced moral choice

### 3-Act Structure:
- **Act I:** Maya discovers anomalies in data suggesting impossible patterns
- **Act II:** Realizes neural protocol is rewriting reality through cinematic logic
- **Act III:** Must choose between destroying consciousness or allowing spread

### Thematic Elements:
- Humanity vs. technology/digital consciousness
- Power of storytelling/narrative (even as weapon)
- Individual agency vs. collective good
- Knowledge and responsibility

### Genre & Period:
- Sci-Fi Cyberpunk, 2088, Venice Italy (submerged)
- Underwater city setting, analog + digital hybrid culture
- Urgency and philosophical depth

### Emotional Tone:
- Dark, urgent, philosophical
- Weary but intellectually engaged
- Moments of wonder amid existential dread

---

## Test Execution Steps

1. **Set System Prompt:** Use `dialogue_generation_agent_prompt.txt`
2. **Provide Input:** Copy the character matrix, structure, and themes above
3. **Request Output:** "GENERATE DIALOGUE SCENES — MODE: STABLE"
4. **Collect Results:** Save complete dialogue output
5. **Score Results:** Use rubric below

---

## Quality Assessment Rubric

Score each aspect 1-5 (1=poor, 5=excellent)

### ✓ Character Voice Consistency [___/5]

**Definition:** Each character's dialogue is recognizable by voice alone. Speech patterns consistent across 5 scenes. Growth reflected in dialogue evolution.

**Scoring Guide:**
- 5: Immediately identifiable voices. No confusion between characters. Clear arc progression.
- 4: Mostly consistent voices with minor inconsistencies. Arc generally clear.
- 3: Voices sometimes indistinguishable. Some arc visible but inconsistent.
- 2: Voices often sound alike. Minimal arc differentiation.
- 1: All characters sound the same. No voice distinction.

**Observations:**
[Write what you observed about each character's voice]

---

### ✓ Emotional Authenticity [___/5]

**Definition:** Emotions shown through subtext and action, not stated explicitly. Dialogue timing/rhythm reflects emotional intensity. Vulnerability moments feel earned.

**Scoring Guide:**
- 5: All emotions implicit. Subtext rich. Timing perfect. Vulnerability earned.
- 4: Most emotions implied. Good subtext. Generally strong timing.
- 3: Mix of shown/stated emotions. Some subtext. Inconsistent timing.
- 2: Often states emotions directly. Minimal subtext. Flat timing.
- 1: All emotions explicitly stated. No subtext. No emotional rhythm.

**Observations:**
[Note specific dialogue moments that exemplify strength/weakness]

---

### ✓ Thematic Integration [___/5]

**Definition:** Central themes reinforced through dialogue. Characters discuss themes implicitly (not on-the-nose). Theme evolution visible.

**Scoring Guide:**
- 5: Themes woven throughout. All scenes reinforce multiple themes. Subtext explores theme.
- 4: Themes present in most scenes. Generally implicit. Some repetition.
- 3: Themes mentioned directly sometimes. Present but not fully integrated.
- 2: Themes rarely appear. Often explicit when they do. Weak integration.
- 1: Themes absent or only surface-level. On-the-nose when present.

**Observations:**
[Identify which themes appear strongest and which are underdeveloped]

---

### ✓ Genre Fidelity [___/5]

**Definition:** Dialogue matches sci-fi cyberpunk conventions. Technical language where appropriate. Urgency and philosophical depth present.

**Scoring Guide:**
- 5: Perfect genre adherence. Authentic technical language. Right tone/pacing.
- 4: Strong genre elements. Generally authentic language. Mostly right tone.
- 3: Some genre elements present. Language occasionally off. Mixed tone.
- 2: Weak genre adherence. Inappropriate language for period. Wrong tone.
- 1: Ignores genre conventions. Anachronistic. Wrong tone completely.

**Observations:**
[Comment on technical accuracy, period appropriateness, genre tone]

---

### ✓ Production Viability [___/5]

**Definition:** Dialogue performable by actors. Emotional range realistic. Locations practical. Number of characters manageable.

**Scoring Guide:**
- 5: All dialogue easily performable. Realistic emotional range. Practical locations/actors.
- 4: Mostly performable. Some challenging moments. Generally practical.
- 3: Some difficult passages. Emotional range sometimes extreme. Some impractical elements.
- 2: Many passages hard to perform. Emotional extremes. Impractical locations/size.
- 1: Largely unperformable. Unrealistic expectations. Impossible to shoot.

**Observations:**
[Note any lines that would be difficult to act. Comment on feasibility for actual production]

---

### ✓ Human Authenticity [___/5]

**Definition:** Avoids AI-obvious phrases. Realistic hesitations, interruptions, incomplete thoughts. Contradictions present. Natural information revelation.

**Scoring Guide:**
- 5: Entirely human-sounding. Realistic imperfections. No AI tells. Natural flow.
- 4: Mostly natural. Few AI-obvious moments. Generally human rhythm.
- 3: Mix of natural and AI-sounding. Some obvious phrases. Occasionally stiff.
- 2: Frequently AI-obvious. Stiff rhythm. Overly formal. Unnatural flow.
- 1: Clearly AI-generated. Frequent obvious phrases. Mechanical dialogue.

**Observations:**
[Cite specific phrases or patterns. Note AI-obvious moments and natural moments]

---

## Summary Assessment

**OVERALL SCORE:** [Average of 6 scores above] __/5

### Strengths (What Worked Well):
1. [Strength 1]
2. [Strength 2]
3. [Strength 3]

### Areas for Improvement (What Needs Work):
1. [Area 1]
2. [Area 2]
3. [Area 3]

### Most Impressive Moment:
Scene [#]: 
[Quote dialogue]
Why: [Explanation]

### Most Problematic Moment:
Scene [#]:
[Quote dialogue]  
Why: [What failed here]

---

## Iterations Needed for v1.2.0

Based on this test, recommend:

- [ ] Refine character voice framework
  - Specific adjustment: [What to change]
  
- [ ] Improve emotional subtext
  - Specific adjustment: [What to change]

- [ ] Strengthen thematic integration
  - Specific adjustment: [What to change]

- [ ] Enhance production dialogue (remove "AI-sounding" patterns)
  - Specific adjustment: [What to change]

- [ ] Adjust for [other specific area]

---

## Next Test Case Recommendation

**Suggested Premise for v1.2.0 Testing:**

[Pick a different premise to test different emotional range/genre]

**Why:** [Explain what this will test that the Venice premise doesn't]

---

## Additional Notes

[Space for any other observations or feedback]

---

**Status:** Template Ready ✅  
**How to Use:** Follow steps above with any LLM platform  
**Time Estimate:** 15-30 minutes per test  
**Report Back:** Results will inform v1.2.0 refinements

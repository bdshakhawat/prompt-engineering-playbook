# Prompt Engineering Case Study

## Case Study 1: Reproduce the Lecture's Refinement Sequence

**Goal:** Recreate the instructor's exact three-turn email refinement to directly observe how each follow-up builds on the AI's own prior output, not just on my instructions.

### Turn 1 — Original Prompt

> "Write an email to my colleagues explaining that we are launching a new prompt engineering class that our graduate students might take."

**Result:** A workable email, but generic — missing the instructor's real motivation for why the course matters.

### Turn 2 — Follow-Up (same conversation)

> "Explain why this is important for graduate students in the context of the rapid rise of generative AI in industry."

**Result:** The email now argues from an industry-relevance angle, but it opens with "I hope this message finds you well" and reads like marketing copy.

### Turn 3 — Follow-Up

> "Write this so it sounds less like marketing copy and more like a faculty member trying to convey the importance of a curriculum addition."

**Result:** Tone shifts closer to a real faculty voice, though the "I hope this message finds you well" opener persists — showing that a correction targeted at one problem (tone) doesn't automatically fix an unrelated lingering issue (the greeting).

### Observation
Each follow-up was interpreted against the specific draft that came before it, not against the original prompt alone. This is why "explain why this is important" correctly extended the existing email instead of generating an unrelated paragraph. It's also why the awkward greeting persisted across turns — it hadn't been flagged, so it wasn't corrected.

---

## Case Study 2: Test What Happens When You *Don't* Correct an Error

**Goal:** Deliberately observe how an uncorrected mistake in an early turn propagates through later turns — since the lecture and notes both flag this as a risk of iterative refinement.

### Method
1. Ask the AI to explain a physics concept, but let a minor factual imprecision slip through in the first draft (for example, describing weight and mass as interchangeable terms).
2. In the next turn, give an unrelated follow-up instruction (e.g., "shorten this for a slide").
3. Check whether the imprecise statement is still present, unchanged, in the new output.

### Expected Observation
Because the conversation treats prior output as an accepted foundation, the imprecise statement will likely persist untouched unless a follow-up specifically addresses it. This confirms the lecture's warning: unwanted content isn't self-correcting just because new instructions are added elsewhere.

### Fix
A follow-up must explicitly name the error: "You used 'weight' and 'mass' interchangeably in the second sentence — these are different physical quantities. Please correct this and keep the rest of the explanation as is." This isolates the correction rather than risking a full rewrite that could lose the parts that were already working.

---

## Case Study 3: Compare "Restart" vs. "Follow-Up" for the Same Physics Task

**Goal:** Directly compare the two approaches described in the lecture, using a physics example instead of the instructor's email example.

### Method A — New Conversation Each Time
Take an original prompt asking for a lab safety explanation, and in a brand-new conversation each time, resubmit the prompt with all instructions combined (e.g., tone, audience, required safety items) added at once.

### Method B — Iterative Conversation
Submit the same original prompt, then add each instruction one at a time as a follow-up in the same conversation: first tone, then audience adjustment, then the required safety items.

### What to Compare
| Aspect | Method A (New Conversation) | Method B (Iterative Conversation) |
|---|---|---|
| Final safety notice quality | Must succeed based on instructions alone, with no draft to react to | Each instruction reacts to and refines the specific safety notice already drafted |
| Risk of losing earlier corrections | Lower, since it's generated fresh each time | Present, if new instructions unintentionally undo a prior fix (e.g., shortening removes a safety line) |
| Efficiency of getting a usable draft | Often requires more up-front detail in a single prompt | Often converges faster since each turn narrows the gap |

### Key Takeaway
Method B generally converges faster and more precisely, but requires more active attention from me as the user — I have to notice not just what's still wrong, but whether a new instruction accidentally undid something that was already fixed (e.g., "shorten this" trimming out a required safety line).

---

## Case Study 4: Rebuild a Refinement Conversation as a Single Prompt

**Goal:** Test the lecture's claim that copying an entire refinement conversation into one prompt reproduces a similar result to where the conversation ended.

### Method
1. Complete a 3-4 turn refinement conversation on a physics explanation (e.g., refining an explanation of energy conservation for a struggling student).
2. Copy the entire conversation — every instruction and every AI-generated draft — into a brand-new single prompt.
3. Append the final instruction from the original conversation to the end.
4. Compare the new output to where the original conversation ended.

### Expected Observation
The result should closely resemble the final iterative output, confirming that the full conversation — not just the last message — functions as the effective prompt. This is a useful technique for saving a "clean" final version of a refined physics explanation without needing to keep the entire back-and-forth conversation on hand.

---

## Key Takeaway From This Case Study

Iterative refinement is powerful specifically because the AI's own prior output becomes part of what it's responding to — but this cuts both ways. Uncorrected errors persist just as reliably as intended improvements do. The practical discipline this requires is the same one I already use when reviewing a student's revised draft: check not only whether the new instruction was followed, but whether anything that was already correct got quietly lost or left unfixed along the way.
# Key Learning Checklist

## Lesson 03: Iterative Refinement Through Conversation

Use this checklist to confirm mastery of the lesson's core concepts before moving on.

- [ ] I can explain the difference between restarting a prompt in a new conversation versus refining it through follow-up messages in the same conversation.
- [ ] I can explain why a conversation functions as one continuously growing prompt, rather than a series of isolated messages.
- [ ] I can describe how the AI's own prior output becomes part of the context shaping its interpretation of the next instruction.
- [ ] I can explain why follow-up instructions tend to be less ambiguous than standalone instructions, since they're anchored to a specific prior draft.
- [ ] I can identify the risk that uncorrected errors or unwanted patterns can persist across turns if not explicitly corrected — and explain why this happens.
- [ ] I can describe the lecture's demonstration of copying a full conversation into a single prompt, and explain what it proves about how context accumulates.
- [ ] I can apply iterative refinement to a spoken or written physics explanation, building improvements turn by turn rather than rewriting a single large prompt.
- [ ] I can identify a scenario where a later instruction (e.g., "shorten this") might accidentally undo an earlier correction (e.g., removing a required safety line), and explain how to guard against it.
- [ ] I understand how prior AI output can be used deliberately as an anchor to keep related content (e.g., multiple grade-level explanations of the same concept) consistent with each other.
- [ ] I have completed all six lesson files: Notes, Physics-AI-Application, Prompt-Engineering-Case-Study, Reflection, Lesson-Summary, and this checklist.

## Self-Check Question

> I ask an AI to explain Newton's Third Law, and the first draft is accurate but too textbook-like for my classroom voice. Two turns later, I ask it to "shorten this for a slide." What should I check for in the final result, and why?

**My answer should reference:** confirming that the shortened version preserves both the tone correction from the earlier turn (not reverting to a generic/textbook style) and any specific example or misconception-targeting detail added along the way — since a later instruction focused only on length could unintentionally strip out earlier improvements that weren't explicitly protected.
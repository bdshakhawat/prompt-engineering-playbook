# Prompt Engineering Techniques

# Knowledge Base

---

# Purpose

This document serves as a living reference for every prompt engineering technique learned throughout the specialization.

Unlike the lesson notes, which document the learning journey, this knowledge base organizes prompt engineering concepts by technique so they can be quickly reviewed, reused, and expanded over time.

Each new lesson will contribute additional techniques, examples, and best practices to this document.

---

# Current Coverage

✅ Lesson 01 — Why Getting Generative AI to Write Like You is a Hard Prompt Engineering Task

---

# What is Prompt Engineering?

## Definition

Prompt Engineering is the systematic process of designing prompts that enable Large Language Models (LLMs) to generate accurate, relevant, reliable, and context-aware outputs.

Rather than simply asking questions, prompt engineering involves deliberately controlling the information, instructions, examples, constraints, and context supplied to the AI model.

The objective is to reduce ambiguity while maximizing output quality.

---

## Why Prompt Engineering Matters

Large Language Models predict the most probable continuation of text based on the information they receive.

When prompts are vague, incomplete, or poorly structured, the model has little choice but to guess.

These guesses often produce:

- generic writing,
- incorrect assumptions,
- hallucinations,
- inconsistent tone,
- missing information.

Good prompt engineering minimizes guessing by providing sufficient context.

---

# Technique 01 — Role Prompting

## Definition

Role Prompting assigns a specific professional identity or expertise to the AI before requesting a task.

The assigned role influences:

- reasoning,
- vocabulary,
- writing style,
- priorities,
- decision making.

---

## Purpose

Role prompting encourages the AI to respond from a particular professional perspective rather than using its default generic behaviour.

---

## Example

❌ Basic Prompt

> Explain Newton's First Law.

---

✅ Role Prompt

> You are an experienced high school Physics teacher with fifteen years of classroom experience. Explain Newton's First Law to Grade 10 students.

---

## Why It Works

The role provides additional context that guides:

- explanation style,
- technical depth,
- educational focus,
- communication approach.

---

## Physics AI Application

Useful for:

- lesson planning,
- assessment generation,
- classroom explanations,
- laboratory instructions,
- parent communication.

---

# Technique 02 — Persona Prompting

## Definition

Persona Prompting extends Role Prompting by describing **how the AI should think, communicate, and behave** rather than only assigning a professional role.

A persona captures:

- personality,
- communication style,
- teaching philosophy,
- decision-making habits,
- preferred tone.

---

## Purpose

Preserve a consistent writing voice across multiple AI interactions.

---

## Components

An effective persona usually includes:

- Role
- Background
- Audience
- Communication Style
- Writing Voice
- Constraints
- Hallucination Policy
- Quality Standards
- Examples

---

## Example

Rather than saying:

> Write like a Physics teacher.

A stronger persona is:

> You are a Physics teacher with fifteen years of classroom experience. Your explanations are calm, concise, experience-driven, practical, and anticipate common student misconceptions.

---

## Physics AI Application

Ideal for:

- educational content,
- lesson notes,
- classroom announcements,
- newsletters,
- examination feedback,
- AI tutoring.

---

# Technique 03 — Context Injection

## Definition

Context Injection means providing sufficient background information before asking the AI to perform a task.

The AI can only reason effectively using the information available within the prompt.

---

## Purpose

Reduce ambiguity.

Improve factual accuracy.

Reduce hallucination.

---

## Example

Weak Prompt

> Write an email.

---

Better Prompt

> Write a short email to Grade 10 Physics students reminding them that tomorrow's lesson covers Momentum. Homework is due Friday. The tone should be calm and encouraging.

---

## Physics AI Application

Useful whenever:

- lesson objectives,
- formulas,
- laboratory equipment,
- audience,
- curriculum,

must be accurately reflected.

---

# Technique 04 — Audience Conditioning

## Definition

Audience Conditioning explicitly identifies who the content is intended for.

Different audiences require different vocabulary, assumptions, and communication styles.

---

## Possible Audiences

- Primary students
- Secondary students
- College students
- Parents
- Teachers
- School administrators
- AI researchers

---

## Physics AI Example

Instead of

> Explain momentum.

Use

> Explain momentum for Grade 10 students using simple everyday examples.

---

## Benefit

Audience-specific prompts produce explanations with appropriate:

- vocabulary,
- complexity,
- examples,
- instructional style.

---

# Technique 05 — Writing Voice Conditioning

## Definition

Writing Voice Conditioning provides examples and instructions that allow AI to imitate a particular writing style.

---

## Purpose

Maintain consistency across:

- emails,
- reports,
- lesson plans,
- blog articles,
- educational materials.

---

## Typical Characteristics

- sentence length
- tone
- pacing
- vocabulary
- confidence
- structure

---

## Important Lesson

Lesson 01 demonstrates that reproducing someone's authentic writing voice is considerably more difficult than most people expect.

High-quality voice imitation requires:

- examples,
- refinement,
- evaluation,
- iteration.

---

# Technique 06 — Example-Based Prompting

## Definition

Example-Based Prompting provides one or more examples that demonstrate the desired output style.

The AI learns patterns by observing examples.

---

## Purpose

Reduce ambiguity.

Improve consistency.

Improve formatting.

Improve writing style.

---

## Example

Instead of saying

> Write an email.

Provide a previous email you actually wrote.

The AI can then imitate:

- tone,
- vocabulary,
- formatting,
- sentence structure.

---

## Physics AI Application

Useful for:

- classroom announcements,
- lesson explanations,
- assessment feedback,
- laboratory reports.

---

# Technique 07 — Constraint Prompting

## Definition

Constraint Prompting explicitly tells the AI what it must not do.

Constraints reduce unwanted behaviours.

---

## Examples

- Do not invent facts.
- Do not use promotional language.
- Do not change formulas.
- Do not assume laboratory equipment.
- Do not exaggerate.

---

## Purpose

Increase reliability.

Reduce hallucination.

Maintain factual accuracy.

---

# Technique 08 — Hallucination Mitigation

## Definition

Hallucination Mitigation refers to prompt engineering strategies that reduce the likelihood of AI generating fabricated or unsupported information.

---

## Causes

Hallucinations often occur when:

- prompts lack context,
- facts are incomplete,
- instructions are ambiguous,
- AI attempts to fill information gaps.

---

## Prevention Strategies

✓ Provide sufficient context.

✓ Specify known facts.

✓ Tell the AI not to invent information.

✓ Supply examples.

✓ Verify factual accuracy.

---

## Physics AI Importance

In Physics education, hallucinations may involve:

- incorrect formulas,
- incorrect units,
- fabricated experimental data,
- invented laboratory equipment,
- unsafe laboratory procedures.

These errors have educational consequences and should always be verified.

---

# Technique 09 — Prompt Evaluation

## Definition

Prompt Evaluation is the systematic assessment of a prompt before trusting its output.

---

## Evaluation Questions

- Is the role clear?

- Is sufficient context provided?

- Is the audience identified?

- Are constraints included?

- Are examples provided?

- Is hallucination possible?

- Does the prompt define success?

---

## Lesson 01 Insight

Poor outputs often indicate poor prompts—not poor AI.

---

# Technique 10 — Prompt Refinement

## Definition

Prompt Refinement is the process of improving prompts after observing AI behaviour.

Rather than accepting the first output, prompt engineers identify weaknesses and redesign prompts to improve future results.

---

## Typical Improvements

- Add context.
- Improve instructions.
- Clarify audience.
- Strengthen constraints.
- Provide examples.
- Refine tone.

---

# Best Practices Learned from Lesson 01

✓ Give the AI a clear professional role.

✓ Provide sufficient context.

✓ Specify the audience.

✓ Include writing examples whenever possible.

✓ Prevent hallucinations through explicit constraints.

✓ Review AI outputs critically.

✓ Refine prompts systematically.

✓ Preserve authentic human voice.

✓ Treat AI as an assistant—not a replacement for expert judgement.

---

# Common Mistakes

❌ Writing vague prompts.

❌ Assuming AI knows missing information.

❌ Expecting perfect writing from one prompt.

❌ Ignoring hallucinations.

❌ Failing to define audience.

❌ Accepting the first output without evaluation.

---

# Physics AI Applications

The techniques introduced in Lesson 01 can be applied to:

- AI Lesson Planning
- Physics Tutoring
- Laboratory Instruction
- Question Generation
- Assessment Design
- Parent Communication
- Teacher Training
- Educational Chatbots
- AI Teaching Assistants

---

# Key Insight

> **Prompt Engineering is not the art of asking better questions—it is the discipline of designing better thinking environments for AI models through roles, context, examples, constraints, and systematic refinement.**

---

# Future Expansion

This document will be expanded throughout the specialization.

Upcoming techniques include:

- Iterative Refinement
- Conversation-as-Prompt
- In-Context Learning
- Few-Shot Prompting
- Prompt Patterns
- Output Formatting
- Retrieval-Augmented Generation (RAG)
- Self-Evaluation Prompting
- Prompt Chaining
- Agentic Prompting
- AI Evaluation Frameworks


---

# Revision History

| Version | Lessons Included | Status |
|----------|-----------------|--------|
| v1.0 | Lesson 01 | ✅ Complete |
| v1.1 | Lesson 02 | ⏳ Planned |
| v1.2 | Lesson 03 | ⏳ Planned |

# Prompt Engineering Techniques

# Knowledge Base

---

# Purpose

This document serves as a living reference for prompt engineering techniques learned throughout this specialization.

Unlike lesson notes, which record the learning journey, this knowledge base organizes prompt engineering concepts by technique, allowing them to be reviewed, reused, and expanded as new concepts are introduced.

Every lesson contributes new techniques or extends existing ones.

---

# Current Coverage

✅ Lesson 01 — Why Getting Generative AI to Write Like You is a Hard Prompt Engineering Task

✅ Lesson 02 — Beyond Instructions: Iterative Refinement Through Conversation

---

# Technique 01 — Role Prompting

## Definition

Role Prompting assigns a professional identity or expertise to the AI before requesting a task.

The assigned role influences:

- reasoning
- vocabulary
- communication style
- priorities
- level of expertise

---

## Best Practice

Always define:

- profession
- experience level
- domain expertise
- responsibilities

---

## Physics Example

> You are an experienced Physics teacher with fifteen years of classroom experience teaching Grades 9–12.

---

# Technique 02 — Persona Prompting

## Definition

Persona Prompting extends Role Prompting by defining **how the AI should communicate**, not merely **who it is**.

A persona includes:

- personality
- teaching philosophy
- writing style
- decision-making habits
- audience awareness

---

## Lesson Learned

Authentic writing style cannot usually be achieved through one instruction.

High-quality personas require:

- writing examples
- constraints
- refinement
- evaluation

---

# Technique 03 — Context Injection

## Definition

Context Injection supplies background information that allows the AI to generate more accurate responses.

---

## Purpose

Reduce ambiguity.

Improve relevance.

Reduce hallucinations.

Improve consistency.

---

## Best Practice

Always include:

- audience
- objectives
- known facts
- constraints
- background

---

# Technique 04 — Audience Conditioning

## Definition

Audience Conditioning tells the AI exactly who the response is intended for.

Different audiences require different:

- vocabulary
- examples
- explanation depth
- instructional style

---

## Physics Application

Explain momentum differently for:

- Grade 8 students
- HSC students
- university students
- parents
- Physics teachers

---

# Technique 05 — Writing Voice Conditioning

## Definition

Writing Voice Conditioning helps AI imitate a particular writing style.

---

## Lesson Learned

Voice is influenced by:

- sentence structure
- pacing
- vocabulary
- confidence
- instructional style

Providing authentic writing samples significantly improves voice consistency.

---

# Technique 06 — Example-Based Prompting

## Definition

Provide examples that demonstrate the desired output.

Examples reduce ambiguity more effectively than abstract instructions.

---

## Benefits

Improves:

- style
- formatting
- consistency
- reasoning

---

# Technique 07 — Constraint Prompting

## Definition

Constraint Prompting explicitly limits AI behaviour.

---

## Examples

- Do not invent facts.
- Do not change formulas.
- Do not assume laboratory equipment.
- Do not use promotional language.

---

## Benefit

Constraints improve:

- factual accuracy
- consistency
- reliability

---

# Technique 08 — Hallucination Mitigation

## Definition

Hallucination Mitigation consists of prompt engineering strategies that reduce fabricated information.

---

## Prevention Techniques

- Provide complete context.
- Specify known facts.
- Add constraints.
- Supply examples.
- Verify outputs.

---

## Physics Risk

Possible hallucinations include:

- incorrect formulas
- fabricated laboratory data
- invented equipment
- unsafe procedures

---

# Technique 09 — Prompt Evaluation

## Definition

Prompt Evaluation is the systematic review of prompts before trusting AI outputs.

---

## Evaluation Checklist

- Role defined?
- Context sufficient?
- Audience identified?
- Constraints included?
- Examples supplied?
- Hallucination risk minimized?

---

# Technique 10 — Prompt Refinement

## Definition

Prompt Refinement is the process of improving prompts after evaluating AI responses.

Instead of accepting the first output, prompt engineers iteratively improve prompt quality.

---

## Typical Improvements

- Add context
- Clarify instructions
- Specify audience
- Add examples
- Strengthen constraints
- Improve tone

---

# NEW — Lesson 02 Techniques

---

# Technique 11 — Iterative Refinement

## Definition

Iterative Refinement is the process of improving AI-generated outputs through multiple conversational turns rather than rewriting the original prompt.

Each follow-up instruction progressively moves the output closer to the desired result.

---

## Why It Matters

The first response is rarely the final response.

Professional AI users improve outputs gradually by refining:

- accuracy
- clarity
- tone
- completeness
- audience fit

---

## Workflow

Initial Draft

↓

Review

↓

Provide Targeted Feedback

↓

Generate Revised Draft

↓

Repeat Until Satisfied

---

## Physics Application

Instead of asking:

> Explain Newton's Second Law perfectly.

Use:

Iteration 1:
Generate explanation.

Iteration 2:
Simplify for Grade 10.

Iteration 3:
Add everyday examples.

Iteration 4:
Correct misconceptions.

Iteration 5:
Finish with a numerical example.

---

# Technique 12 — Conversation-as-Prompt

## Definition

Conversation-as-Prompt is the principle that an entire conversation functions as one continuously growing prompt.

The AI does not interpret only the latest message.

It interprets the entire conversation history.

---

## Components

Conversation history includes:

- previous prompts
- AI responses
- corrections
- refinements
- user feedback

---

## Importance

Conversation history reduces ambiguity.

Every new instruction becomes more meaningful because it references existing context.

---

## Lesson Insight

Prompt engineering extends beyond writing prompts.

It includes managing conversations.

---

# Technique 13 — Context Accumulation

## Definition

Context Accumulation is the gradual growth of conversational context throughout multiple interactions.

Every conversational turn contributes additional information.

---

## Benefits

Improves:

- continuity
- consistency
- personalization
- instruction following

---

## Risk

Incorrect information may also accumulate.

Prompt engineers should continuously monitor conversational context.

---

# Technique 14 — Conversational Memory Management

## Definition

Conversation Memory Management is the practice of monitoring accumulated conversational history to ensure that previous outputs continue supporting rather than degrading future responses.

---

## Responsibilities

Prompt engineers should:

- monitor previous outputs
- correct errors immediately
- remove misleading assumptions
- prevent conversational drift

---

## Professional Importance

This technique is especially important for:

- AI tutors
- AI teaching assistants
- educational chatbots
- customer support assistants

---

# Technique 15 — Instruction Refinement

## Definition

Instruction Refinement means improving AI behaviour by modifying follow-up instructions rather than rewriting the original prompt.

---

## Examples

Instead of:

Rewrite everything.

Use:

- Make the tone more conversational.
- Shorten the introduction.
- Add one real-world example.
- Remove promotional language.
- Explain for Grade 10 students.

---

## Best Practice

Each refinement should improve one specific aspect of the response.

---

# Technique 16 — Context Management

## Definition

Context Management is the deliberate process of controlling accumulated conversational context.

Prompt engineers decide:

- what should remain,
- what should be corrected,
- what should be removed,
- when to restart.

---

## Context Should Be Managed When

- hallucinations appear
- conversation drifts
- incorrect assumptions accumulate
- outputs become inconsistent

---

# Technique 17 — Multi-Turn Prompting

## Definition

Multi-Turn Prompting is a prompting strategy that intentionally uses multiple conversational interactions to complete one task.

---

## Benefits

Compared with single-turn prompting, multi-turn prompting provides:

- higher quality
- better personalization
- greater consistency
- easier refinement
- improved educational quality

---

## Physics Example

Lesson explanation

↓

Simplify

↓

Add diagram description

↓

Include misconceptions

↓

Add assessment questions

↓

Generate homework

Each conversational turn improves the educational resource.

---

# Best Practices (Lessons 01–02)

✓ Define a professional role.

✓ Build a detailed persona.

✓ Provide sufficient context.

✓ Specify the audience.

✓ Include authentic examples.

✓ Prevent hallucinations.

✓ Evaluate AI outputs critically.

✓ Refine through conversation.

✓ Improve one aspect at a time.

✓ Monitor accumulated context.

✓ Correct errors immediately.

✓ Preserve authentic teaching voice.

---

# Common Mistakes

❌ Writing vague prompts.

❌ Assuming AI knows missing information.

❌ Restarting conversations unnecessarily.

❌ Ignoring conversation history.

❌ Allowing hallucinations to accumulate.

❌ Giving multiple unrelated corrections simultaneously.

❌ Failing to review intermediate drafts.

---

# Physics AI Applications

The techniques learned so far support:

- AI Physics Tutors
- Lesson Planning
- Laboratory Instructions
- Assessment Generation
- Student Feedback
- Parent Communication
- Educational Chatbots
- AI Teaching Assistants
- Physics Curriculum Design

---

# Key Insight

> **Prompt Engineering is no longer just the discipline of writing effective prompts. It is the discipline of designing, evaluating, and managing intelligent conversations that progressively guide AI toward accurate, reliable, and context-aware outputs.**

---

# Revision History

| Version | Lessons Included | Status |
|----------|-----------------|--------|
| v1.0 | Lesson 01 | ✅ Complete |
| v2.0 | Lessons 01–02 | ✅ Complete |
| v3.0 | Lesson 03 | ⏳ Planned |
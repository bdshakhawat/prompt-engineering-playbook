# Persona Design Analysis

## Purpose

This document explains the design decisions behind my **Physics Teacher Writing Persona Prompt** and identifies the prompt engineering techniques used in each section.

Rather than writing a prompt intuitively, I intentionally combined multiple prompt engineering techniques to improve output quality, consistency, factual reliability, and preservation of writing style.

---

# Prompt Architecture

The persona prompt consists of multiple components, each serving a specific purpose.

---

# 1. ROLE

## Purpose

The Role section establishes the AI's identity and primary responsibility before any task is performed.

Instead of treating the model as a generic assistant, it defines a very specific professional identity:

> "You are my professional AI writing assistant."

This immediately narrows the model's behaviour and creates a consistent perspective for generating responses.

The role also explicitly states that the AI should write **in my voice**, not its default writing style.

Without a clear role, LLMs often fall back to generic assistant behaviour.

## Prompt Engineering Techniques

- Role Prompting
- Persona Prompting
- Identity Conditioning

---

# 2. GOAL

## Purpose

The Goal section defines what success looks like.

Rather than simply asking the AI to "write," it establishes the desired outcome:

> Produce writing that faithfully reproduces my communication style.

Providing an explicit objective reduces ambiguity and gives the model a measurable target.

## Prompt Engineering Techniques

- Goal-Oriented Prompting
- Objective Specification
- Task Framing

---

# 3. CONTEXT

## Purpose

Large Language Models perform better when they understand the environment in which the writing will be used.

The Context section informs the AI that the writing is intended for educational communication rather than marketing or creative writing.

This helps the model choose appropriate vocabulary, tone, and structure.

## Prompt Engineering Techniques

- Context Injection
- Domain Conditioning

---

# 4. AUDIENCE ADAPTATION

## Purpose

Good writers naturally adjust their communication depending on the audience.

This section teaches the AI to modify language while preserving the same underlying writing personality.

Students require simple explanations.

Parents require reassurance.

Teachers expect technical precision.

School administrators prefer concise professional communication.

Separating audiences significantly improves response quality.

## Prompt Engineering Techniques

- Audience Conditioning
- Adaptive Prompting
- Context-Specific Prompting

---

# 5. MY WRITING VOICE

## Purpose

This is the core of the persona prompt.

Instead of saying

> "Write professionally"

the prompt explicitly defines characteristics such as:

- calm
- practical
- concise
- experienced
- anticipates misconceptions
- avoids unnecessary enthusiasm

These characteristics collectively create a unique writing identity.

This allows the AI to imitate style rather than merely generate correct grammar.

## Prompt Engineering Techniques

- Style Transfer
- Persona Prompting
- Attribute Conditioning

---

# 6. WRITING PRINCIPLES

## Purpose

Writing style alone is insufficient.

The Writing Principles section defines the values that should guide every response.

These principles ensure that the AI consistently prioritizes:

- clarity
- honesty
- usefulness
- professionalism

This creates behavioural consistency across different writing tasks.

## Prompt Engineering Techniques

- Behavioral Conditioning
- Principle-Based Prompting

---

# 7. RULES

## Purpose

The Rules section explicitly defines acceptable and unacceptable behaviour.

Instead of assuming the model understands what should be avoided, the prompt clearly states:

DO

and

DO NOT

instructions.

Negative instructions often reduce undesirable outputs.

## Prompt Engineering Techniques

- Constraint Prompting
- Rule-Based Prompting
- Negative Prompting

---

# 8. HALLUCINATION POLICY

## Purpose

Hallucination is one of the major limitations of Large Language Models.

This section explicitly instructs the model:

Never invent facts.

Instead of optimizing only for fluent writing, the prompt prioritizes factual accuracy.

This is particularly important for educational content.

## Prompt Engineering Techniques

- Hallucination Mitigation
- Truthfulness Prompting
- Reliability Prompting

---

# 9. CLARIFICATION POLICY

## Purpose

Most AI systems attempt to answer every question, even when important information is missing.

This policy changes that behaviour.

Instead of guessing,

the AI is instructed to ask follow-up questions.

This significantly reduces hallucinations.

## Prompt Engineering Techniques

- Interactive Prompting
- Clarification Prompting
- Human-in-the-Loop Prompting

---

# 10. OUTPUT REQUIREMENTS

## Purpose

This section defines the expected properties of the final response.

Examples include:

- natural English
- concise writing
- factual accuracy
- logical organization

Providing explicit output requirements improves response consistency.

## Prompt Engineering Techniques

- Output Specification
- Structured Prompting

---

# 11. SELF-CHECK

## Purpose

Before generating the final response,

the AI evaluates its own work against predefined quality criteria.

This encourages an additional reasoning step before producing the answer.

Self-evaluation often improves quality and reduces obvious mistakes.

## Prompt Engineering Techniques

- Self-Reflection Prompting
- Self-Evaluation
- Prompt Chaining
- Iterative Refinement

---

# 12. WRITING SAMPLE

## Purpose

The writing sample demonstrates the desired writing style rather than merely describing it.

Large Language Models learn style much more effectively from examples than from abstract instructions.

This enables more accurate imitation of vocabulary, sentence structure, tone, pacing, and organization.

## Prompt Engineering Techniques

- In-Context Learning
- Example-Based Prompting
- Few-Shot Prompting
- Style Transfer

---

# Overall Prompt Engineering Techniques Used

This persona prompt combines multiple prompt engineering techniques into a single production-style prompt.

| Technique | Used? | Purpose |
|-----------|:----:|---------|
| Role Prompting | ✅ | Define AI identity |
| Persona Prompting | ✅ | Reproduce author's voice |
| Goal-Oriented Prompting | ✅ | Define success criteria |
| Context Injection | ✅ | Provide writing environment |
| Audience Conditioning | ✅ | Adapt communication style |
| Style Transfer | ✅ | Preserve writing personality |
| Constraint Prompting | ✅ | Prevent unwanted behaviour |
| Rule-Based Prompting | ✅ | Control model behaviour |
| Hallucination Mitigation | ✅ | Improve factual reliability |
| Clarification Prompting | ✅ | Prevent guessing |
| Output Specification | ✅ | Standardize responses |
| Self-Evaluation | ✅ | Improve final output quality |
| In-Context Learning | ✅ | Learn from writing examples |
| Example-Based Prompting | ✅ | Demonstrate desired style |

---

# Key Learning

This assignment demonstrated that effective prompt engineering is not simply writing longer prompts.

Instead, it is the deliberate combination of multiple prompt engineering techniques that guide a Large Language Model toward reliable, context-aware, and human-like outputs.

Each section of the persona prompt serves a specific engineering purpose.

Together, these components create a structured system that improves writing quality, preserves author voice, reduces hallucinations, and produces more consistent AI-generated content.
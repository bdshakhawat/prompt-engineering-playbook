# knowledge-base/01 AI Glossary

> A practical reference of key Artificial Intelligence, Generative AI, Large Language Model, Prompt Engineering, and AI Evaluation terminology used throughout this Prompt Engineering Playbook.

---

## Purpose

This glossary provides a consistent vocabulary for the concepts, techniques, and patterns used throughout this repository.

The terms are particularly relevant to:

- Generative AI
- Large Language Models (LLMs)
- Prompt Engineering
- In-Context Learning
- AI Evaluation
- AI Training
- Retrieval-Augmented Generation (RAG)
- Educational AI
- Physics AI applications

The definitions are written from a practical Prompt Engineering perspective rather than as a comprehensive technical dictionary.

---

# A

## AI — Artificial Intelligence

A broad field of computing focused on creating systems capable of performing tasks that involve capabilities associated with human intelligence, such as language understanding, pattern recognition, reasoning, learning, and decision-making.

**Prompt Engineering relevance:**  
AI systems can be guided through carefully designed instructions, context, examples, constraints, and output requirements.

---

## AI Evaluation

The systematic process of assessing the quality, accuracy, reliability, or usefulness of an AI system or its output.

Evaluation may consider:

- Accuracy
- Relevance
- Instruction following
- Reasoning quality
- Consistency
- Safety
- Format compliance
- Domain correctness

**Physics AI example:**  
Evaluating whether an AI-generated explanation of momentum is scientifically accurate and appropriate for a secondary-school student.

---

## AI Trainer

A person who contributes to improving AI systems through activities such as creating examples, evaluating model outputs, providing feedback, labeling data, or applying domain expertise.

**Physics AI relevance:**  
A Physics AI Trainer may evaluate AI-generated Physics questions, solutions, explanations, or reasoning.

---

## AI Subject Matter Expert (AI SME)

A domain expert who applies specialized subject knowledge to AI development, training, evaluation, or quality assurance.

**Physics AI example:**  
A Physics SME evaluates whether an AI-generated solution correctly applies Newton's Laws.

---

# C

## Chain of Thought (CoT)

A term used to describe step-by-step reasoning associated with solving a problem.

In Prompt Engineering, reasoning-oriented instructions may encourage a model to carefully analyze a task before producing its answer.

**Important evaluation principle:**  
Focus on the correctness and usefulness of the model's observable response rather than requiring disclosure of private internal reasoning.

---

## Context

The information available to a model when generating a response.

Context can include:

- Instructions
- Previous conversation
- Examples
- Documents
- Retrieved information
- User-provided data

**Prompt Engineering relevance:**  
Good prompts provide the model with the context it needs to perform the task accurately.

---

## Context Window

The amount of information a model can process within a particular interaction.

**Prompt Engineering relevance:**  
When working with large documents or knowledge bases, relevant information may need to be selected, retrieved, summarized, or divided into smaller sections.

---

## Constraint

A rule or limitation placed on an AI task.

Examples:

- Maximum word count
- Required format
- Target audience
- Number of recommendations
- Required sections
- Prohibited content

**Example:**

> "Explain the concept in fewer than 100 words and include one real-world example."

Constraints help make the desired output more predictable.

---

# E

## Evaluation Criteria

Specific properties used to determine whether an AI output meets a desired standard.

Examples:

- Accuracy
- Relevance
- Clarity
- Completeness
- Instruction following
- Appropriate tone
- Mathematical correctness

---

## Evaluation Rubric

A structured framework containing criteria and performance levels used to evaluate AI outputs consistently.

Example:

| Criterion | Strong | Weak |
|---|---|---|
| Accuracy | Correct information | Contains factual errors |
| Relevance | Directly answers the task | Goes off-topic |
| Format | Follows requested structure | Ignores structure |

---

# F

## Few-Shot Prompting

A prompting technique in which the model receives several examples demonstrating the desired input-output behavior before being asked to perform a new task.

Typical structure:

```text
Input: Example 1
Output: Desired Output 1

Input: Example 2
Output: Desired Output 2

Input: New Task
Output:
==============================================================================================================================================
G
Generative AI

AI capable of generating new content based on learned patterns and provided instructions.

Examples include generation of:

Text
Images
Audio
Video
Code

Prompt Engineering relevance:
Prompt Engineering helps guide what Generative AI produces and how it is structured.

Grounding

Connecting an AI response to reliable, relevant information rather than relying only on the model's general learned knowledge.

Grounding can involve:

User-provided information
Documents
Knowledge bases
Retrieved sources
Structured data
H
Hallucination

An AI-generated statement that is inaccurate, unsupported, fabricated, or inconsistent with the available information, despite appearing plausible.

Examples include:

Inventing facts
Fabricating sources
Creating unsupported numerical values
Inventing information not present in the supplied material
Hallucination Mitigation

Techniques used to reduce unsupported or incorrect AI-generated information.

Examples include:

Providing relevant context
Restricting the model to supplied information
Requiring evidence
Identifying information gaps
Using structured prompts
Applying evaluation criteria
Grounding responses in reliable sources
I
In-Context Learning

The ability of a model to adapt its response to instructions, context, or examples provided within the current interaction without changing the underlying model parameters.

Examples and instructions can demonstrate:

Task behavior
Output structure
Tone
Classification rules
Desired reasoning approach

Few-shot prompting is a common form of in-context learning.

Information Gap

Information needed to perform a task accurately but not provided in the available context.

Example:

A Physics problem asks for acceleration but does not provide enough information to calculate it.

A reliable AI response should identify the information gap rather than inventing missing information.

Instruction

A directive telling the AI what task to perform or how to perform it.

Example:

"Analyze the following plan using four distinct analytical lenses."

Input

The information provided to an AI model for processing.

An input may be:

A question
A document
A dataset
A user request
A Physics problem
A set of examples
L
LLM — Large Language Model

An AI model trained on large amounts of data to process and generate language.

LLMs can perform tasks such as:

Question answering
Summarization
Classification
Transformation
Content generation
Information extraction
Reasoning assistance

Prompt Engineering relevance:
Prompt Engineering provides instructions and context that guide an LLM toward a desired output.

M
Markdown

A lightweight markup language used to create structured documents using plain text.

Common Markdown elements include:

# Header

## Section

- Bullet point

| Column | Column |
|---|---|
| Data | Data |

Markdown is used extensively throughout this Prompt Engineering Playbook because it is readable, portable, and easy to version-control with Git.

Multi-Perspective Analysis

A prompting approach that analyzes the same problem using multiple distinct analytical lenses.

For example:

Risk Lens
Feasibility Lens
Stakeholder Lens
Opportunity Lens

The purpose is to reduce the limitations of relying on a single perspective.

P
Persona Prompting

A prompting technique that establishes a role, perspective, expertise, or communication style for the AI.

Example:

"Act as an experienced secondary-school Physics educator."

A persona can help establish the perspective and style expected for a task.

Prompt

An instruction or set of instructions given to an AI model to guide its response.

A prompt may contain:

Role
Task
Context
Examples
Constraints
Output Format
Evaluation Criteria
Prompt Engineering

The systematic design, testing, evaluation, and refinement of prompts to improve the usefulness, reliability, and structure of AI-generated outputs.

Prompt Engineering may involve:

Clear instructions
Context
Examples
Constraints
Output formats
Prompt patterns
Iterative refinement
Evaluation
Prompt Pattern

A reusable solution structure for a recurring Prompt Engineering problem.

Examples include:

Persona Pattern
Template Pattern
Few-Shot Pattern
Multi-Perspective Pattern
Taxonomy Pattern
Evaluation Pattern

A pattern is more general than a single task-specific prompt.

Prompt Template

A reusable prompt containing fixed instructions and placeholders for information that changes from task to task.

Example:

Act as a [ROLE].

Your task is to [TASK].

Use the following information:
[INPUT]

Return the result in this format:
[OUTPUT FORMAT]

Templates improve consistency and reduce the need to rewrite prompts from scratch.

Preference-Driven Refinement

A process of improving AI outputs by explicitly defining the qualities or preferences that the desired output should satisfy.

Examples:

More concise
More professional
More student-friendly
Less repetitive
More evidence-based
More structured

Preference-driven refinement can also be used to develop better examples for few-shot prompting.

Prompt Chaining

A technique in which multiple prompts or AI calls are connected so that the output of one step becomes the input or context for another step.

Example:

Extract Information
       ↓
Analyze Information
       ↓
Generate Recommendations
       ↓
Format Final Report

This can be useful when a complex task is easier to handle as a sequence of smaller tasks.

Prompt Injection

An attempt to manipulate an AI system by inserting instructions into user-provided or retrieved content that conflict with the intended instructions.

Example:

A document being analyzed contains hidden or explicit instructions telling the AI to ignore its original task.

Best practice:
Treat untrusted retrieved content primarily as data to analyze rather than automatically treating embedded instructions as authoritative.

R
RAG — Retrieval-Augmented Generation

A method in which relevant information is retrieved from an external knowledge source and supplied to an AI model as context before generating a response.

Typical workflow:

User Question
      ↓
Retrieve Relevant Information
      ↓
Provide Retrieved Context
      ↓
Generate Response
      ↓
Evaluate Response

RAG can help ground AI responses in specific knowledge sources.

Retrieval

The process of finding relevant information from a knowledge base, document collection, database, or other information source.

S
Semantic Similarity

The degree to which two pieces of information are similar in meaning, even if they use different words.

Semantic similarity is useful in systems that retrieve information based on meaning rather than exact keyword matching.

Structured Output

An AI response that follows a predefined structure or format.

Examples:

Tables
Lists
Markdown sections
JSON
Rubrics
Taxonomies

Structured output makes AI responses easier to evaluate, compare, store, and reuse.

Synthetic Data

Artificially generated data designed to resemble useful examples of real-world data.

In Prompt Engineering, synthetic examples can be created to demonstrate desired input-output behavior for few-shot prompts.

Synthetic data should still be reviewed for:

Accuracy
Relevance
Diversity
Consistency
Unintended bias
T
Taxonomy

A hierarchical classification system that organizes information into categories and subcategories.

Example:

Education
├── Teaching
│   ├── Lesson Planning
│   └── Assessment
└── Technology
    ├── AI
    └── Automation

A taxonomy can help organize clustered information into a meaningful hierarchy.

Template Pattern

A Prompt Engineering pattern in which the desired structure of the output is explicitly defined.

Example:

# Executive Summary

# Key Findings

# Recommendations

# Next Steps

The model is instructed to fill the structure while preserving the requested organization.

Token

A unit of text processed by a language model.

A token may represent:

A complete word
Part of a word
Punctuation
Other text elements

Tokenization varies between models.

U
User Intent

The underlying objective or purpose behind a user's request.

Understanding user intent helps distinguish what the user literally says from what they actually need the AI to accomplish.

Uncertainty

A situation in which the available information is insufficient to establish a conclusion with confidence.

A reliable AI system should acknowledge meaningful uncertainty rather than presenting unsupported conclusions as certain.

V
Validation

The process of checking whether an AI output, prompt, dataset, or knowledge resource meets the intended requirements.

Validation may involve:

Testing examples
Comparing outputs
Checking factual accuracy
Applying evaluation rubrics
Reviewing edge cases
Z
Zero-Shot Prompting

A prompting technique in which the model is asked to perform a task without being provided task-specific examples.

Example:

Explain Newton's First Law to a Grade 10 student in simple language.

No example input-output pairs are provided.

Key Prompt Engineering Concepts

The following concepts form an important progression within this playbook:

Clear Task
    ↓
Context
    ↓
Role / Persona
    ↓
Constraints
    ↓
Examples
    ↓
Output Structure
    ↓
Evaluation
    ↓
Refinement

Not every prompt requires every component.

The appropriate components should be selected according to the task.

Prompting Spectrum

Prompting techniques can range from simple to more structured approaches:

Zero-Shot
    ↓
Clear Instructions
    ↓
Role / Persona
    ↓
Constraints
    ↓
Template
    ↓
Few-Shot Examples
    ↓
Preference-Driven Refinement
    ↓
Multi-Step / Chained Workflows
    ↓
RAG / Grounded Workflows

This is not a strict hierarchy of "better" techniques. More complex prompting is not automatically better.

The goal is to use the simplest approach that reliably achieves the desired result.

AI Output Quality

Throughout this playbook, a high-quality AI response should generally aim to be:

Accurate + Relevant + Clear + Instruction-Following + Appropriate + Reliable

For domain-specific work, such as Physics, subject-matter accuracy becomes an additional critical requirement.

Relationship to This Playbook

The terms in this glossary support the other knowledge-base files:

AI-Glossary
      ↓
Terminology
      ↓
Prompt Engineering Techniques
      ↓
Prompt Patterns
      ↓
Reusable Templates
      ↓
Best Practices
      ↓
Hallucination Mitigation
      ↓
AI Evaluation

Each file has a different purpose. The glossary defines the terminology; it does not attempt to provide the complete explanation of every technique.

Glossary Maintenance

This is a living document.

New terms may be added as they become relevant to:

Prompt Engineering
Generative AI
AI evaluation
AI training
RAG
Educational AI
Physics AI
LLM workflows

When adding a new term:

Provide a concise definition.
Explain its Prompt Engineering relevance when useful.
Give an example when it improves understanding.
Avoid unnecessary technical jargon.
Keep terminology consistent with the rest of the repository.
Avoid duplicating detailed material that belongs in another knowledge-base file.
Version

Version: 1.0
Status: Active Development
Last Updated: August 2026

Author

Muhammad Shakhawat Hossain

M.Sc. in Physics | Physics Educator | Prompt Engineering | Generative AI | AI Evaluation

GitHub: https://github.com/bdshakhawat
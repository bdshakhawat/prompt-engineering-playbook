# AI Glossary

> A reusable reference of key Artificial Intelligence, Generative AI, Prompt Engineering, LLM, AI Evaluation, and AI Training terminology used throughout the Physics AI Knowledge Base.

---

## Purpose

This glossary provides consistent definitions for technical terms used across this repository.

The goal is to maintain a common vocabulary when designing:

- Physics AI prompts
- AI evaluation frameworks
- AI training resources
- Physics knowledge units
- AI-assisted educational content
- Retrieval-Augmented Generation (RAG) experiments
- Physics AI projects

Definitions are written with a practical focus on **Physics education, AI training, prompt engineering, and AI evaluation**.

---

# A

## AI — Artificial Intelligence

A field of computing focused on creating systems that can perform tasks that normally require aspects of human intelligence, such as reasoning, learning, language understanding, perception, and decision-making.

**Physics AI relevance:**  
AI systems can assist with Physics explanation, question generation, assessment, tutoring, and evaluation.

---

## AI Evaluation

The systematic process of assessing the quality, accuracy, reliability, safety, or usefulness of an AI system or its outputs.

**Physics AI example:**  
Evaluating whether an AI-generated explanation of Newton's Laws is scientifically correct, logically sound, and appropriate for the intended student level.

---

## AI Training

The process of preparing AI systems to perform desired tasks through training data, examples, feedback, evaluation, or other learning processes.

**Physics AI relevance:**  
Physics SMEs may contribute domain knowledge, examples, rubrics, annotations, evaluations, and expert feedback used to improve AI systems.

---

## AI Trainer

A person who helps improve AI systems by creating, reviewing, labeling, evaluating, or refining training examples and AI-generated responses.

**Physics AI relevance:**  
A Physics AI Trainer may evaluate whether an AI response correctly explains a Physics concept or solves a Physics problem.

---

## AI Subject Matter Expert (AI SME)

A domain expert who provides specialized knowledge to help develop, train, evaluate, or improve AI systems in a particular subject area.

**Physics AI example:**  
A Physics SME evaluates whether an AI-generated solution correctly applies conservation of momentum and identifies conceptual errors.

---

## AI-Assisted Education

The use of AI tools to support teaching, learning, assessment, content creation, feedback, or educational planning.

**Important principle:**  
AI should augment educational expertise rather than replace appropriate human judgment.

---

## Annotation

The process of adding structured labels, classifications, explanations, or other information to data so that it can be used for AI training or evaluation.

**Physics example:**  
Labeling an AI-generated Physics answer as:

- Correct
- Partially Correct
- Incorrect
- Contains Conceptual Misconception

---

## Assumption

An unstated or explicitly stated condition accepted as true for the purpose of an analysis, solution, or response.

**Physics AI relevance:**  
AI responses should distinguish between information provided in a problem and assumptions introduced to complete the reasoning.

---

# C

## Chain of Thought (CoT)

A term commonly used to describe step-by-step reasoning processes used to arrive at an answer.

**Physics AI relevance:**  
Physics problems often require sequential reasoning involving equations, assumptions, substitutions, and conclusions.

**Evaluation note:**  
For professional AI evaluation, focus on whether the observable reasoning, explanation, and final answer are correct rather than requiring disclosure of private internal reasoning.

---

## Context

The information available to an AI model when it generates a response.

Context may include:

- User instructions
- Previous conversation
- Documents
- Examples
- Retrieved information
- Structured data

**Physics example:**  
Providing the relevant Physics knowledge and problem conditions as context before asking an AI to solve a problem.

---

## Context Window

The amount of text or other information an AI model can process as context during a particular interaction.

**Physics AI relevance:**  
Large knowledge bases may need to be divided, retrieved, or summarized so that relevant information fits within the model's available context.

---

## Constraint

A rule or limitation placed on an AI task.

Examples:

- Word limit
- Required format
- Target audience
- Required equations
- Prohibited content
- Number of recommendations

**Physics example:**  
"Explain momentum to a Grade 10 student in fewer than 100 words and include one real-world example."

---

## Curriculum Alignment

The process of ensuring that AI-generated educational content matches a specified curriculum, learning objective, grade level, or educational standard.

---

# E

## Embedding

A numerical representation of text or other information that captures aspects of its meaning and can be used for similarity-based retrieval or comparison.

**RAG relevance:**  
Embeddings can help identify knowledge-base content that is semantically related to a user's question.

---

## Evaluation Criteria

Specific properties used to judge whether an AI response meets a desired standard.

Examples:

- Factual accuracy
- Conceptual accuracy
- Mathematical correctness
- Reasoning quality
- Clarity
- Relevance
- Appropriate difficulty
- Unit correctness

---

## Evaluation Rubric

A structured set of criteria and performance levels used to consistently evaluate AI outputs.

**Physics example:**

| Criterion | Excellent | Needs Improvement |
|---|---|---|
| Physics accuracy | Scientifically correct | Contains conceptual errors |
| Calculation | Correct | Calculation error |
| Units | Correct SI units | Missing or incorrect units |
| Explanation | Clear and appropriate | Confusing or incomplete |

---

## Evidence

Information that supports a claim, conclusion, classification, or evaluation.

**Physics AI relevance:**  
An evaluator should be able to identify what part of an AI response supports a judgment about its correctness.

---

# F

## Few-Shot Prompting

A prompting technique in which a model is given several examples of inputs and desired outputs before being asked to handle a new input.

Typical structure:

```text
Input: ...
Output: ...

Input: ...
Output: ...

Input: [new task]
Output:

========================================================================================================================================

Physics AI example:
Providing several examples of high-quality Physics explanations before asking the model to explain a new Physics concept.

Fine-Tuning

A process in which a pretrained AI model is further trained on a specific dataset or task so that its behavior can become better adapted to that task.

Important distinction:
Few-shot prompting changes the instructions and examples provided in the context; fine-tuning changes the model through additional training.

G
Generative AI

AI systems capable of generating new content such as:

Text
Images
Audio
Video
Code

Physics AI relevance:
Generative AI can produce Physics explanations, examples, questions, lesson materials, and evaluation drafts that require expert review.

Grounding

Connecting an AI response to reliable, relevant information rather than allowing the model to rely only on its general learned patterns.

Physics example:
Grounding an AI explanation in a verified Physics knowledge base.

H
Hallucination

An AI-generated statement that appears plausible but is unsupported, inaccurate, fabricated, or inconsistent with available information.

Physics example:
An AI invents a Physics constant, uses a nonexistent equation, or claims an experiment produces a result that is not supported by the supplied information.

Hallucination Mitigation

Techniques used to reduce unsupported or incorrect AI-generated information.

Examples:

Providing authoritative source information
Using structured prompts
Requiring evidence
Restricting the model to supplied information
Identifying information gaps
Applying evaluation rubrics
Verifying calculations and equations
I
In-Context Learning

The ability of a model to adapt its response behavior based on instructions, examples, or information provided within the current context without changing the underlying model parameters.

Example:

Example Input → Example Output
Example Input → Example Output
New Input → Expected patterned output

Few-shot prompting is a common way to perform in-context learning.

Information Gap

Information required to answer or evaluate a question accurately but not provided in the available context.

Physics example:
A problem asks for acceleration but does not provide enough information to determine the net force.

A reliable AI system should identify the missing information rather than invent it.

Instruction

A directive that tells an AI model what task to perform or how to perform it.

Example:

"Evaluate the following Physics explanation for conceptual accuracy."

Input

The information provided to an AI system for processing.

Examples:

Question
Physics problem
Student response
Document
Dataset
Prompt
L
LLM — Large Language Model

A machine-learning model designed to process and generate language and other forms of information.

LLMs can perform tasks such as:

Question answering
Summarization
Classification
Content generation
Transformation
Reasoning assistance
Information extraction

Physics AI relevance:
LLMs can assist with Physics education and evaluation but require domain-specific validation.

Long-Context Model

An AI model capable of processing a comparatively large amount of information within a single context.

Physics AI relevance:
Useful when working with large Physics documents, curricula, datasets, or collections of knowledge units.

M
Markdown

A lightweight markup language used to format structured text.

Common Markdown elements include:

# Header

## Subheader

- Bullet point

| Column | Column |
|---|---|
| Data | Data |

Markdown is used throughout this knowledge base because it is readable by humans and convenient for structured documentation.

Model

A trained computational system capable of performing specified AI tasks.

In Generative AI contexts, a model may generate or transform content based on input and instructions.

Model Output

The response generated by an AI model after receiving an input, prompt, or other context.

Physics AI evaluation:
Model outputs should be evaluated for accuracy, reasoning quality, relevance, clarity, and appropriateness.

Multi-Perspective Analysis

A prompting approach that evaluates a problem using multiple analytical lenses or viewpoints.

Example lenses:

Risk
Feasibility
Stakeholder impact
Opportunity

Physics AI application:
A Physics AI response could be evaluated from multiple perspectives such as scientific accuracy, mathematical correctness, pedagogy, and clarity.

P
Persona Prompting

A prompting technique that instructs the AI to adopt a particular role, expertise, perspective, or communication style.

Example:

"Act as an experienced secondary-school Physics educator."

Purpose:
To establish the perspective and style expected for the task.

Prompt

An instruction or set of instructions provided to an AI model to guide its behavior and output.

A prompt may contain:

Role
Task
Context
Examples
Constraints
Output format
Evaluation criteria
Prompt Engineering

The systematic design, testing, and refinement of prompts to obtain useful, reliable, and appropriately structured AI outputs.

Common techniques include:

Role prompting
Few-shot prompting
Template patterns
Constraints
Structured output
Multi-perspective analysis
Preference-driven refinement
Evaluation prompts
Prompt Pattern

A reusable structure for solving a recurring prompting problem.

Examples:

Persona Pattern
Template Pattern
Few-Shot Pattern
Multi-Perspective Pattern
Evaluation Pattern
Taxonomy Pattern

A prompt pattern is more general than a single task-specific prompt.

Prompt Template

A reusable prompt containing fixed instructions and placeholders for variable information.

Example:

Explain [PHYSICS CONCEPT] to [TARGET AUDIENCE].

Include:
- Definition
- Key principle
- Real-world example
- Common misconception
Preference-Driven Refinement

A process in which desired qualities or preferences are explicitly defined and used to improve generated outputs.

Examples of preferences:

Clear rather than technical
Concise rather than verbose
Student-friendly
Evidence-based
Structured
Professional

Preference-driven refinement can also be used to create better synthetic examples for few-shot prompting.

Prompt Injection

An attempt to manipulate an AI system by inserting instructions into user-provided or retrieved content that conflict with the intended instructions or system behavior.

Knowledge-base relevance:
Retrieved documents should be treated as information to analyze rather than automatically trusted instructions.

R
RAG — Retrieval-Augmented Generation

A method in which relevant information is retrieved from an external knowledge source and provided to a Generative AI model as context before generating a response.

Typical workflow:

User Question
      ↓
Retrieve Relevant Knowledge
      ↓
Provide Knowledge to Model
      ↓
Generate Response
      ↓
Evaluate Response

Physics AI example:
Retrieve the relevant knowledge unit for "momentum" before asking an AI system to answer a student question about momentum.

Retrieval

The process of finding relevant information from a knowledge base, document collection, database, or other information source.

Response Evaluation

The process of examining an AI-generated response against predefined criteria.

A Physics response may be evaluated for:

Physics accuracy
Mathematical accuracy
Reasoning
Units
Misconceptions
Clarity
Student-level appropriateness
S
Semantic Similarity

A measure of how closely related two pieces of information are in meaning, even when they use different words.

RAG relevance:
Semantic similarity can help retrieve knowledge that is conceptually related to a user's question.

SME — Subject Matter Expert

A person with specialized knowledge and experience in a particular domain.

Physics SME example:
An experienced Physics educator who can determine whether an AI-generated explanation is scientifically and pedagogically appropriate.

Structured Output

An AI response that follows a predefined organization or format.

Examples:

Markdown sections
Tables
JSON
Lists
Rubrics
Taxonomies

Structured output makes AI responses easier to evaluate, compare, store, and reuse.

Synthetic Data

Artificially generated data created to resemble useful examples of real-world data.

AI training relevance:
Synthetic examples can be used to develop prompt examples, evaluation scenarios, or test cases, but they should be reviewed for accuracy and suitability.

T
Taxonomy

A hierarchical classification system that organizes related concepts into categories and subcategories.

Example:

Physics
├── Mechanics
│   ├── Motion
│   ├── Forces
│   └── Momentum
│
└── Electricity
    ├── Charge
    ├── Electric Field
    └── Current

AI relevance:
Taxonomies can help organize knowledge bases and analyze clusters of information.

Template Pattern

A prompt engineering approach in which the desired structure of the output is explicitly specified before the model performs the task.

Example:

# Summary

# Key Findings

# Recommendations

The model fills the template while preserving the requested structure.

Token

A unit of text processed by a language model.

A token may represent:

A complete word
Part of a word
Punctuation
Other text elements

Tokenization differs between models.

U
Uncertainty

A lack of sufficient information or confidence to establish a conclusion reliably.

Physics AI principle:
An AI system should communicate meaningful uncertainty rather than presenting an unsupported conclusion as certain.

User Intent

The underlying goal or purpose behind a user's request.

Physics example:
A student asking "Why does the ball stop?" may be seeking a conceptual explanation rather than simply asking for a numerical calculation.

V
Validation

The process of checking whether an AI output, dataset, prompt, or knowledge resource meets the intended requirements.

Physics example:
Checking whether an AI-generated solution produces the correct result and uses physically valid reasoning.

Z
Zero-Shot Prompting

A prompting approach in which the model is asked to perform a task without being given task-specific examples.

Example:

Explain Newton's First Law to a Grade 9 student.

No example input/output pairs are provided.

Key Relationships Between Terms

The following relationships are particularly important for this project:

                    PHYSICS SME
                        │
                        ▼
               Physics Knowledge
                        │
                        ▼
                 Prompt Engineering
                        │
          ┌─────────────┼─────────────┐
          ▼             ▼             ▼
      Templates      Examples      Constraints
          │             │             │
          └─────────────┼─────────────┘
                        ▼
                  Generative AI
                        │
                        ▼
                   Model Output
                        │
                        ▼
                 AI Evaluation
                        │
          ┌─────────────┼─────────────┐
          ▼             ▼             ▼
       Accuracy     Reasoning     Pedagogy
          │             │             │
          └─────────────┼─────────────┘
                        ▼
                 Refined Output
Core Terms for This Knowledge Base

The following terms are especially important throughout this project:

Term	Primary Role
Physics SME	Provides domain expertise
AI Trainer	Helps improve AI through examples, evaluation, and feedback
Prompt Engineering	Designs effective AI instructions
Generative AI	Generates or transforms content
LLM	Processes and generates language
In-Context Learning	Uses information/examples provided in context
Few-Shot Prompting	Uses examples to demonstrate desired behavior
RAG	Provides retrieved knowledge to the model
AI Evaluation	Measures output quality
Evaluation Rubric	Provides structured evaluation criteria
Hallucination	Unsupported or incorrect generated information
Grounding	Connects responses to reliable information
Taxonomy	Organizes knowledge hierarchically
Structured Output	Produces predictable, reusable response formats
Synthetic Data	Artificially generated examples or datasets
Physics AI Quality Principle

For this project, a high-quality AI-generated Physics response should aim to be:

Accurate + Relevant + Well-Reasoned + Clear + Appropriately Difficult + Grounded + Evaluated

A response should not be considered high quality simply because it sounds fluent or confident.

Glossary Maintenance

This glossary is a living document.

New terms may be added when they become relevant to:

Physics AI projects
Prompt Engineering
AI evaluation
AI training
RAG experiments
Educational AI
LLM evaluation
Knowledge-base development

When adding a new term:

Use a clear definition.
Explain its relevance to this project.
Provide a Physics AI example when useful.
Avoid unnecessary jargon.
Keep terminology consistent across the repository.
Version

Version: 1.0
Status: Active Development
Last Updated: August 2026

Author

Muhammad Shakhawat Hossain
M.Sc. in Physics | Physics Educator | Prompt Engineering | Generative AI | AI Evaluation

GitHub: https://github.com/bdshakhawat



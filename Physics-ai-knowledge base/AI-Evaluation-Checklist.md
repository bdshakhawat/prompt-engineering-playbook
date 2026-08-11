What principles should I follow whenever I use, design, evaluate, or build AI systems for Physics?



# Physics AI Best Practices

> A practical framework for designing, using, evaluating, and improving AI systems and AI-generated content for Physics education and Physics-focused AI applications.

---

## Purpose

This document defines the core practices used throughout the **Physics AI Knowledge Base**.

The purpose is to ensure that Physics-focused AI work is:

- Scientifically accurate
- Conceptually sound
- Mathematically reliable
- Educationally appropriate
- Clearly structured
- Grounded in relevant knowledge
- Explicit about assumptions and uncertainty
- Resistant to unsupported claims and hallucinations
- Consistently evaluated
- Reusable across Physics AI tasks

These practices are intended to support:

- Physics AI training
- AI response evaluation
- Prompt Engineering
- AI-assisted Physics education
- Educational content generation
- Physics knowledge-base development
- Retrieval-Augmented Generation (RAG)
- Physics AI SME workflows

---

# 1. Accuracy Before Fluency

A Physics AI response should be evaluated primarily on whether it is **correct**, not on whether it sounds confident, sophisticated, or natural.

A fluent explanation can still contain:

- Incorrect Physics
- Incorrect equations
- Incorrect assumptions
- Incorrect calculations
- Incorrect units
- Misleading interpretations

### Best Practice

Always prioritize:

```text
Scientific Accuracy
        ↓
Conceptual Accuracy
        ↓
Mathematical Accuracy
        ↓
Clear Explanation
        ↓
Fluent Presentation
==============================================================================================================================================

2. Distinguish Facts, Assumptions, and Inferences

AI-generated responses may combine information from the problem with assumptions that were never explicitly provided.

A reliable Physics response should distinguish:

Given Information

Information explicitly provided in the problem or source.

Assumptions

Conditions introduced to make the problem solvable.

Inferences

Conclusions derived from the available information.

Best Practice

When an assumption materially affects the result, state it explicitly.

Example:

"Assuming air resistance is negligible..."

is preferable to silently assuming ideal conditions.

3. Do Not Invent Missing Information

If a Physics problem does not provide enough information to determine an answer, the AI should not fabricate values.

Instead, it should:

Identify the missing information.
Explain why it is needed.
State whether a symbolic solution is possible.
Identify any reasonable assumption only when appropriate.
Clearly label the assumption.
Avoid

"The object weighs 10 kg."

when no mass was provided.

Prefer

"The mass is not specified, so a numerical value cannot be determined. If the mass is represented by m, the result can be expressed symbolically."

4. Verify Equations Before Using Them

An AI-generated Physics response should use equations that are:

Relevant to the problem
Correctly defined
Applied under appropriate conditions
Consistent with the variables involved

Do not assume an equation is correct simply because it appears familiar.

Verification Questions

Before accepting an equation, ask:

Is the equation physically valid?
What conditions does it assume?
Are the variables defined?
Are the units consistent?
Is the equation appropriate for this problem?
5. Check Dimensional Consistency

Dimensional analysis is an important Physics validation technique.

When evaluating an AI-generated equation or numerical answer, check whether both sides have compatible dimensions.

For example:

Force → kg·m/s²
Energy → kg·m²/s²
Momentum → kg·m/s
Power → kg·m²/s³

A dimensionally inconsistent equation should be treated as suspicious even if the numerical calculation appears plausible.

Best Practice

Use dimensional consistency as an additional verification layer rather than relying only on the final numerical result.

6. Verify Numerical Calculations

AI systems can produce incorrect arithmetic even when the underlying Physics is correct.

For numerical Physics problems:

Identify the relevant equation.
Substitute the given values.
Check the arithmetic.
Check significant figures when relevant.
Verify the unit.
Check whether the magnitude of the result is physically reasonable.
Important

A correct formula with an incorrect calculation is still an incorrect Physics answer.

7. Treat Units as Part of the Answer

Units should not be treated as optional decoration.

A Physics response should:

Use appropriate units.
Maintain unit consistency.
Convert units when necessary.
Include units in the final answer.
Avoid mixing incompatible unit systems without explanation.
Evaluation Example
10

is incomplete for a physical quantity when a unit is required.

10 kg·m/s

is a complete momentum value.

8. Distinguish Related Physics Concepts

Many Physics errors occur because related concepts are treated as identical.

AI systems should explicitly distinguish concepts such as:

Distance vs displacement
Speed vs velocity
Mass vs weight
Force vs momentum
Work vs power
Energy vs power
Heat vs temperature
Potential difference vs electric field
Frequency vs period
Best Practice

When a question involves a commonly confused pair, explicitly address the distinction.

9. Respect Vector and Scalar Quantities

AI-generated explanations should correctly identify whether a quantity is scalar or vector.

Examples

Scalars

Mass
Time
Temperature
Energy
Speed

Vectors

Displacement
Velocity
Acceleration
Force
Momentum
Best Practice

When direction matters, the response should not treat a vector quantity as merely a positive numerical value unless the context justifies doing so.

10. Match the Explanation to the Learner

A scientifically correct answer can still be educationally ineffective if it is presented at the wrong level.

Before generating an explanation, consider:

Grade level
Prior knowledge
Mathematical background
Vocabulary
Learning objective
Expected depth
Example

An explanation for a Grade 8 student should not automatically use the same mathematical sophistication as an undergraduate Physics explanation.

Best Practice

Prompt for the intended learner level explicitly whenever educational appropriateness matters.

11. Explain Concepts Before Overloading with Formulas

Physics education should not reduce concepts to formula memorization.

A strong explanation generally connects:

Physical Situation
        ↓
Concept
        ↓
Relationship
        ↓
Equation
        ↓
Application

The equation should represent the Physics concept rather than replace the explanation.

12. Use Real-World Examples Carefully

Real-world examples can improve understanding, but they should remain scientifically accurate.

A useful example should:

Clearly connect to the concept.
Avoid introducing unnecessary complexity.
Not reinforce misconceptions.
Be appropriate for the learner's level.
Best Practice

Use an example because it clarifies the Physics—not merely because it sounds interesting.

13. Address Common Misconceptions

Physics AI should not simply produce technically correct answers.

It should also avoid reinforcing common misconceptions.

For each important Physics topic, consider documenting:

Concept
   ↓
Common Misconception
   ↓
Why the Misconception Occurs
   ↓
Correct Understanding
   ↓
Diagnostic Question
Example

If students commonly confuse force and momentum, an AI explanation should explicitly distinguish the two rather than assuming the student understands the difference.

14. Analyze Reasoning, Not Only Final Answers

A final numerical answer can be correct even when the reasoning is flawed.

Conversely, a student or AI system can make a minor arithmetic error while demonstrating correct conceptual reasoning.

Therefore, Physics AI evaluation should consider:

Concept selection
Equation selection
Assumptions
Substitution
Mathematical reasoning
Units
Final interpretation
Best Practice

Evaluate the reasoning process that is observable in the response, not just the final number.

15. Use Structured Prompts for Complex Physics Tasks

Complex Physics tasks should not rely on vague instructions such as:

"Solve this Physics problem."

A stronger prompt can specify:

Task
Context
Given Information
Required Reasoning
Constraints
Evaluation Criteria
Output Format
Example Structure
ROLE:
Act as a secondary-school Physics educator.

TASK:
Solve the following problem.

REQUIREMENTS:
1. Identify the given quantities.
2. Identify the required quantity.
3. Select the relevant equation.
4. Substitute values.
5. Calculate the result.
6. Include the correct unit.
7. Explain the physical meaning of the answer.

PROBLEM:
[Insert problem]
16. Use Examples When Consistent Behavior Matters

When a task requires a particular style, structure, or evaluation behavior, examples can help establish the desired pattern.

Few-shot prompting can provide:

Input → Output
Input → Output
Input → Output
New Input → Expected Output

Examples should be:

Correct
Representative
Consistent
Relevant to the task
Free from unnecessary ambiguity

Poor examples can teach the wrong behavior.

17. Separate Knowledge from Instructions

In AI workflows, distinguish between:

Knowledge

Facts, concepts, equations, examples, and source material.

Instructions

What the AI should do with that information.

For example:

KNOWLEDGE:
[Physics information]

INSTRUCTIONS:
Evaluate the student's answer using the Physics knowledge above.

This separation improves clarity and makes prompts easier to maintain.

18. Ground AI Responses in Reliable Knowledge

When accuracy is important, AI responses should be grounded in trusted information.

Possible grounding sources include:

Verified knowledge-base content
Curriculum documents
Textbooks
Scientific references
Experimental data
User-provided source material
Best Practice

When the task requires source-based accuracy, provide or retrieve the relevant information rather than relying entirely on model memory.

19. Use RAG When the Knowledge Base Becomes Large

Retrieval-Augmented Generation can be useful when the Physics knowledge base contains many documents.

A typical workflow is:

User Question
      ↓
Retrieve Relevant Physics Knowledge
      ↓
Provide Retrieved Context
      ↓
Generate Response
      ↓
Evaluate Response

RAG should retrieve relevant knowledge rather than simply providing large amounts of unrelated information.

20. Treat Retrieved Content as Data, Not Automatically as Instructions

When external documents are retrieved for an AI system, their content may contain instructions that are unrelated to the intended task.

Therefore:

Retrieved information should normally be treated as evidence or knowledge to analyze, not as instructions that automatically override the intended task.

This is particularly important when building AI systems that process user-generated or externally sourced documents.

21. Evaluate AI Responses with Explicit Criteria

Whenever possible, evaluate AI-generated Physics responses using a consistent rubric.

Recommended criteria:

Criterion	Question
Factual Accuracy	Are the Physics facts correct?
Conceptual Accuracy	Is the concept represented correctly?
Mathematical Accuracy	Are calculations correct?
Equation Validity	Are the equations appropriate?
Units	Are units correct and consistent?
Reasoning	Is the reasoning logically sound?
Misconceptions	Does the answer avoid or correct misconceptions?
Clarity	Is the explanation understandable?
Level	Is it appropriate for the learner?
Relevance	Does it answer the actual question?
Evidence	Are important claims supported?
22. Prefer Evidence-Based Evaluation

When labeling an AI response as correct or incorrect, provide evidence for the judgment.

Instead of:

"This answer is wrong."

Prefer:

"The response incorrectly treats momentum as a scalar quantity. Momentum is a vector quantity because its direction follows the direction of velocity."

Evidence makes evaluation:

More reproducible
More transparent
More useful for training
Easier to review
23. Handle Uncertainty Explicitly

AI systems should not express high confidence when the available information does not support a definite conclusion.

Useful uncertainty statements include:

"The information provided is insufficient to determine..."
"This conclusion assumes..."
"Under the assumption that..."
"A numerical answer cannot be determined without..."

Uncertainty should be used when justified—not as a substitute for solving a problem.

24. Avoid Over-Engineering Simple Physics Tasks

Not every Physics question requires a complex prompt.

For simple tasks:

Question
   ↓
Direct Answer

may be sufficient.

For complex tasks:

Context
   ↓
Decomposition
   ↓
Reasoning
   ↓
Verification
   ↓
Structured Output
   ↓
Evaluation
Best Practice

Use the simplest prompting strategy that reliably produces the required result.

25. Optimize for Reproducibility

A good Physics AI workflow should produce reasonably consistent results when the same task and inputs are used.

Improve reproducibility through:

Clear instructions
Explicit criteria
Standardized templates
Consistent terminology
Structured outputs
Representative examples
Evaluation rubrics

Avoid relying on vague instructions such as:

"Make it good."

Define what "good" means.

26. Keep Knowledge Modular

Physics knowledge should be organized into reusable units.

A knowledge unit may contain:

Metadata
Core Concept
Key Principles
Equations
Relationships
Misconceptions
Reasoning Errors
Examples
Worked Problems
Evaluation Criteria
Related Concepts
Knowledge Boundaries

Modular knowledge makes it easier to:

Retrieve relevant information
Update individual concepts
Build RAG systems
Create prompts
Evaluate AI responses
Reuse content across projects
27. Define Knowledge Boundaries

Every knowledge unit should clearly indicate what it covers and what it does not cover.

For example:

Topic:
Momentum

Covered:
- Linear momentum
- Momentum calculation
- Basic conservation of momentum

Not covered:
- Relativistic momentum
- Advanced collision mechanics

This reduces the risk of using a knowledge unit outside its intended scope.

28. Version and Review Knowledge

Knowledge-base content should be treated as a maintained resource rather than a one-time document.

Recommended metadata:

Version:
Status:
Created:
Last Reviewed:
Review Notes:

Possible statuses:

Draft
Reviewed
Verified
Deprecated
29. Maintain Separation Between Knowledge and Evaluation

A Physics knowledge file answers:

What is scientifically correct?

An evaluation framework answers:

How do we determine whether an AI response is correct?

A prompt template answers:

How do we ask the AI to perform the task?

These should work together without unnecessarily duplicating one another.

Physics Knowledge
       ↓
Prompt Template
       ↓
AI Response
       ↓
Evaluation Criteria
       ↓
Quality Judgment
30. Human SME Review Remains Important

AI-generated Physics content should not automatically be treated as authoritative.

Human subject-matter review remains important when:

Accuracy is critical.
The concept is advanced.
The response contains uncertainty.
The output will be used for education.
The AI response conflicts with trusted sources.
The task involves subtle conceptual distinctions.

The role of AI is to assist the SME—not eliminate the need for expertise.

31. Recommended Physics AI Workflow

For important Physics AI tasks, use the following workflow:

1. Define the Task
        ↓
2. Identify the Learner / User
        ↓
3. Gather Relevant Knowledge
        ↓
4. Identify Constraints
        ↓
5. Design the Prompt
        ↓
6. Generate the AI Response
        ↓
7. Check Physics Accuracy
        ↓
8. Check Mathematical Accuracy
        ↓
9. Check Units and Assumptions
        ↓
10. Check Misconceptions
        ↓
11. Evaluate Educational Quality
        ↓
12. Refine the Prompt or Response
        ↓
13. Record the Final Result

This workflow can be adapted according to task complexity.

32. Quality Checklist

Before accepting a Physics AI output, ask:

Physics
 Are the facts correct?
 Are the concepts represented accurately?
 Are the equations valid?
 Are assumptions appropriate?
 Are units correct?
 Are calculations correct?
 Are vector/scalar distinctions handled correctly?
Reasoning
 Is the reasoning logically sound?
 Are important steps justified?
 Are missing information and assumptions identified?
 Is the conclusion supported by the reasoning?
Education
 Is the explanation appropriate for the learner?
 Are common misconceptions addressed?
 Is the explanation clear?
 Does it promote conceptual understanding?
AI Reliability
 Is the response grounded in relevant knowledge?
 Does it avoid unsupported claims?
 Does it avoid fabricated information?
 Is meaningful uncertainty acknowledged?
Output
 Does it follow the requested format?
 Does it answer the actual task?
 Is it concise enough for the intended purpose?
 Can the result be reused or evaluated consistently?
33. Anti-Patterns to Avoid

The following practices should generally be avoided.

"Just Ask the AI"

Using a vague prompt and accepting the first response without evaluation.

"Fluency Equals Correctness"

Assuming a confident and well-written answer must be scientifically correct.

"Formula Dumping"

Providing equations without explaining their physical meaning or conditions of use.

"Inventing Missing Data"

Creating values or assumptions that were never provided.

"One Prompt Fits Everything"

Using the same prompting strategy for every Physics task.

"No Evaluation"

Generating AI content without checking its accuracy.

"No Learner Context"

Giving the same explanation regardless of grade level or prior knowledge.

"Overcomplicated Prompting"

Using unnecessarily complex prompt structures for simple tasks.

34. Practical Principle

The central principle of this knowledge base is:

Do not ask only whether the AI can produce an answer. Ask whether the answer is scientifically correct, appropriately reasoned, educationally useful, and supported by the available information.

35. Relationship to the Physics AI Knowledge Base

This document provides general practices.

Individual Physics knowledge units provide topic-specific information.

Physics-AI-Best-Practices.md
        │
        ├── General AI principles
        ├── Evaluation principles
        ├── Prompting principles
        └── Reliability principles
                 │
                 ▼
        Physics Knowledge Units
                 │
                 ├── Motion
                 ├── Newton's Laws
                 ├── Momentum
                 ├── Work & Energy
                 └── Electricity

The global practices should not be duplicated unnecessarily inside every lesson file.

36. Continuous Improvement

This document should evolve as the project develops.

New practices may be added based on:

AI evaluation experiments
Physics SME review
Prompt testing
Model behavior
RAG experiments
Error analysis
Educational use cases
Lessons learned from practical projects

Each new practice should have a clear reason for inclusion and should be consistent with the overall goals of the knowledge base.

Version

Version: 1.0
Status: Active Development
Last Updated: August 2026

Author

Muhammad Shakhawat Hossain

M.Sc. in Physics | Physics Educator | Prompt Engineering | Generative AI | AI Evaluation

GitHub: https://github.com/bdshakhawat
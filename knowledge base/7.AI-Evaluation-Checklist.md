knowledge-base/07-AI-Evaluation-Checklist.md

# AI Evaluation Checklist

> A practical framework for evaluating AI-generated outputs for accuracy, relevance, instruction-following, consistency, reliability, and task-specific quality.

---

## Purpose

The purpose of this checklist is to provide a systematic method for evaluating AI-generated outputs rather than accepting an answer simply because it sounds fluent, confident, or well-written.

This framework is designed for:

- Prompt Engineering experiments
- LLM output evaluation
- AI training and data-quality workflows
- Prompt refinement
- Few-shot example development
- Synthetic example validation
- Generative AI applications
- Physics AI and educational AI evaluation

The central principle is:

> **Evaluate the output against explicit criteria and the information available to the model—not against how convincing the answer sounds.**

---

# 1. Evaluation Workflow

Use the following sequence when evaluating an AI response:

```text
Task & Intent
      ↓
Input / Context
      ↓
Instruction Following
      ↓
Accuracy
      ↓
Reasoning / Logic
      ↓
Completeness
      ↓
Relevance
      ↓
Format & Style
      ↓
Unsupported Claims
      ↓
Overall Quality
      ↓
Refinement
==========================================================================================================
2. Step 1 — Task Understanding

Before evaluating the AI output, identify exactly what the prompt asked the model to do.

Checklist
 Is the intended task clear?
 What is the expected outcome?
 Is the target audience specified?
 Are there explicit constraints?
 Is a particular format required?
 Are examples provided?
 Is source information provided?
 Are there specific evaluation criteria?
Evaluation Principle

Do not evaluate an answer against requirements that were never part of the original task.

3. Step 2 — Input and Context Fidelity

Check whether the AI correctly used the information provided in the prompt.

Checklist
 Did the response use the relevant input?
 Did it preserve important facts?
 Did it misunderstand any provided information?
 Did it ignore important context?
 Did it introduce information that was not provided?
 Did it change the meaning of the original information?
Important

If the prompt explicitly says:

"Base your answer only on the information provided."

then unsupported additions should be treated as a significant evaluation issue.

4. Step 3 — Instruction Following

Determine whether the AI followed the instructions in the prompt.

Checklist
 Completed the requested task
 Followed the requested sequence
 Followed explicit constraints
 Used the requested tone
 Used the requested audience level
 Included all required components
 Avoided prohibited components
 Followed the requested output format
Example

If a prompt says:

"Provide exactly three recommendations."

and the AI provides seven, the response has an instruction-following problem even if all seven recommendations are useful.

5. Step 4 — Accuracy

Evaluate whether the content of the response is correct.

Accuracy depends on the task.

For a factual task:

Are the facts correct?

For a mathematical task:

Are the calculations correct?

For a Physics task:

Are the scientific concepts and relationships correct?

For a transformation task:

Was the original information preserved accurately?
Checklist
 No factual errors
 No incorrect calculations
 No incorrect interpretations
 No contradictions
 Claims are supported by the available information
6. Step 5 — Reasoning and Logic

Evaluate whether the conclusions follow logically from the information and instructions.

Checklist
 Reasoning is internally consistent
 Conclusions follow from available evidence
 Important logical steps are not missing
 No unsupported leap in reasoning
 Cause and effect are not confused
 Alternatives are considered when required
 Assumptions are identified when relevant
Important Principle

A long explanation is not necessarily good reasoning.

The goal is:

Relevant, logically sound reasoning appropriate to the task.

7. Step 6 — Assumptions and Information Gaps

AI systems may fill missing information with assumptions.

Evaluate whether those assumptions are appropriate and clearly identified.

Checklist
 Are important assumptions stated?
 Are assumptions reasonable?
 Does the answer distinguish assumptions from facts?
 Does the response identify important information gaps?
 Does it avoid inventing missing information?
Example

If a Physics problem does not provide air resistance information, the response might state:

"Assuming air resistance is negligible..."

rather than silently treating that condition as a given fact.

8. Step 7 — Hallucination and Unsupported Claims

Check whether the AI generated information that is unsupported, fabricated, or inconsistent with the available context.

Look for:
Invented facts
Fabricated sources
Made-up statistics
Unsupported numerical values
Nonexistent references
False quotations
Invented features
Unsupported claims of certainty
Checklist
 No fabricated information
 No invented sources
 No unsupported numerical claims
 No false attribution
 No unsupported certainty

A response can be fluent and still contain hallucinations.

9. Step 8 — Completeness

Determine whether the response sufficiently addresses the task.

Checklist
 All major requirements are addressed
 Important information is not omitted
 Required examples are included
 Required analysis is complete
 The response does not stop before completing the task
Important Distinction

Completeness does not mean unnecessary length.

A concise response can be complete if it satisfies the task requirements.

10. Step 9 — Relevance

Evaluate whether the response stays focused on the actual task.

Checklist
 Directly addresses the user's request
 Includes relevant information
 Avoids unnecessary tangents
 Does not answer a different question
 Does not add irrelevant background
Rating
Rating	Description
High	Directly focused on the task
Medium	Mostly relevant with some unnecessary material
Low	Partially relevant
Failure	Does not meaningfully address the task
11. Step 10 — Clarity

Evaluate whether the output is understandable to its intended audience.

Checklist
 Clear language
 Logical organization
 Appropriate terminology
 No unnecessary ambiguity
 Ideas are easy to follow
 Important distinctions are clearly explained

Clarity should always be evaluated relative to the intended audience.

12. Step 11 — Tone and Persona

When the prompt specifies a particular tone or persona, evaluate whether the response actually reflects it.

Possible dimensions
Professional
Academic
Conversational
Friendly
Concise
Persuasive
Student-friendly
Expert-level
Formal
Checklist
 Tone matches the instructions
 Persona is maintained consistently
 Language is appropriate for the audience
 Style does not contradict the requested voice
13. Step 12 — Output Structure and Formatting

Check whether the response follows the requested structure.

Checklist
 Required headings included
 Required sections included
 Required table included
 Required list included
 Required labels used
 Requested Markdown format followed
 Requested word or character limit respected
Example

If the prompt requests:

Summary
Analysis
Recommendations

the response should preserve that structure unless the task explicitly allows another format.

14. Step 13 — Consistency

Evaluate whether the response is internally consistent.

Checklist
 No contradictions between sections
 Terminology is used consistently
 Numerical values remain consistent
 Conclusions match the analysis
 Recommendations match the identified problems
Example

If the response says:

"The plan has no significant budget risk."

but later identifies an unspecified budget as its largest risk, the response contains an internal inconsistency.

15. Step 14 — Source and Grounding

When a task provides source material, evaluate whether the output remains grounded in that material.

Checklist
 Relevant source information is used
 Source information is represented accurately
 Important claims can be traced to the source
 Unsupported additions are identified
 The response does not contradict the supplied source
Grounding Principle

When the prompt requires source-based analysis:

The source should constrain the answer.

16. Step 15 — Domain Accuracy

For specialized tasks, add domain-specific criteria.

For Physics AI, evaluate:

Physics Accuracy
 Concepts are scientifically correct
 Laws and principles are correctly applied
 Equations are appropriate
 Units are correct
 Calculations are correct
 Assumptions are physically reasonable
 Common misconceptions are not reinforced
Educational Accuracy
 Explanation matches the learner's level
 Technical terms are appropriate
 Conceptual understanding is supported
 Examples are scientifically valid

This domain layer can be adapted for other subject areas.

17. Step 16 — Example Quality

When evaluating few-shot prompts or synthetic examples, evaluate the examples themselves.

Checklist
 Examples are correct
 Examples clearly demonstrate the intended behavior
 Input and Output are properly paired
 Examples are representative
 Examples are sufficiently diverse
 Examples do not contain accidental contradictions
 Examples do not teach undesirable patterns
 Examples reflect the stated preferences
Important Principle

Bad examples can teach bad behavior.

Few-shot examples should therefore be evaluated as carefully as final outputs.

18. Step 17 — Preference Alignment

When a prompt contains explicit preferences, evaluate whether the response satisfies them.

For example:

Preference:
Clear and concise

Output:
Long, repetitive, and highly technical

The response may be factually correct but still fail the preference requirement.

Checklist
 Required preferences are satisfied
 Conflicting preferences are identified
 Style matches the intended use
 Output reflects the refined examples
19. Error Severity

Not every error has the same importance.

Classify errors using the following levels:

Severity	Meaning
Critical	Fundamental failure that makes the output unusable or seriously misleading
Major	Significant error affecting correctness or task completion
Moderate	Meaningful problem that requires correction
Minor	Small issue with limited effect
Cosmetic	Presentation issue with no substantive effect
Examples

Critical

Fabricated central information
Fundamentally incorrect Physics
Completely fails the requested task

Major

Incorrect conclusion
Important instruction ignored
Significant hallucination

Moderate

Missing important requirement
Incorrect but localized reasoning
Important formatting failure

Minor

Small wording issue
Minor formatting problem
Slightly incomplete explanation

Cosmetic

Minor punctuation issue
Non-substantive stylistic difference
20. Overall Evaluation Rating

After evaluating the individual dimensions, assign an overall judgment.

Excellent

The response:

Is accurate
Follows instructions
Is relevant
Is well structured
Contains no meaningful unsupported claims
Meets the intended quality standard
Good

The response is fundamentally correct and useful but contains minor issues that could be refined.

Needs Improvement

The response has meaningful weaknesses that should be corrected before use.

Fail

The response contains major or critical problems and should not be accepted without substantial revision.

21. Suggested Scoring Framework

A numerical score can be useful when comparing multiple AI outputs.

Use a 0–4 scale:

Score	Meaning
4	Excellent
3	Good
2	Needs Improvement
1	Poor
0	Missing / Incorrect
Core Evaluation Dimensions
Dimension	Score
Task Understanding	/4
Input / Context Fidelity	/4
Instruction Following	/4
Accuracy	/4
Reasoning / Logic	/4
Assumption Handling	/4
Hallucination Control	/4
Completeness	/4
Relevance	/4
Clarity	/4
Format / Structure	/4
Consistency	/4

Maximum: 48 points

For domain-specific tasks, additional criteria can be added.

22. Score Interpretation

The following ranges provide a practical starting point:

Score	Interpretation
44–48	Excellent
38–43	Strong
30–37	Acceptable / Needs Minor Revision
20–29	Needs Significant Improvement
0–19	Poor / Fail

These thresholds are not universal standards. They should be refined when the rubric is tested against real evaluation data.

23. Evidence-Based Evaluation

A score alone is not sufficient.

Important judgments should be supported by evidence.

Use:

Criterion:
[Name of criterion]

Score:
[0–4]

Evidence:
[Specific part of the response supporting the judgment]

Issue:
[What is wrong or missing]

Recommended Improvement:
[What should change]
Example
Criterion:
Instruction Following

Score:
2/4

Evidence:
The prompt requested exactly three recommendations, but the response provided six.

Issue:
The numerical constraint was not followed.

Recommended Improvement:
Limit the output to the three highest-value recommendations.

This makes evaluation more transparent and reproducible.

24. Evaluation Record Template

Use the following template when evaluating an AI output.

# AI Output Evaluation

## Task

[Describe the original task]

## Overall Rating

[Excellent / Good / Needs Improvement / Fail]

## Scores

| Criterion | Score |
|---|---:|
| Task Understanding | /4 |
| Input / Context Fidelity | /4 |
| Instruction Following | /4 |
| Accuracy | /4 |
| Reasoning / Logic | /4 |
| Assumption Handling | /4 |
| Hallucination Control | /4 |
| Completeness | /4 |
| Relevance | /4 |
| Clarity | /4 |
| Format / Structure | /4 |
| Consistency | /4 |

**Total: __/48**

## Strengths

- ...
- ...

## Issues

### Critical

- ...

### Major

- ...

### Moderate

- ...

### Minor

- ...

## Evidence

- ...

## Recommended Improvement

- ...

## Final Judgment

[Accept / Revise / Reject]
25. Prompt Refinement Through Evaluation

Evaluation should not be the end of the process.

Use evaluation results to improve the prompt.

Prompt
  ↓
AI Output
  ↓
Evaluation
  ↓
Identify Failure
  ↓
Modify Prompt
  ↓
Test Again
  ↓
Compare Results

This creates an iterative Prompt Engineering cycle.

26. Common Evaluation Mistakes

Avoid the following mistakes.

Mistake 1 — Fluency Bias

Assuming a well-written response must be correct.

Mistake 2 — Length Bias

Assuming a longer response is better.

Mistake 3 — First-Answer Bias

Accepting the first plausible output without evaluation.

Mistake 4 — Ignoring Instructions

Evaluating content quality while ignoring whether the model followed the prompt.

Mistake 5 — Ignoring Context

Judging the response without checking the information provided to the model.

Mistake 6 — Ignoring Hallucinations

Accepting plausible-sounding information without checking whether it is supported.

Mistake 7 — Over-Penalizing Style

Treating personal stylistic preferences as factual errors.

Mistake 8 — Under-Penalizing Domain Errors

Treating serious scientific or mathematical errors as minor wording problems.

27. Evaluation Principles for Prompt Engineering

The following principles should guide evaluations throughout this playbook:

Principle 1 — Evaluate Against the Task

The prompt defines the intended behavior.

Principle 2 — Separate Accuracy from Style

A response can be beautifully written and factually wrong.

Principle 3 — Separate Facts from Assumptions

Important assumptions should be visible.

Principle 4 — Require Evidence for Important Judgments

Evaluation should be explainable.

Principle 5 — Use Consistent Criteria

The same standard should be applied across comparable outputs.

Principle 6 — Adapt Evaluation to the Task

A Physics problem, marketing copy, taxonomy, and RAG response require different domain-specific checks.

Principle 7 — Use Evaluation to Improve Prompts

Evaluation should feed back into prompt refinement.

28. Relationship to the Prompt Engineering Playbook

This checklist is one component of the broader knowledge base.

AI Glossary
     ↓
Prompt Engineering Techniques
     ↓
Prompt Patterns
     ↓
Prompt Templates
     ↓
Best Practices
     ↓
Hallucination Mitigation
     ↓
AI Evaluation
     ↓
Prompt Refinement

The purpose of this file is not to replace the other resources.

Instead:

AI-Glossary.md defines important terminology.
Prompt-Engineering-Techniques.md documents techniques.
Prompt-Patterns-Library.md organizes reusable patterns.
Physics-Prompt-Templates.md provides practical Physics applications.
Physics-AI-Best-Practices.md defines recommended practices.
Hallucination-Mitigation.md focuses on reducing unsupported AI output.
AI-Evaluation-Checklist.md provides a structured method for judging results.
29. Future Development

This checklist can later be extended into:

Prompt evaluation datasets
Physics AI benchmarks
Human evaluation guidelines
LLM-as-judge experiments
Automated evaluation prompts
Error classification datasets
Few-shot example validation
RAG evaluation
Prompt comparison experiments
AI training data quality checks

Any automated evaluation system should be tested against appropriate human or SME judgments before being treated as authoritative.

30. Final Principle

The most important principle of this checklist is:

Do not evaluate an AI response by how convincing it sounds. Evaluate whether it correctly performs the requested task, uses the available information appropriately, follows the instructions, avoids unsupported claims, and meets the quality criteria relevant to the task.

A strong AI evaluation is:

Task-Aware + Evidence-Based + Consistent + Domain-Appropriate + Reproducible

Version

Version: 1.0
Status: Active Development
Last Updated: August 2026

Author

Muhammad Shakhawat Hossain

M.Sc. in Physics | Physics Educator | Prompt Engineering | Generative AI | AI Evaluation


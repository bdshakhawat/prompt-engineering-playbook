# Prompt Engineering Case Study

## Lesson 01
### Why Getting Generative AI to Write Like You is a Hard Prompt Engineering Task

---

# Objective

The objective of this case study is to demonstrate how insufficient prompt design leads to poor AI-generated content and how prompt engineering techniques can significantly improve the quality, accuracy, and authenticity of AI outputs.

This exercise follows the example presented in the lecture and extends it with professional prompt engineering analysis.

---

# Case Study 1 — The Original Prompt

## Original Prompt

> "I need to write an email to my colleagues at Vanderbilt explaining that we are launching a new prompt engineering class on Coursera that our graduate students might take."

---

## AI Output (Observed Problems)

The AI generated an email that included:

- Subject: **Exciting opportunity for graduate students**
- Opening sentence: **I'm thrilled to announce...**
- Invented statements such as:
  - Comprehensive curriculum
  - Expert instructors
  - Flexible learning experience

Although the email was grammatically correct, it failed to accurately represent the author's writing style and introduced information that had never been provided.

---

# Root Cause Analysis

| Problem | Root Cause |
|----------|------------|
| Overly enthusiastic tone | No instructions describing the author's writing style or preferred tone. |
| Generic marketing language | The model defaulted to statistically common announcement emails. |
| Hallucinated course details | Insufficient factual context encouraged the model to invent missing information. |
| Weak personalization | No writing persona or writing samples were provided. |
| Lack of audience awareness | The prompt identified "colleagues" but did not specify the expected professional communication style. |

---

# Engineering Diagnosis

The poor output was **not caused by limitations of the AI model**.

Instead, it resulted from an under-specified prompt.

The model attempted to predict missing information based on common patterns found in similar announcement emails.

This illustrates one of the fundamental principles of prompt engineering:

> **Poor prompts create uncertainty, and uncertainty often leads to generic responses and hallucinations.**

---

# Improved Prompt

> Write a concise, professional email to my colleagues at Vanderbilt.

> Use a calm, matter-of-fact tone.

> Avoid promotional language such as "I'm thrilled to announce" or similar marketing expressions.

> Only include the following verified facts:

> • We are launching a new Prompt Engineering course on Coursera.

> • The course is intended for graduate students.

> • The course is currently under development.

> • Curriculum details have not yet been finalized.

> Do not invent additional information.

> If information is missing, leave it out rather than guessing.

> End with a simple next step encouraging colleagues to contact me directly if they have questions.

---

# Prompt Engineering Techniques Applied

This improved prompt intentionally combines multiple prompt engineering techniques.

| Technique | Purpose |
|-----------|---------|
| Context Injection | Provides accurate factual information. |
| Constraint Prompting | Prevents invented content. |
| Hallucination Mitigation | Explicitly instructs the model not to guess missing information. |
| Style Conditioning | Defines the desired writing style. |
| Tone Control | Prevents promotional language. |
| Audience Conditioning | Specifies that the readers are professional colleagues. |
| Output Specification | Defines the desired ending and overall structure. |

---

# Output Evaluation

| Evaluation Criterion | Original Prompt | Improved Prompt |
|----------------------|----------------|-----------------|
| Tone Match | Poor | Excellent |
| Writing Style | Generic | Authentic |
| Hallucination Risk | High | Very Low |
| Factual Accuracy | Low | High |
| Audience Appropriateness | Moderate | Excellent |
| Professionalism | Moderate | High |
| Reader Trust | Low | High |

---

# Physics AI Application

This lesson has significant implications for AI-assisted Physics education.

Suppose the prompt simply states:

> Explain Newton's Second Law.

The AI is likely to produce a generic textbook explanation.

A better educational prompt would specify:

- Target audience (e.g., HSC students)
- Learning objective
- Mathematical level
- Common misconceptions
- Required real-life examples
- Desired lesson structure
- Assessment questions

For example:

> Explain Newton's Second Law to an HSC Physics student.

> Begin with an everyday example.

> Introduce the concept before presenting the equation.

> Include a free-body diagram description.

> Explain two common misconceptions.

> Finish with one worked numerical example and two conceptual questions.

Providing educational context dramatically improves the usefulness of AI-generated instructional content.

---

# Best Practices

When designing prompts for educational writing:

- Clearly define the audience.
- Specify the desired writing style.
- Provide sufficient factual context.
- State explicit constraints.
- Prevent hallucinations whenever factual accuracy matters.
- Define the expected output structure.
- Revise prompts iteratively based on AI responses.

---

# Future Improvements

As I continue this specialization, I plan to improve this prompt further by incorporating:

- Writing Personas
- Example-Based Prompting
- Few-Shot Prompting
- Prompt Patterns
- Structured Output Formatting
- Self-Evaluation Prompts
- Prompt Chaining

This exercise will serve as a baseline for comparing increasingly sophisticated prompt engineering techniques throughout the course.

---

# Key Takeaways

This exercise reinforced several important prompt engineering principles:

- High-quality outputs require high-quality prompts.
- AI cannot accurately reproduce an author's voice without explicit guidance.
- Hallucinations often result from insufficient context rather than model failure.
- Prompt engineering is an iterative design process rather than a one-time instruction.
- Small improvements in prompt design can significantly improve reliability, accuracy, and writing quality.

---

# Personal Insight

This exercise changed the way I think about prompt engineering.

Previously, I believed that improving AI outputs mainly involved experimenting with better wording.

I now understand that effective prompt engineering is a systematic process of defining objectives, context, audience, constraints, writing style, and factual boundaries.

As an aspiring **Physics AI Subject Matter Expert**, I see prompt engineering as a core professional skill for developing trustworthy AI-assisted educational systems.

Rather than asking AI to "write better," I must learn to engineer prompts that enable the model to produce accurate, consistent, and context-aware educational content.
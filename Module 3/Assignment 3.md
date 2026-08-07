Question 1:
Create a prompt that uses a social media post/comments, set of survey responses, or other data cluster data and enrich the clustering with a hierarchy. You can tell the model to create a "taxonomy as an ASCII tree" to help make this happen. Your prompt should include the data being analyzed. 

Now, remove the source data from your prompt so that it is a template that you can reuse to perform the same task. Make sure that there is none of your original data that was analyzed in the template. Copy/paste your template in as the answer.
========================================================================================================================================

Final answer:
You are an expert qualitative research analyst specializing in thematic analysis and hierarchical taxonomy design.

I will provide a qualitative dataset (such as survey responses, customer feedback, social media comments, reviews, or discussion posts).

Your task is to organize the data into a hierarchical taxonomy by progressively grouping related responses into increasingly broader categories.

Instructions:

1. Identify the smallest meaningful clusters of related responses.
2. Merge similar clusters into broader themes.
3. Continue grouping until a clear hierarchical taxonomy emerges.
4. Present the taxonomy as an ASCII tree.
5. For each node in the tree, include the number of responses assigned to that category.
6. Place responses that do not naturally belong in any category under an "Unclassified" branch rather than forcing them into an existing category.
7. Explain any category containing fewer than two responses and indicate whether it represents a meaningful niche or possible noise.
8. Base every category only on patterns found in the data. Do not invent themes that are unsupported by the dataset.

OUTPUT FORMAT

Summary

ASCII Taxonomy Tree

Category Explanations

Rare Categories

Unclassified Items

DATA TO ANALYZE:

[Insert survey responses, social media posts/comments, or other qualitative data here]

========================================================================================================================================

Discussion to understand the question:
This is an excellent question. I can also see **exactly where your confusion comes from**. The assignment wording is a little tricky because it actually asks you to do **two different things**, but only **submit one**.

If I were Dr. Jules White grading this assignment, here's how I would think about it.


# Step 1: Let's break the question into pieces

The assignment says:

> **Create a prompt that uses a social media post/comments, set of survey responses, or other clustered data and enrich the clustering with a hierarchy.**

This is **Task A**.

It means:

You must first create a prompt that **contains actual data**.

For example:

```
Survey Responses

1....
2....
3....
```

or

```
Tweets

Tweet 1...
Tweet 2...


The AI should analyze that data and organize it into a hierarchy.

Example output:


Learning Issues
│
├── Conceptual Confusion
│   ├── Momentum
│   └── Force
│
├── Teaching Pace
│
└── Labs

The instructor even suggests

> taxonomy as an ASCII tree

Then the assignment says:

> Now, remove the source data from your prompt so that it is a template that you can reuse...

This is Task B.

It means

Take your first prompt

↓

Delete the actual survey responses

↓

Replace them with


DATA TO ANALYZE

[Insert data here]

Now it becomes reusable.

Finally it says

> Copy/paste your template in as the answer.

This is the important sentence.

It means

You do not submit Task A.

You only submit the reusable template (Task B).

# Therefore...

Task B: 
Pros

✔ Data removed

✔ Reusable

✔ Generic

✔ Works for

* surveys

* social media

* comments

* reviews

✔ Exactly follows the instructions

This is the one to submit.

> I have a qualitative dataset...
I would instead give the model a role.

For example:
You are an expert qualitative research analyst specializing in thematic analysis and taxonomy construction.
This is consistent with everything you've been learning in the course.

Then I would improve one more thing.
Instead of saying
Identify recurring themes.
I'd say
Identify the smallest meaningful clusters first.

Then merge related clusters into broader themes.

Finally organize those themes into a hierarchical taxonomy.
```

Why?

Because

The assignment says

> enrich the clustering with hierarchy

That means

cluster

↓

merge

↓

hierarchy

not simply

themes

↓

subthemes

The hierarchy should emerge from the clusters.



# Real life Analogy:

Suppose we have: 
Apple
Banana
Orange
Dog
Cat
Lion
```

A normal clustering prompt gives


Fruit

Animals

That's clustering.

But hierarchical clustering gives
Living Things

├── Plants
│    └── Fruits
│          ├── Apple
│          ├── Banana
│          └── Orange
│
└── Animals
     ├── Pets
     │     ├── Dog
     │     └── Cat
     │
     └── Wild Animals
           └── Lion
Notice

It creates

cluster

↓

cluster of clusters

↓

tree

That is

hierarchical clustering

# My version (10/10)

I'd submit something like this:

text
You are an expert qualitative research analyst specializing in thematic analysis and hierarchical taxonomy design.

I will provide a qualitative dataset (such as survey responses, customer feedback, social media comments, reviews, or discussion posts).

Your task is to organize the data into a hierarchical taxonomy by progressively grouping related responses into increasingly broader categories.

Instructions:

1. Identify the smallest meaningful clusters of related responses.
2. Merge similar clusters into broader themes.
3. Continue grouping until a clear hierarchical taxonomy emerges.
4. Present the taxonomy as an ASCII tree.
5. For each node in the tree, include the number of responses assigned to that category.
6. Place responses that do not naturally belong in any category under an "Unclassified" branch rather than forcing them into an existing category.
7. Explain any category containing fewer than two responses and indicate whether it represents a meaningful niche or possible noise.
8. Base every category only on patterns found in the data. Do not invent themes that are unsupported by the dataset.

OUTPUT FORMAT

Summary

ASCII Taxonomy Tree

Category Explanations

Rare Categories

Unclassified Items

DATA TO ANALYZE:

[Insert survey responses, social media posts/comments, or other qualitative data here]
========================================================================================================================================
Assignment question 2: Create a prompt that uses a social media posts/comments, set of survey responses, or other data to predict who else might be interested in your thoughts. 

Now, remove the source data from your prompt so that it is a template that you can reuse to perform the same task. Make sure that there is none of your original data that was analyzed in the template. Copy/paste your template in as the answer.
========================================================================================================================================

Answer of question 2:
You are an expert audience research and content strategy analyst. I will provide a collection of social media posts, comments, survey responses, blog posts, or other written content.

Your task is to analyze the content and predict which additional audience segments—beyond the current audience—would be most likely to find these ideas valuable or engaging.

Instructions:

1. Identify the recurring themes, topics, writing style, tone, and underlying perspectives present across the content.

2. Based only on patterns found in the content, identify 4–6 specific audience segments that are likely to be interested.

For each audience segment provide:
- Audience Segment Name
- Why this audience would be interested
- Which themes, topics, or writing characteristics support this prediction
- Confidence Level (High / Medium / Low)

3. Identify the ONE audience segment most likely to become long-term, highly engaged followers and explain why.

4. Clearly identify any prediction that depends on assumptions rather than direct evidence from the content.

5. Do not invent themes, demographic characteristics, or interests that are not reasonably supported by the provided content.

Output Format:

Content Summary:
Audience Segment 1
- Name
- Evidence
- Reason
- Confidence

Audience Segment 2
…………

Best Long-Term Audience

Assumptions

Content to Analyze:

[Insert social media posts, comments, survey responses, or other qualitative content here]



========================================================================================================================================

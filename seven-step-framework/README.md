# The Seven-Step Framework

A methodology for designing AI systems in high-accountability environments. Developed through two years of iterative testing inside a live broadcast newsroom.

## Why this framework exists

Most prompt engineering guides focus on what to write. This framework focuses on how to think before you write. It came out of a specific problem: AI systems that work in demos but fail in production — especially in domains where errors carry legal, ethical, or reputational weight.

The seven steps are not academic. They emerged from cataloging failures, finding patterns, and building structures that prevented those failures from recurring.

## The Seven Steps

### 1. Define the pain

Before writing a single instruction, name the specific failure you are trying to prevent. Not "improve output quality" — that is a slogan, not a problem. Pain has to be concrete enough that you can recognize it when you see it again.

Example: "The model confuses 'detained' with 'arrested' in legal coverage. This produces output that violates Turkish press law."

### 2. Write an observable test

Define a test that can answer "is this rule being applied?" with a yes or no. If you cannot test it, you cannot enforce it.

Example: "If the output uses the word 'arrested' for someone who has not been formally indicted, the system has failed."

### 3. Document the misinterpretation

Write down the plausible-sounding wrong reading of your rule. The model will find this misinterpretation on its own — better that you find it first.

Example: "A YouTube video from a verified news channel might look like a primary source. It is not. Verified does not mean primary."

### 4. Draw the scope boundary

State explicitly when the rule does not apply. Without scope, the rule becomes either too rigid or too vague.

Example: "These verification rules apply to news output. They do not apply to fictional writing, brainstorming sessions, or historical analysis."

### 5. Adapt instructions to context

The same rule needs different framing for different platforms, audiences, or use cases. A rule written for one context fails when transplanted unchanged.

Example: A source verification rule for Grok must account for X integration. The same rule for Perplexity must account for citation engine behavior. The intent is identical; the instructions are not.

### 6. Close the abstract-concrete loop

Every abstract rule needs a concrete reason. Every concrete prohibition needs an abstract principle. If you only state the rule, the model will follow it brittlely. If you only state the principle, the model will improvise around it.

Example: "Do not generate SEO metadata blocks. The editor's need is to choose a headline, not to receive a metadata package."

### 7. Define the trigger

State explicitly when this command or rule activates. Without a trigger definition, the system either applies rules everywhere or nowhere predictably.

Example: "This protocol activates when the user types `breaking [topic]` or pastes a URL with `breaking` prefixed."

## How to use this framework

Apply it in order. Skipping steps produces brittle systems.

Most failures in AI system design come from skipping steps 1, 3, and 4. Builders write rules without naming the pain (step 1), without anticipating misreadings (step 3), and without limiting scope (step 4). These three steps prevent more failures than any prompt-writing trick.

## Where this came from

This framework was extracted from working on Turkish-language newsroom systems for two years. It started as a checklist. It became a methodology after I noticed I was applying the same seven moves regardless of which system I was building.

The framework is domain-agnostic. It applies to any high-accountability AI deployment — legal tech, medical decision support, financial reporting, journalism. The pain points differ; the design discipline does not.

## Status

This is a working document. The framework will evolve as it is tested in new domains.

---

*Part of [prompt-engineering-for-journalism](../README.md).*

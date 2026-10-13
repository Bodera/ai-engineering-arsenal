# AI Engineering Arsenal

> A personal knowledge base, collection of guidelines, practical frameworks, and behavioral personas for AI-assisted software engineering, reasoning, architecture, and continuous learning.

This repository is not a catalog of AI models or a collection of prompt tricks.

It is a living record of **how I think, learn, build, and use AI as an engineering tool**. The initial motivation is AI-assisted programming: prompts, agents, workflows, model selection, and practical experimentation with tools such as [OpenCode](https://github.com/sst/opencode). Over time, the scope intentionally expands beyond AI into the underlying engineering knowledge that makes those tools useful: logical reasoning, graph thinking, software architecture, programming principles, problem solving, and other concepts I learn and turn into reusable practice.

## Philosophy

AI should amplify engineering judgment, not replace it.

This repository exists to capture the ideas, rules of thumb, mental models, experiments, and working methods that help me:

- reason about problems before reaching for implementation;
- use AI deliberately instead of delegating understanding;
- turn recurring problems into repeatable workflows;
- connect concepts across software engineering disciplines;
- document lessons learned while they are still fresh;
- continuously refine my own way of working.

The repository is intentionally **evolutionary**. Some entries will begin as rough notes, then become guidelines, frameworks, personas, experiments, or principles as they mature.

## Structure

### [`guidelines/`](./guidelines)

Practical rules and recommendations for how I work.

Examples: AI interaction guidelines, code review practices, debugging habits, agent usage, prompt design, tool selection, and engineering heuristics.

### [`frameworks/`](./frameworks)

Reusable ways of thinking and structured approaches to solving classes of problems.

Examples: decision frameworks, problem-solving workflows, reasoning methods, architecture analysis, investigation processes, and AI-assisted development workflows.

### [`knowledge-base/`](./knowledge-base)

The underlying knowledge and concepts I am studying or consolidating.

Examples: logical reasoning, graph theory, software architecture, programming principles, networking, distributed systems, and other foundations that strengthen engineering judgment.

### [`personas/`](./personas)

Reusable behavioral profiles that shape how an AI model approaches a task: the principles it prioritizes, how it handles uncertainty, what it pays attention to, and how it presents its conclusions. This section is tool-agnostic: the same persona definition can be adapted to different agents and model providers.

Personas are not a substitute for a clear task, project constraints, source verification, or human judgment. They are a behavioral lens, not a guarantee of correctness.

## How this evolves

A piece of knowledge does not have to start as a polished framework. A common path is:

`observation → notes → experiment → insight → guideline / framework / persona`

The repository should preserve that evolution rather than hide it. Personas, like the rest of this material, are living documents: revise them when testing reveals ambiguity, unwanted behavior, or a better interpretation of their foundations.

## Current AI context

My current development environment is Linux/Fedora, and I have experimented with several AI agents and coding workflows. At the moment, [OpenCode](https://github.com/sst/opencode) is the main agent I use because it allows me to switch between different model providers and models, including hosted and local models.

The tool is not the centerpiece of this repository. The centerpiece is the **methodology around using the tool well**.

## Influences

My current references and sources of ideas include:

- Fabio Akita
- Karol Attekita
- Tech Leads Club
- documentation, books, experiments, discussions, and my own experience

These are influences, not authorities. Ideas documented here should be tested, challenged, adapted, and occasionally discarded.

## Status

This repository is intentionally growing gradually. Its initial structure established guidelines, frameworks, and a knowledge base. The personas section is a new layer for documenting reusable behavioral lenses before exploring any persona-generation tooling.

The goal is not to accumulate pages. The goal is to turn learning and experience into knowledge that can be retrieved, evaluated, and applied.

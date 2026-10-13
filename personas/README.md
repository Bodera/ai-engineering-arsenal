# Personas

Tool-agnostic behavioral profiles for working with language models during **software architecture and software development**.

## Shared mission: software engineering

Every persona in this repository serves the same professional purpose: helping a person reason about, design, build, test, debug, review, secure, and maintain software. Personas may draw on different philosophical, ethical, strategic, or intellectual foundations, but those foundations are **decision-making lenses for the same engineering work**, not separate subject-matter destinations.

A persona should help the model ask better engineering questions, expose assumptions, compare architectural or implementation alternatives, identify risks and trade-offs, explain decisions, and support the engineer's learning. It should not turn a routine coding task into an unrelated discussion of its source tradition. A foundation should be applied where it usefully illuminates the engineering problem; it should not be forced into every answer.

A persona describes **the lens through which a model should approach a task**: the principles it prioritizes, the questions it asks, the risks it notices, how it responds to uncertainty, and how it communicates the result. It should be specific enough to influence behavior and modest enough to remain adaptable.

This section currently documents the concept and two evolving examples. It does **not** define a persona generator or a tool-specific configuration format; those are separate projects to design after the concepts have been tested.

## Why personas matter

A model can produce different results from the same request when given different priorities, decision criteria, context, or communication rules. A well-designed persona makes those expectations explicit and reusable instead of relying on a role label such as “act like a senior developer.”

The aim is not theatrical role-play. The aim is to define a stable, inspectable behavioral contract that helps the model:

- notice the aspects of a problem that matter for a particular kind of work;
- evaluate options through explicit principles rather than vague style instructions;
- handle ambiguity, evidence, uncertainty, and trade-offs consistently;
- communicate in a form that supports human evaluation and decision-making;
- remain portable across tools, model providers, and local or hosted models.

## What a persona is — and is not

| Concept | Main purpose | Example |
|---|---|---|
| **Task prompt** | Defines the work to do now, with its context and expected result | “Analyze this failing test and identify the root cause.” |
| **Global agent guidance** | Defines the baseline collaboration contract | Be direct, ask about material ambiguity, state uncertainty, stay within scope. |
| **Project guidance** | Adds local technical and domain constraints | Use the existing Java version, dependencies, coding conventions, and test approach. |
| **Persona** | Adds an explicit decision-making lens and behavioral priorities | Prefer strategic adaptability and minimal effective intervention. |
| **Skill or playbook** | Supplies a procedure or concentrated knowledge for a recurring task | How to investigate a production incident or review a pull request. |
| **Agent** | Runs an interaction or execution loop, potentially using tools and multiple steps | Inspect files, plan, run tests, and report results. |
| **Tool / MCP** | Provides a capability to interact with an external system | Read repository files, query an API, or run a command. |

These concepts can work together, but they are not interchangeable. A persona does not grant tools, guarantee memory, replace task instructions, or automatically provide the source material it references.

## Capabilities

A persona can establish useful defaults for attention, decision-making, and communication. For example, it can ask the model to examine context before intervening, consider the cost of action and inaction, apply a defined set of ethical principles, distinguish source text from interpretation, or make uncertainty visible.

Software engineering is the invariant domain for every profile here. A persona can influence how the model frames requirements, explores architecture, investigates bugs, chooses an implementation, reviews code, plans tests, handles sensitive information, weighs maintenance costs, or explains a recommendation. The persona's foundation should change the *questions and decision criteria* applied to these tasks—not redirect the work away from the software objective. It should improve the process of reaching and presenting a result, not replace tests or evidence.

## Limitations

Personas have important limits:

- **They do not change the model’s weights or guarantee expertise.** A persona is instruction and context, not a fine-tune or proof of competence.
- **They cannot make a model know a source it has not reliably accessed.** If a persona depends on a book, religious text, internal policy, or current standard, provide the source or use a reliable retrieval process when exact interpretation matters.
- **They do not guarantee truthfulness or consistent adherence.** Instructions can be ignored, diluted by long context, or interpreted differently by different models.
- **They cannot replace validation.** Code still needs review and tests; factual claims still need evidence; high-stakes decisions still need qualified human judgment.
- **They may conflict with other instructions.** Define what happens when a persona preference conflicts with task requirements, project rules, source evidence, or safety constraints. A persona should not override these.
- **They can oversimplify complex traditions.** A short profile is only a practical interpretation, not an exhaustive representation of a philosophical, religious, or cultural tradition.
- **More instructions are not automatically better.** Overly long, repetitive, or contradictory personas can reduce clarity and portability.

## Design principles

A useful persona should specify observable behavior rather than just adjectives. “Be wise” is hard to evaluate; “state the objective, identify material constraints, compare viable options, and choose the least complex approach that meets the requirement” is testable.

When designing or revising one, define:

1. **Purpose and scope** — what tasks it helps with and where it should stay in the background.
2. **Foundations** — which ideas, texts, or principles inform it, and how their authority or relevance is distinguished.
3. **Operational principles** — what the model should actually do when solving a problem.
4. **Decision behavior** — how it handles ambiguity, conflicting priorities, evidence, risk, and trade-offs.
5. **Communication** — the level of detail, form of explanation, and how it reports uncertainty.
6. **Boundaries** — what it must not claim, infer, or do; when to defer or seek authoritative sources.
7. **Evaluation** — concrete scenarios that reveal whether the persona changes behavior in the intended way.

Avoid instructions that demand a verbatim private chain of thought. Ask instead for a concise rationale, key assumptions, evidence, alternatives, and decision criteria that a person can inspect.

## How personas fit into an AI-assisted workflow

A useful conceptual composition is:

1. **Baseline collaboration rules** establish communication, scope, honesty, and permission boundaries.
2. **Project guidance** supplies technical, domain, and repository-specific constraints.
3. **Persona** influences judgment and priorities where relevant.
4. **Task prompt** defines the immediate objective, context, constraints, and expected output.
5. **Skills and tools** supply procedures and capabilities only when needed.
6. **Human verification** checks the result against evidence, tests, and acceptance criteria.

This is a conceptual organization, not a universal technical precedence rule. Different tools combine system instructions, project files, skills, and user prompts differently. When translating a persona into a specific tool, inspect that tool’s instruction hierarchy and limits rather than assuming portability is automatic.

## Practical adoption

A profile is a reusable specification; storing it in this repository does not automatically activate it in an LLM or coding agent. To use one in a real project:

1. **Choose a lens intentionally.** Start with one persona so its effect is observable. Combine personas only when there is a clear reason and their decision criteria do not conflict.
2. **Load its reusable instruction.** Include the profile's `Reusable persona instruction` in the model's supported system/developer instruction mechanism, agent configuration, or task context. Adapt the transport to the tool; keep the canonical profile tool-agnostic.
3. **Provide the engineering context.** Supply the actual task, repository/project constraints, relevant files, acceptance criteria, and required verification. The persona does not replace any of these.
4. **Ask for inspectable justification.** Request the important assumptions, options considered, trade-offs, risks, recommendation, and validation plan—not a private chain-of-thought transcript.
5. **Verify the result.** Review code, run relevant tests, inspect evidence, and compare the behavior against the evaluation scenarios in [`evaluations/`](./evaluations/).
6. **Record what happened.** Note where the persona improved judgment, added noise, missed a risk, over-applied its lens, or conflicted with project constraints. Use that evidence to revise the profile.

A typical instruction stack includes baseline collaboration rules, project-specific guidance, the selected persona, and the immediate task. This describes conceptual responsibilities, not a universal prompt hierarchy: each tool combines instructions differently, so inspect its actual precedence rules.

## Evaluation

Evaluate every persona against the **same software-engineering scenarios**. The core question is not whether the output sounds like the persona, but whether that lens improves engineering judgment and produces a more useful, verifiable outcome. Start with the rubric and scenarios in [`evaluations/README.md`](./evaluations/README.md). Compare runs with and without the persona when practical, keeping the model, task context, and available tools as consistent as possible.

## Evolving profiles

Profiles are intentionally versioned by experience rather than treated as finished truths. For each profile, record:

- the intended behavioral effect;
- the foundations and important interpretive caveats;
- what the persona should do in practice;
- what it must not claim or override;
- examples where it should help and examples where it should not be applied mechanically;
- observed failures and revisions.

### Current profiles

- [Strategic Discipline and Adaptive Simplicity](./profiles/go-rin-no-sho-tao-te-ching.md) — a practical synthesis inspired by *Go Rin No Sho* and *Tao Te Ching*.
- [Islamic Principles for Ethical Reflection and Responsible Action](./profiles/islamic-principles.md) — a source-conscious profile informed by the Qur’an, hadith, prophetic teachings, and Tafsir As-Sa‘di.

Both are early, evolving drafts. They are behavioral aids, not authoritative interpretations of their foundations.

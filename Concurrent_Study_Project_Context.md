# Concurrent Programming Oral Exam — Agent Handoff Context

## Purpose

This file transfers the context of a Spanish-language conversation to another AI agent. The user is preparing for a **Concurrent Programming (Programación Concurrente) oral exam / colloquium (coloquio)**. They want a concise, accurately grounded study guide that covers historical oral-exam questions without forcing them to jump around between topics.

**Communication:** The user speaks Spanish and prefers explanations and final study material in Spanish. This handoff is in English because the user explicitly requested it. The user values the perspective of an expert concurrent-programming instructor, with **brief, accessible answers** and deeper explanation only when necessary.

## Source files and location

**IMPORTANT: All the following files are expected to live in the same directory as this Markdown file.** Resolve paths **relative to this file**, not by relying on an environment-specific absolute path.

- [`./Preguntero Concurrente.pdf`](./Preguntero%20Concurrente.pdf) — **Primary source and canonical study order.** Contains topic-by-topic answers that the user is already studying. Preserve its sequence, terminology, and concise explanatory style.
- [`./TemasConcurrenteColoquio.pdf`](./TemasConcurrenteColoquio.pdf) — **Coverage checklist / cross-reference source.** Collects historical questions asked by examiners, plus several practical Petri-net examples and observations. Use this to identify omitted questions and underdeveloped answers.
- [`./Preguntero_Concurrente_Ampliado.html`](./Preguntero_Concurrente_Ampliado.html) — **HTML study guide produced during this conversation.** It is intended to combine questions and succinct answers in the original *Preguntero* order, with added missing content and visual examples. This is the main artifact to inspect and improve if asked.

In the original runtime these files were located in `/mnt/data/`. In a different agent environment, locate the **directory containing this Markdown file** and open the three sibling files there. Do not assume `/mnt/data/` exists there.

If other implementation artifacts happen to be alongside these files (e.g. `build_preguntero.py`, `render_preguntero.py`, `preguntero_data.json`), they may help with regeneration, but the three items above are the intended references. Verify their presence rather than assuming them.

## Conversation history and decisions

1. The user first asked for brief beginner-friendly explanations of *interleaving*, reactive systems, event-driven architecture, deadlock, livelock, and starvation, including Petri-net examples. Their preferred style was clearly **short, clear, and educational**.
2. The user uploaded `TemasConcurrenteColoquio.pdf` and `Preguntero Concurrente.pdf` and asked for a comparison: **Which questions/topics from the former are absent from the latter?** The motivation was to use the existing *Preguntero* as the sole main study path while ensuring no historical colloquium topic was overlooked.
3. The assistant produced a comparison: topics absent, topics present but underdeveloped, and topics broadly covered.
4. The user then requested **an HTML file with questions and corresponding answers, following the exact order in `Preguntero Concurrente.pdf`, supplemented with missing topics**, plus **visual examples**. They emphasized **short answers** matching the original handout’s style: do not inflate the document with lengthy prose.
5. The assistant created `Preguntero_Concurrente_Ampliado.html`, and described it as an interactive Spanish study guide with collapsible questions, visual examples, added-topic tags, search/filters, and progress tracking. The previous response reported **77 questions, 21 additions, and 6 sections**; treat these numbers as claims to verify from the current HTML, not as immutable requirements.
6. The current user request is to create this **English-language Markdown handoff context** for another agent, explicitly referencing the PDFs in the same directory so it can independently contrast the sources.

## Coverage gap findings from the initial comparison

These were identified as **absent or not explicitly developed** in the primary *Preguntero* and deserve careful cross-checking against both PDFs:

1. Relationship between **interleavings (execution traces)** and **T-invariants**.
2. **Petri-net liveness** (vivacidad), and its relationship with deadlock and starvation.
3. **Incidence matrices**, including input/output matrices.
4. **Petri-net state equation** and markings reached by firing vectors.
5. **Reachability graph versus marking graph** (grafo de alcanzabilidad vs. grafo de marcado).
6. **Sink places/transitions** (sumideros), where relevant to the course terminology.
7. **Ownership** differences between semaphores and locks.
8. Monitor **condition variables** and `wait`, `signal`, `empty`.
9. The monitor's **courtesy/urgent queue** (cola de cortesía) and its purpose.
10. Rules for deriving the **number of threads from Petri-net T-invariants**, joins and conflicts.
11. Distinction between **formal and informal grammars**.

The following were identified as **present but insufficiently detailed for some colloquium questions**:

- Bounded-buffer producer–consumer: number and initialization of semaphores, acquisition order (space/items before mutex), why that ordering matters, Petri-net representation.
- Petri-net properties: boundedness, safeness, liveness, quasi-liveness/pseudo-liveness, deadlock freedom, conflicts.
- Dining philosophers: full network classifications, starvation, physical interpretations of P- and T-invariants, colored-net simplification.
- Barbershop: constructing/classifying its Petri net, invariants, threads and behavior.
- Monitors: signal-and-continue vs. signal-and-wait vs. signal-and-urgent-wait vs. signal-and-exit, wakeup/condition caveats and queue scheduling.
- Timed Petri nets: strong vs. weak time semantics, and meanings of alpha and beta.
- Race conditions: general definition and illustrative examples.
- P-/T-invariants: how to derive them and what they physically mean.
- Mealy vs. Moore: differences, output timing, relative expressiveness.
- Semaphore vs. lock advantages, disadvantages, fairness and ownership.
- Determinism, real Petri-net conflicts and policies implementing conflict resolution in the coursework project (TP).

These findings are a **starting checklist**, not a substitute for freshly reading both PDFs when a thorough audit is requested.

## Desired content organization

The existing *Preguntero* starts with basic concurrency and proceeds to other topics. Keep the exact **source order**, inserting new explanations immediately next to the nearest relevant original topic rather than appending a separate grab-bag chapter at the end:

- Atomic operations; interleaving; critical sections; mutual exclusion; testing limitations and modeling; reactive systems; event-driven architectures; deadlock/livelock/starvation.
- Processes vs. threads; Java `start()` vs. `run()`; thread states; scheduling; fairness; locks, semaphores, producer–consumer; concurrency vs. parallelism.
- Mealy/Moore machines; regular expressions; alphabets/languages/grammars; automata, Chomsky hierarchy, Turing machines, linear-bounded automata, pushdown and finite automata, deterministic/non-deterministic models.
- Petri-net invariants; non-autonomous nets; structural classes; nondeterministic conflicts; siphons/traps; Petri-net matrices, state equation, reachability, firing/enabling.
- Monitors, policies and condition queues; barbershop; dining philosophers; temporal semantics, colored Petri nets; producer–consumer Petri net.

This is an **outline**, not an assertion that every item already has an adequate answer. Consult the primary PDF to determine exact ordering and wording.

## Key study-guide design principles

- **Spanish output for the study guide**, despite this English handoff.
- **Question → short answer** structure, ideally one compact paragraph or a few bullets per concept.
- **Preserve the original progression** and the general teaching vocabulary of `Preguntero Concurrente.pdf`.
- **Mark newly inserted content** (the previous guide used an `Agregado` label), so the user can tell which concepts were supplemental.
- **Visual examples** should clarify a concept rather than decorate: small diagrams for interleavings, semaphore ordering, bounded buffers, monitor queues/policies, Petri-net tokens/transitions, conflicts, invariants, reachability, or state equations.
- Include **practical explanations and diagrams** for the three particularly prominent Petri-net case studies: producer–consumer, dining philosophers, and barbershop.
- Avoid walls of text; the user explicitly said not to generate unnecessary text that would make studying harder.
- Preserve useful HTML interaction if editing the existing artifact: collapsible answers, navigation/search, progress marks, and mobile-friendly readability.
- Keep it suitable for preparation for an **oral exam**, including follow-up questions examiners might ask, but do not sacrifice brevity.

## Accuracy and evidence guidelines

The source PDFs reflect class notes and recollections of examiner questions; **not every statement in them is necessarily correct**. If the task is *source-faithful extraction*, distinguish what the PDFs say from external interpretation, and do not silently change their claims. If the user requests a corrected/enhanced study guide, distinguish factual corrections from content added for pedagogical value.

In particular, verify delicate statements rather than repeating them uncritically:

- A **T-invariant** is a nonnegative integer firing-count vector satisfying the incidence matrix equation; such a vector does **not by itself guarantee** the firing sequence is executable from a given marking.
- The **state equation** gives a necessary marking relation, but nonnegative results alone do **not generally prove reachability**.
- The exact meaning of **strong versus weak timed-Petri-net semantics** depends on the course's formalism; verify the PDFs and avoid overgeneralizations.
- **Java fairness** and semaphore wakeup order have implementation-specific qualifications; `fair=true` is not an unconditional guarantee of FIFO order under every operation or scheduling scenario.
- **Moore vs. Mealy**: avoid categorical assertions about comparative expressiveness or security without specifying the model and assumptions.
- Petri-net **safeness, liveness, deadlock freedom and invariants** depend on the exact network and initial marking, not just the name of the textbook problem.
- For threaded producer–consumer, blocking on the availability semaphore **before** acquiring the shared-buffer mutex generally prevents holding the mutex while waiting for an item/slot.

Where a visual question depends on a figure embedded in a PDF, inspect the relevant original page, not only its extracted text.

## Useful next tasks for another agent

If asked to **audit or extend the HTML**, the recommended process is:

1. Inspect the existing `Preguntero_Concurrente_Ampliado.html` to identify its current question order, added topics, answer content, styling and diagrams.
2. Read `Preguntero Concurrente.pdf` completely to recover the primary source sequence and baseline explanations.
3. Read `TemasConcurrenteColoquio.pdf` and build a question-by-question coverage map, distinguishing fully covered, partially covered and missing items.
4. Cross-check the HTML against both sources and correct omissions or substantive conceptual errors **without unnecessarily lengthening answers**.
5. Insert missing questions next to related topics and create concise conceptual visuals where they genuinely help.
6. Deliver an updated working self-contained HTML file, and if requested, a separate concise coverage checklist.

If asked to **teach or quiz**, proceed in the primary PDF's order, use short Spanish explanations, and optionally ask oral-style follow-ups. Focus on conceptual understanding and on drawing/analyzing representative Petri nets rather than rote memorization alone.

## Core user intent (one-sentence summary)

> Help a Spanish-speaking concurrent-programming student study every historically asked oral-exam topic **in the familiar order and concise style of `Preguntero Concurrente.pdf`**, using `TemasConcurrenteColoquio.pdf` to fill gaps, with visual examples and an interactive HTML guide that stays easy to navigate.

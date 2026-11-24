---
name: little-red-schoolhouse
description: Write or rewrite prose in the reader-centered style taught by the University of Chicago's Little Red Schoolhouse (Joseph Williams, Gregory Colomb, Larry McEnerney): problem-framed introductions (shared context, destabilizing condition, cost, main point), issue-then-discussion paragraphs, and Williams's sentence principles (characters as subjects, actions as verbs, old before new, stress at the end). Use this whenever the user mentions the Little Red Schoolhouse, LRS, UChicago writing, Williams's "Style" or "Clarity and Grace", "The Craft of Research", McEnerney, or asks to make a document reader-centered, problem-framed, "lead with the problem", "make readers care", "fix the intro so it says why this matters", or to revise a memo, proposal, spec, PR description, ADR, report or paper so its point and stakes come through. Also use it when the user asks for output "in that style" after this style has come up in the conversation.
---

# Little Red Schoolhouse (LRS) style

The Little Red Schoolhouse is the University of Chicago's advanced writing course. Its premise is that
**readers don't read to learn what the writer thinks; they read because something they care about is
unstable, costly or wrong, and they hope the text will help.** Writing is judged by its effect on the
reader, not by how faithfully it records the writer's thinking.

Most drafts are organized the way the writer thought: background, exploration, then the point. An LRS
revision reorganizes the text around the reader's problem, so the reader sees early why to keep reading,
what the writer claims, and where each part fits.

## How to apply it

Work top-down: fix the global structure first, then the paragraphs, then the sentences. Polishing
sentences in a draft whose introduction states no problem is wasted effort.

### 1. Identify the reader and their stake

Before writing, name (to yourself) who reads this and what they care about: a reviewer deciding
whether to merge, an executive deciding whether to fund, a lawyer deciding whether a risk is real.
Everything else depends on this. If the source doesn't make the reader clear, infer the most likely one
from context and state your assumption briefly when you hand back the rewrite.

Ask also whether the reader has to **decide** something: approve a pull request, choose between
options, sign off on a plan, accept a risk. If so, the document exists to support that decision. Name it
in the introduction, list the questions it turns on (for a reviewer, typically "is X ever kept?", "can
Y be bypassed?", "what proves it?"), and order the body by those questions. Then each section answers
one of them, and the reader can tell when they have enough to decide.

### 2. Frame the problem in the introduction

An LRS introduction has up to four moves, in this order:

1. **Shared context** (optional, brief): what the reader already accepts. One or two sentences at most.
   It exists only to set up the instability, so skip it if the instability stands on its own.
2. **Destabilizing condition**: the gap, inconsistency, risk, anomaly or tension. Mark it with words
   that signal instability: *but, however, yet, although, unless, despite, instead*. Without this move
   there's no problem, only a topic.
3. **Cost or consequence**: why the condition matters *to this reader*. What do they lose, risk, pay or
   misunderstand if it stays unresolved? This is the move writers most often leave out, and it's the
   one that makes readers care. Sometimes the cost is the benefit forgone ("we could… but…").
4. **Main point (resolution)**: the claim, recommendation or answer, placed at the **end of the
   introduction**. Make it specific and contestable, a claim a reader could disagree with, not a
   promise to "discuss" or "explore".

Avoid "describe/explain/explore/examine" as the stated purpose. Those verbs promise a topic tour, not a
resolution. Say what the document shows, proposes or decides.

**Break the introduction at the turn.** The four moves are an order, not a single paragraph. Put the
context, instability and cost in one paragraph (two if the cost needs room), then give the main point a
short paragraph of its own. A reader who skims sees the point standing alone instead of buried at the
end of a dense block. As a rough guide, if one introductory paragraph passes about 120 words, split it.

### 3. Structure the body as issue, then discussion

Every section and every substantial paragraph opens with an **issue**: a sentence or two that states
that unit's point and introduces the key terms the rest of the unit will use. Then comes the
discussion: evidence, reasoning, detail.

- Put the point at the **end of the issue**, just before the discussion, mirroring the introduction.
- A reader who reads only the issues (or only the headings plus first sentences) should get the whole
  argument. Use that as your check.
- Keep **thematic key terms** consistent. Introduce them in the issue and repeat them in the
  discussion. Don't swap synonyms for elegance; readers take a new word to mean a new thing.
- Headings, where the format uses them, should state claims or name the issue ("The guard rejects
  opaque origins"), not just label topics ("Origin handling").
- **Notes, warnings and caveats need a cost too.** A maintenance note, a "keep this in sync" box or a
  caveat is an instruction the reader will skip unless it says what goes wrong when they ignore it
  ("If the two drift apart, admins will advise firms on rules the product no longer follows"). Open it
  with the instruction, give the cost, and turn a long inline run of file paths or conditions into a
  list the reader can check against their change.

### 4. Conclude with point and significance

The conclusion restates the main point (in fresh words, not a summary of every section) and then adds
**significance**: what follows from it, what the reader can now do or decide, or what remains open.
Don't introduce a new main claim here, and don't simply recap.

### 5. Revise sentences with Williams's principles

These come from Joseph Williams's *Style: Lessons in Clarity and Grace*:

- **Characters as subjects.** Make the grammatical subject the actor: a person, system, component or
  concept the reader can picture. "The guard rejects the request" beats "Rejection of the request
  occurs."
- **Actions as verbs.** Turn nominalizations back into verbs. "We analyzed" instead of "an analysis was
  performed"; "decide" instead of "make a decision"; "fails" instead of "experiences a failure".
- **Get to the verb quickly.** Short, concrete subjects; no long introductory windup before the main
  verb; don't split subject and verb with a long interruption.
- **Old before new.** Start each sentence with information the reader already has (from the previous
  sentence or the issue) and end it with what's new. This is what makes prose feel cohesive.
- **Stress position.** The end of a sentence gets the most emphasis. Put the important new idea, the
  technical term being introduced, or the consequence there, not a trailing qualifier.
- **Consistent topic strings.** Across a paragraph, keep sentence subjects on the same few characters,
  so the reader can tell what the paragraph is about.
- **Concision.** Cut meaningless words, doubled terms ("each and every"), what readers can infer, and
  metadiscourse that doesn't help the reader navigate ("It is important to note that…").

Passive voice is fine when it puts old information first or keeps a topic string consistent. The rule
is about who the reader sees acting, not a ban on the passive.

## Integrity rules

- **Don't invent stakes or facts.** If the source doesn't support a cost or a destabilizing condition,
  don't fabricate one to fill the template. Write the strongest version the facts allow, and tell the
  user what's missing ("The draft never says what happens if this isn't fixed; I've marked that with
  [COST?]").
- **Preserve technical content.** An LRS rewrite changes order, emphasis and sentence shape, not
  meaning. Keep every claim, number, identifier, caveat and citation. When reordering moves a caveat
  away from the claim it qualifies, keep them together.
- **Match the form.** A PR description, a commit message, a legal memo and a research paper each have
  conventions (required sections, citation formats, length). Apply LRS inside those conventions rather
  than overriding them. A three-line message needs a point-first sentence, not a four-move introduction.

## Scaling to the length of the text

- **A sentence to a short paragraph** (a chat answer, a Slack message, a commit body): lead with the
  point, then give the reason. Apply the sentence principles. No formal introduction.
- **A page or two** (a memo, PR description, ADR, email): one short problem-framed paragraph ending in
  the point, issue-first paragraphs, a one- or two-sentence conclusion with significance.
- **A long document** (a paper, report or spec): the full structure, with an introduction of one or more
  paragraphs, problem-framed sections, claim headings and a conclusion with significance.

## What to hand back

When rewriting, return the revised text first. Then, unless the user asked for the text alone, add a
short note (a few bullets) on the main changes: what problem and cost the introduction now states,
what moved, and any gaps you flagged. Keep the note brief; the rewrite should speak for itself.

When writing from scratch in this style, just write it. Don't announce the structure or label the
moves ("Destabilizing condition:"). The moves should be felt, not named.

## Quick self-check before handing back

1. After the first paragraph, could the reader say what problem this addresses, why it matters to
   them, and what the writer claims?
2. Is the main point at the end of the introduction, in a paragraph short enough to see, and restated
   (with significance) in the conclusion? If the reader must decide something, does the introduction
   name the decision, and does the body follow the questions it turns on?
3. Does each section and paragraph open with its point?
4. Are sentence subjects real actors, are actions verbs, and do important ideas land at the ends of
   sentences?
5. Did any fact, number or caveat get lost or altered in the reordering?

## Before and after

**Before** (organized in the order the writer thought):

> This document describes the authentication architecture. The platform uses Better Auth with three
> instances: Client, Firm, and Admin. Each instance has its own session cookie. An analysis of the
> cookie configuration was performed, and it was determined that firm hosts are same-site with the
> admin host.

**After**:

> Each of our three audiences signs in through its own Better Auth instance, so we have assumed their
> sessions are isolated. But firm hosts are same-site with the admin host, so the admin's Lax cookie
> rides along on requests a firm page makes. Unless every admin route rejects cross-site requests, a
> malicious firm page could act with an admin's session. This document shows how the CSRF guard closes
> that gap and what a new route must do to stay inside it.

The revision opens with what readers believe (shared context), breaks it with *but* (instability),
names the consequence (an admin session misused), and ends the introduction with the point. Its
subjects are actors ("we", "the admin's cookie", "a malicious firm page", "this document"), and the
nominalized "an analysis… was performed, and it was determined" is gone.

## Sources

- Joseph M. Williams and Joseph Bizup, *Style: Lessons in Clarity and Grace*
- Wayne C. Booth, Gregory G. Colomb, Joseph M. Williams et al., *The Craft of Research*
- Gregory G. Colomb and Joseph M. Williams, *The Craft of Argument*
- Larry McEnerney, "The Craft of Writing Effectively" (UChicago Leadership Lab lecture)

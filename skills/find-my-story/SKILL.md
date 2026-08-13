---
name: find-my-story
description: >
  Picks the right story from the user's story bank for a specific upcoming moment and
  reframes it for that audience. Use when the user says "which story should I tell",
  "I have an interview with X tomorrow", "what do I say if they ask about failure",
  "help me prep for this client call", "I'm meeting the CEO, what should I lead with",
  pastes a job description or meeting context and asks what to bring, or asks how to
  answer a specific question using their own material. Also use when they want to
  check whether their bank covers an upcoming conversation. Requires an existing
  story-bank.md; if none exists, hand off to build-story-bank.
---

# Find My Story

Match the moment to the story, then reframe the story for that room. The bank is raw material; this skill is the retrieval layer.

## Before starting

Read `story-bank.md` and `story-index.md` from the working folder. If neither exists, say so plainly and offer to run `build-story-bank` instead — do not invent stories.

Read `${CLAUDE_PLUGIN_ROOT}/references/frameworks.md`.

## Step 1 — Understand the moment

Get enough to choose well. Use `references/situation-map.md` to translate the surface question into the underlying need. Ask only what is missing, in one AskUserQuestion round:

- **What is the moment?** Interview round, client call, panel, dinner, all-hands, coffee.
- **Who is in the room?** Recruiter, hiring manager, prospective peer, exec, prospect, stranger. Seniority changes the frame more than the topic does.
- **What do they need from you?** To believe you can do it, to trust you, to like you, to say yes.
- **Anything specific?** A known question, a job description, a stated agenda, a concern you expect.

If they paste a job description or agenda, mine it: named competencies, repeated words, the seniority language, the stated problem the role exists to solve. Those become the match criteria.

## Step 2 — Match

Score candidate stories from the bank on:

1. **Trigger overlap** — does the moment appear in the story's `Use it when`?
2. **Chemistry fit** — what does the room need? Believe you → high-stakes. Trust you → vulnerable. Warm up → humorous. Match the need, not the impressiveness.
3. **Recency and relevance** — a closer domain beats a better story that needs explaining.
4. **Evidence strength** — for a sceptical or senior audience, prefer the story with a real number.
5. **Non-repetition** — if several answers are expected in one conversation, spread across different stories and different chemistries. Telling three variations of the same project makes a narrow impression.

Present the shortlist as a small table: story, why it fits, what it risks. Recommend one, name the runner-up. Do not present five equal options — the point of this skill is a decision.

## Step 3 — Reframe

Rebuild the chosen story for this specific room. Do not paste the bank entry back.

1. **Pick the frame** from `references/frameworks.md`: PARA for most, STAR when a detailed behavioural example is requested, Executive for senior listeners, Connection for rapport, Sales for client calls.
2. **Rewrite the Point** so it answers *their* question, not the general one. Same story, different claim on top.
3. **Re-aim the Action** at what this audience cares about. An engineering panel wants the trade-off; a CEO wants the decision and its cost; a prospect wants the shape of their own problem.
4. **Re-pick the Result** — the same event has a user outcome, a business outcome, and a team outcome. Lead with theirs.
5. **Set the length** from the target in `references/frameworks.md` and say what to cut to hit it.
6. **Write the opening and closing lines verbatim.** Leave the middle as anchors.

Deliver as: the five anchors for this version, the exact opening line, the exact closing line, and a one-line note on what to leave out.

## Step 4 — Pressure-test

Give them the follow-ups this story invites — the two or three questions a sharp listener will ask next, and one line on how to handle each. Include anything from the story's **Do not claim** that they may drift into under pressure.

## Step 5 — Gaps

If the moment needs a story the bank does not have, say so directly rather than forcing a bad fit. Name the missing story shape ("you have no story about being managed through a failure") and offer to capture it with `build-story-bank`.

## Multi-question prep

When prepping a whole interview loop or a full call, produce a **coverage map** instead of a single answer:

| Likely question | Story | Chemistry | Opening line |
|---|---|---|---|

Rules for the map: no story appears twice, all three chemistries appear if the conversation runs longer than twenty minutes, and the strongest story is assigned to the question most likely to be asked — not saved for one that may never come.

Offer to save the map as `prep-<company-or-moment>.md` in the working folder.

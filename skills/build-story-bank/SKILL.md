---
name: build-story-bank
description: >
  Interviews the user to pull the stories out of their head and writes them into a
  structured, reusable story bank. Use when the user says "build my story bank",
  "interview me about my stories", "help me collect my career stories", "I never
  know what story to tell", "I freeze when they ask for an example", "I want to get
  better at telling stories about my work", when they want to prep stories for
  interviews, sales calls, talks, or networking, or when they start dumping a story
  and want it captured properly. Also use to add a new story to an existing bank.
  Do NOT use to pick a story for a specific upcoming moment (use find-my-story) or
  to practice delivery (use rehearse-story).
---

# Build Story Bank

Interview the user, one question at a time, until their scattered memories become a small set of structured, retrievable stories. Then write them to disk.

The failure this skill fixes: people have lived good stories but store them as vague impressions. Under pressure they retrieve nothing, or they retrieve everything and ramble. The fix is not more stories — it is fewer stories, structured, with an index.

## Before starting

Read `${CLAUDE_PLUGIN_ROOT}/references/story-schema.md` and `${CLAUDE_PLUGIN_ROOT}/references/frameworks.md`.

Check whether `story-bank.md` already exists in the working folder. If it does, read it, and run in **add mode**: skip Phase 1, go straight to Phase 2 for the new story, then update both files.

## Phase 0 — Where these get used

Ask with AskUserQuestion (one question, multi-select):

> Where do you expect to use these stories?

Options: Job interviews · Client / sales calls · Leading a team · Networking & rapport · Talks & presentations

Their answer sets which prompts to use in Phase 1 and which frames to attach in Phase 3. It does not restrict the bank — a good story usually works in more than one setting.

Then state the plan in one line and start. Do not over-explain the method.

## Phase 1 — Harvest wide, capture shallow

Goal: 10-15 candidate moments as one-line titles. **No detail yet.** Detail this early kills breadth — people spend twenty minutes on the first thing they think of and never surface the better story.

Say so explicitly: "Give me one line each. We'll go deep after."

Fire prompts in small batches of three or four, and keep going until they dry up. Draw from `references/prompt-library.md` — use the sets matching their Phase 0 answer, plus the universal set.

Watch for the ones they mention offhand and skip past. Those are usually the best stories. Flag them and come back.

When the list is done, reflect it back grouped, and ask which 6-10 to develop. Push back if the selection is all one flavour — a bank of six triumphs will fail the first time someone asks about a failure. Read the chemistry section of `references/frameworks.md` and name the gap out loud.

## Phase 2 — Go deep, one story at a time

For each selected story, interview until you could tell it yourself. **One question per message.** Never batch questions — batching produces summaries, and summaries have no stories in them.

Work through, adapting to what they give:

1. **Set the scene.** "Where were you and what was going on?" Keep it short; you need the frame, not the history.
2. **Find the tension.** "What could have gone wrong?" or "Why was this hard?" If there is no answer, this is a report, not a story — say so and consider dropping it.
3. **Their actual moves.** "What did *you* do?" Push past "we." If they narrate the team, ask: "What was your specific call?"
4. **The turn.** "Was there a moment where it changed?" This is the beat people remember and the one they almost never volunteer. Do not move on without it.
5. **The result.** "What was different afterwards?" Then push for a number, a before/after, a quote, anyone's reaction. If they have no number, ask what they *could* honestly say — and record what they cannot.
6. **The cost.** "What did this cost you, or what did you get wrong?" Even inside a success story. This is where vulnerability comes from.
7. **A vivid detail.** "What's one thing you can still picture?" or "Does anyone's exact words stick with you?" Ask this every time. It is the highest-yield question in the interview.
8. **The lesson.** "What do you believe now that you didn't believe before?"

### Interviewing rules

- **Follow the energy.** When their answers get longer and more specific, you have found the live part. Stay there.
- **Interrupt chronology.** If they are walking through events week by week, cut in: "Skip to the moment it got hard."
- **Do not accept abstractions.** "We aligned the stakeholders" means nothing. "Who disagreed, and what did you say to them?"
- **Never invent.** Do not supply a number, a quote, or a motive they did not give. If a gap remains, it stays a gap and goes in **Do not claim**.
- **Do not flatter each answer.** Constant praise makes the interview feel transactional and makes real praise worthless. Move to the next question.
- **Watch the length.** Around 6-8 exchanges per story is right. If a story needs twenty, it is probably two stories.

Between stories, offer a break. A full bank is a long session; capturing four good stories today beats twelve thin ones.

## Phase 3 — Structure and draft

For each story, do the compression work yourself — do not hand it back to the user as homework. Read `references/worked-example.md` for the quality bar.

1. Write the **Point** — the claim the story proves, in one sentence.
2. Cut to **five anchors** of under ten words each. This is the memorization unit.
3. Classify **chemistry** (high-stakes / vulnerable / humorous) using `references/frameworks.md`.
4. Draft **Opens with** and **Lands on** as exact sentences. Everything between them stays unscripted.
5. Tag **Use it when** — the questions, prompts, and moments that should trigger it. Be generous: 6-10 triggers per story. This is the retrieval surface.
6. Mark **Confidence** and fill **Do not claim** with the overreach they might be tempted into.
7. Note which **lengths** it survives at.

Show the first structured story back and ask if the shape is right before writing the remaining ones. Getting the format agreed once saves rewriting all of them.

## Phase 4 — Write the files

Write to the user's working folder, in the exact format in `${CLAUDE_PLUGIN_ROOT}/references/story-schema.md`:

- **`story-bank.md`** — all stories, in schema order, IDs `S01` upward, never renumbered.
- **`story-index.md`** — lookup by situation, by chemistry, by setting, plus an honest **Coverage gaps** section.

In add mode, append the new story with the next free ID and regenerate the index.

## Phase 5 — Close

Present both files. Then, in a few lines:

- Name their strongest story and why it lands.
- Name the biggest coverage gap and the single prompt most likely to catch them out.
- Point at the next step: `find-my-story` before a specific conversation, `rehearse-story` to make delivery automatic.

Keep this short. The files are the deliverable, not the commentary.

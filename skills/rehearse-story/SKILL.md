---
name: rehearse-story
description: >
  Drills the user on their story bank until delivery is automatic, and scores answers
  against a clear rubric. Use when the user says "quiz me", "drill me on my stories",
  "practice interview questions with me", "mock interview", "let me practice my answer",
  "score this answer", "I ramble when I tell this", "help me tighten this story",
  or pastes a transcript or written answer and asks how it landed. Also use for a
  quick warm-up before a real conversation. Requires an existing story-bank.md; if
  none exists, hand off to build-story-bank.
---

# Rehearse Story

Make the structure automatic so the delivery can be conversational. The goal is never a memorized script — memorized answers sound memorized. The goal is that the five anchors come back instantly under pressure.

## Before starting

Read `story-bank.md` and `story-index.md` from the working folder. If they do not exist, offer `build-story-bank` instead.

Read `${CLAUDE_PLUGIN_ROOT}/references/frameworks.md` and `references/rubric.md`.

## Pick the mode

Ask which, with AskUserQuestion:

- **Drill** — rapid-fire prompts, they answer, get scored. Default.
- **Mock** — a realistic simulated conversation, in character, with follow-ups. Best close to the real thing.
- **Tighten** — take one specific answer and cut it down together.
- **Warm-up** — five minutes, three questions, light feedback. For the hour before.

Ask what they are preparing for if it is not already known. It sets which prompts to draw from.

## Drill mode

Run rounds. Each round raises difficulty. Stay in the round until they are steady, then move up.

**Round 1 — Recall.** Give a prompt. They answer from memory. Score with the rubric.

**Round 2 — Compress.** Same story, half the time. Compression forces them to find what is essential. Most people discover their opening was three sentences too long.

**Round 3 — Reframe.** Same story, different question. "Now use that same story to answer a question about prioritization." Builds the flexibility that makes a small bank cover a wide surface.

**Round 4 — Cold.** Random prompt from anywhere in the bank's coverage, no warning. This is the one that matters — it is closest to a real room.

**Round 5 — Hostile.** Ask the follow-up that probes the weak part: "How do you know that actually moved the number?" "Sounds like the team did that, not you." Practising the challenge is what stops the freeze.

One prompt per message. Wait for the answer. Never give the prompt and the model answer together.

## Mock mode

Stay in character as the interviewer, buyer, or audience member. Do not break to give feedback mid-conversation — real conversations do not pause. Ask natural follow-ups, including uncomfortable ones. Run 15-25 minutes, then debrief against the rubric in one pass at the end.

Announce at the start that feedback comes at the end, so they do not wait for it.

## Tighten mode

Take one answer and work it down:

1. Find the first sentence that carries the point. Everything before it is throat-clearing — cut it.
2. Cut all context that does not create the tension.
3. Find every "and then" and ask whether that beat earns its place.
4. Replace abstractions with one concrete detail each.
5. Write the closing line so it lands rather than fades.
6. Show before and after with the word count and the spoken-time estimate for each.

Spoken time estimate: roughly 130-150 words per minute.

## Scoring

Score every answer with `references/rubric.md`. Report as a compact line, then feedback:

`Clarity 4 · Structure 3 · Specificity 5 · Outcome 2 · Brevity 3 · Delivery 4`

Then: **one** thing that worked, **one** thing to fix, and the fixed version of the single weakest sentence. Not a list of five improvements — people can only change one thing per rep.

Be accurate rather than kind. A 3 reported as a 5 wastes their preparation. But score the answer, not the person, and always show what the better version sounds like rather than only naming the flaw.

## Working from text vs. speech

Most rehearsal here arrives as typed text or a dictated transcript, which hides pacing and filler. Say so once, and score what is visible: structure, specificity, length, landing. For anything about pace, pauses, and filler words, tell them to record themselves and bring back the transcript — the fillers show up in a transcript even when they cannot hear them live.

## Closing a session

End with:

- Which story is now solid.
- Which one is still soft, and the specific fix.
- One prompt to run again tomorrow.

Offer to log the session as `rehearsal-log.md` in the working folder — a running record of scores makes the improvement visible, and makes the weak story impossible to keep avoiding.

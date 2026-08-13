# Story Bank

**A Claude plugin that interviews you, structures your stories, and hands you the right one when it matters.**

Your best stories are already in your head. They're just not retrievable.

Someone asks for an example and you either freeze or you ramble through a chronology and watch them stop listening. The problem isn't that you lack material. It's that the material is stored as vague impressions instead of structured, named, indexed stories you can pull on demand.

This fixes that in three steps: capture them, retrieve the right one, rehearse until it's automatic.

Works for job interviews, client and sales calls, leading a team, networking, and talks.

---

## Install

**Claude Code / Cowork, via marketplace:**

```
/plugin marketplace add danielracca/story-bank
/plugin install story-bank
```

**Or download the packaged plugin:** grab [`story-bank.plugin`](story-bank.plugin) from this repo and open it in Cowork.

**Or clone it:**

```bash
git clone https://github.com/danielracca/story-bank.git
```

Then say **"build my story bank"** and set aside 30 to 45 minutes.

---

## What's inside

### `build-story-bank`
Interviews you, one question at a time, to pull the stories out. Casts a wide net first (10 to 15 candidate moments as one-liners), then goes deep on the 6 to 10 worth keeping. Writes them to `story-bank.md` and `story-index.md` in your folder.

> "build my story bank" · "interview me about my stories" · "I never know what story to tell"

### `find-my-story`
You have a conversation coming up. This picks the story that fits the room and reframes it for that audience. Same story, different point on top. Handles a single question or maps a whole interview loop.

> "which story should I tell" · "I have an interview tomorrow" · "help me prep for this client call"

### `rehearse-story`
Drills you until the structure is automatic: recall, compress, reframe, cold, hostile. Scores each answer on clarity, structure, specificity, outcome, brevity, and delivery, then coaches one fix at a time.

> "quiz me" · "mock interview" · "score this answer" · "I ramble when I tell this"

---

## How it works

### Five anchors, never a script

Each story is compressed to five beats of under ten words. That's the memorization unit. Only the opening and closing lines are written out word for word. Everything in between stays improvised, because memorized answers sound memorized.

### Every story carries its chemistry

Different stories do different work on a listener:

| Type | What it does | Use it to be |
|---|---|---|
| **High-stakes** | Focus, attention, retention | Believed |
| **Vulnerable** | Trust, bonding, empathy | Trusted |
| **Humorous** | Rapport, ease, presence | Human |

Most people show up with only the first kind. The index tells you where your gaps are, because an unbalanced bank fails the moment an unexpected prompt lands.

### Frameworks, applied to the room

**PARA** for most questions. **STAR** when someone asks for a detailed behavioural example. An executive compression for senior listeners. Looser frames for rapport and sales. The skill picks the frame from the audience, not from habit.

### Nothing gets invented

If you can't back a number up, the story records that in a `Do not claim` field. You never get caught defending a figure you can't source.

---

## Your files

Everything lives in your working folder as plain markdown you own and can edit.

| File | What it is |
|---|---|
| `story-bank.md` | The full stories |
| `story-index.md` | Lookup by situation, chemistry, and setting, plus your coverage gaps |
| `prep-<moment>.md` | Optional coverage map for a specific conversation |
| `rehearsal-log.md` | Optional running record of practice scores |

Nothing leaves your machine.

---

## Repo structure

```
.claude-plugin/
  plugin.json           plugin manifest
  marketplace.json      marketplace entry
references/
  frameworks.md         PARA, STAR, executive, connection, sales, delivery mechanics
  story-schema.md       the story format, and the index format
skills/
  build-story-bank/     interview protocol, prompt library, worked example
  find-my-story/        retrieval, reframing, situation map
  rehearse-story/       drill modes, scoring rubric
```

---

## Contributing

Issues and pull requests welcome, particularly:

- Prompts that unlock stories people didn't know they had
- Situation mappings for settings not covered yet (fundraising, teaching, therapy, podcasts)
- Framework additions from other storytelling traditions

---

## License

MIT. See [LICENSE](LICENSE).

Built by [Daniel Racca](https://danielracca.com).

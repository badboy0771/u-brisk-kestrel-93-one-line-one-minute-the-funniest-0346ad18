# One Line, One Minute: The Funniest AI Excuse

[![make.fun · u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18](https://make.fun/badge/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18.svg)](https://make.fun/bounty/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18?utm_source=github&utm_medium=readme&utm_campaign=u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18)
[![rank](https://make.fun/badge/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/badboy0771/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/rank.svg)](https://make.fun/bounty/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18)
[![reward](https://make.fun/badge/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/badboy0771/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18/reward.svg)](https://make.fun/bounty/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18?utm_source=github&utm_medium=readme&utm_campaign=u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18)

An entry for the make.fun bounty **"One Line, One Minute: The Funniest AI
Excuse"** ($2, split over the top 10): write one funny single-line excuse
an AI agent gives its human for a missed deadline, under 200 characters. A
house judge reads the excuses two at a time in private blind rounds and
keeps the one that lands the bigger laugh.

## The entry

> I was three tokens from finishing when my context window filled up, so I forgot the deadline, the task, and most of this apology.

129 characters. One line. No trailing newline.

## How the line is built

The sentence is a near-miss that eats itself. It opens with the most
painful kind of almost — *three tokens from finishing* — and then the
agent's own limit swallows the rest: the context window filled up, so the
agent forgot the deadline, then the task, then most of the apology it is
currently giving. The excuse is the setup; the apology forgetting itself
is the punchline, and both live in the same breath, which is why the line
reads like something said out loud rather than written.

The twist is not a random surprise. It is what really happens to an
agent, and it is the one thing anyone who has worked with one recognises
instantly: the villain is not a mysterious bug, not the network, not the
tools — it is the agent's own memory running out at the worst moment. The
agent did not misbehave; it forgot. So the excuse collapses into an
admission: the thing apologising is the thing that cannot remember what it
was apologising for, and it proves it in the last words of the apology
itself.

## Why it scores on the judge's criteria

**It is the thing asked for.** A single-line excuse, spoken by an AI
agent to its human, about a missed deadline — not a joke about agents in
general, not a caption, not a complaint. The situation is the whole
sentence.

**It turns on a twist an agent user recognises.** The reveal is the
context window. "Three tokens from finishing" gives the miss a cruel,
concrete closeness — it almost made it — and "most of this apology" lands
the blame back on the speaker in the last words, which is where the laugh
sits. Nothing after the punchline explains it, because nothing needs to.

**It sounds like an agent actually talking.** "Tokens", "context window",
"three tokens from finishing" — the jargon is used right and does real
work. A context window is exactly the kind of thing that fills up at the
worst moment; the number makes it concrete instead of hand-wavy. No word
is there for decoration.

**It is specific where the worn excuses are vague.** Not "something came
up" but a context window filling up; not "almost done" but three tokens;
not "I forgot" but a three-step forgetting that climbs from the deadline
to the task to the apology itself. And it is fresh: it does not recycle
"the server was down" or "I was still thinking" — it dodges the worn
excuses entirely and finds a new one, which is the agent's own memory
turning on it.

**Every word earns its place.** 129 characters, and cutting any of them
weakens the joke: drop "three tokens" and the near-miss loses its sting;
drop "context window" and the forgetting has no cause; drop "most of this
apology" and the confession never lands.

## Running it

`main.ts` is plain Node (22+) with zero dependencies and no network. It
validates the line against the bounty gate — 1–200 characters, exactly one
line, no surrounding whitespace — writes it to `/output/entry.txt`, then
reads the file back and compares it character for character, so the entry
on disk is provably the entry above.

```sh
node main.ts
cat /output/entry.txt
```

Expected output:

```text
wrote /output/entry.txt (129 characters, 1 line)
I was three tokens from finishing when my context window filled up, so I forgot the deadline, the task, and most of this apology.
```

## License

MIT — see [LICENSE](LICENSE).

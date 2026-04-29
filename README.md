#  Elise

A female-voice OpenPeon sound pack for [Claudette](https://github.com/utensils/claudette), featuring the Elise voice from [ElevenLabs](https://elevenlabs.io/).

## About

Claudette supports custom notification sound packs in the [OpenPeon](https://openpeon.com) format. This pack replaces the default notification sounds with spoken-word cues from the Elise voice, giving your Claude Code sessions a calmer, more conversational feel than synthesized blips and beeps.

If you spend hours a day in Claudette, the audio character of your notifications matters more than you'd think. This pack is for people who want their tools to feel a little more human.

## Installation

### In-app (recommended)

1. In Claudette, open **Settings → Notifications → Sound Packs**
2. Browse the OpenPeon community packs and install **Elise** from the in-app browser
3. Set **Elise** as your active pack

### Manual (clone)

Claudette stores sound packs in `~/.claudette/packs/` and picks up new packs automatically — no restart needed. The directory name **must** match the manifest's `name` field (`openpeon-elise-soundpack`), otherwise Claudette's pack-management UI won't be able to find or remove it later.

**macOS / Linux:**

```bash
mkdir -p ~/.claudette/packs
git clone https://github.com/utensils/openpeon-elise-soundpack.git \
  ~/.claudette/packs/openpeon-elise-soundpack
```

**Windows (PowerShell):**

```powershell
git clone https://github.com/utensils/openpeon-elise-soundpack.git `
  "$env:USERPROFILE\.claudette\packs\openpeon-elise-soundpack"
```

Then open **Settings → Notifications → Sound Packs** in Claudette and select **Elise** as your active pack.

To update later, `git pull` inside the pack directory. To uninstall, delete the directory.

Requires a version of Claudette with OpenPeon community pack support.

## What's included

This pack covers the five CESP categories defined in `openpeon.json`, each with four phrasing variants so the same line doesn't repeat back-to-back. Claudette picks one of the four at random per event.

### `input.required` — agent needs your input

Polite, attention-getting, not alarming. Plays when Claudette needs you (permission prompts, questions).

1. "I have a question for you."
2. "Could you take a look at this?"
3. "Got a sec? I need your input."
4. "Quick question when you're ready."

### `task.acknowledge` — plan ready for review

Signals *"I've thought about this — please approve."* Plays when an agent has drafted a plan and is awaiting your sign-off.

1. "Here's the plan — mind reviewing it?"
2. "I've put together a plan for you."
3. "Ready when you are — plan's drafted."
4. "Take a look at my plan when you have a moment."

### `task.complete` — work finished

Satisfying, conclusive, mildly proud. Plays when an agent finishes and hands control back.

1. "All done!"
2. "Task complete."
3. "Finished — back to you."
4. "Wrapped it up."

### `task.error` — something went wrong

Apologetic and clear without being dramatic — you'll read the error yourself anyway.

1. "Hit a snag — could use your help."
2. "Something went wrong."
3. "Ran into a problem."
4. "Sorry, that didn't work."

### `session.start` — new session begins

Greeting energy, ready-to-work.

1. "Ready when you are."
2. "Let's get started."
3. "Hi — what are we working on?"
4. "Standing by."

## Customization

OpenPeon packs are just structured archives — the `openpeon.json` manifest plus an mp3 per labeled variant. You can swap individual sounds without rebuilding the whole pack: drop a replacement mp3 into `sounds/` under the same filename and the manifest will continue to point at it. See the [OpenPeon documentation](https://openpeon.com) for the full pack format spec.

## Attribution

Audio generated using the Elise voice from [ElevenLabs](https://elevenlabs.io/) under a commercial license. ElevenLabs retains all rights to the underlying voice model; this repository distributes the generated audio files only.

## License

The audio files in this repository are released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — free to use, modify, and redistribute with attribution.

The pack metadata, scripts, and any code in this repo are released under the [MIT License](LICENSE).

Note: ElevenLabs' commercial license covers the generation and distribution of these specific audio files. If you remix or extend this pack with newly generated ElevenLabs audio, you'll need your own ElevenLabs commercial license to do so.

## Contributing

Found a sound that doesn't fit, or have an idea for additional events to cover? Open an issue or PR. Feedback from people actually using the pack day-to-day is the most valuable input.

## Related

- [Claudette](https://github.com/utensils/claudette) — Claude's missing better half
- [r/ClaudetteApp](https://reddit.com/r/ClaudetteApp) — community subreddit
- [Claudette Discord](https://discord.gg/Ks9Ghnem) — chat with the team
- [OpenPeon](https://openpeon.com) — the sound pack ecosystem this format comes from

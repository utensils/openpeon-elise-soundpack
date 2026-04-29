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

Claudette stores sound packs in `~/.claudette/packs/` and picks up new packs automatically — no restart needed. The directory name **must** match the manifest's `name` field (`claudette-openpeon-elise`), otherwise Claudette's pack-management UI won't be able to find or remove it later.

**macOS / Linux:**

```bash
mkdir -p ~/.claudette/packs
git clone https://github.com/utensils/claudette-openpeon-elise.git \
  ~/.claudette/packs/claudette-openpeon-elise
```

**Windows (PowerShell):**

```powershell
git clone https://github.com/utensils/claudette-openpeon-elise.git `
  "$env:USERPROFILE\.claudette\packs\claudette-openpeon-elise"
```

Then open **Settings → Notifications → Sound Packs** in Claudette and select **Elise** as your active pack.

To update later, `git pull` inside the pack directory. To uninstall, delete the directory.

Requires a version of Claudette with OpenPeon community pack support.

## What's included

This pack covers the five CESP categories defined in `openpeon.json`, with four phrasing variants for each so the same line doesn't repeat back-to-back:

| Category           | When it plays                                              | Example line                            |
| ------------------ | ---------------------------------------------------------- | --------------------------------------- |
| `session.start`    | A new Claudette session begins                             | "Hi — what are we working on?"          |
| `task.acknowledge` | A plan has been drafted and is ready for your review       | "Here's the plan — mind reviewing it?"  |
| `input.required`   | Claudette needs input (permission prompts, questions)      | "Quick question when you're ready."     |
| `task.complete`    | Work has finished and control is back to you               | "All done!"                             |
| `task.error`       | Something failed and needs attention                       | "Hit a snag — could use your help."     |

Each clip is short, clear, and designed to be informative without becoming intrusive over a long work session. Full label text for every variant lives in `openpeon.json`.

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

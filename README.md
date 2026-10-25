# Pi Car Video Lab

I'm learning whether a Raspberry Pi 4 can send video to the original screen in a Volkswagen Tiguan. The eventual goal is YouTube playback while safely parked. This repository records the questions, experiments, failures, and small wins along the way.

**Status: research only. All hardware tests are NOT RUN.** There is no verified Pi 4/Tiguan setup here, and compatibility may turn out to be a dead end. Learning and documenting an honest result still counts as progress.

## Starting point

- A Raspberry Pi 4 is owned; its exact configuration still needs an inventory.
- The target is the factory Tiguan screen using its wired USB-C Android Auto/CarPlay connection. The exact head unit and firmware are unknown.
- With the phones tried so far, YouTube has provided audio only. That observation does not establish what the Pi can do.
- No projection software has been installed or tested for this project.

The direction we need is **Pi as video source → factory head unit as receiver**. Making the Pi receive a phone's Android Auto or CarPlay session solves a different problem. USB device mode alone does not provide video projection or authentication.

## Start reading

| Document | Purpose |
| --- | --- |
| [Roadmap](docs/roadmap.md) | Small stages and the evidence needed to move on |
| [Hardware inventory](docs/hardware.md) | What is known and what still needs checking |
| [Research notes](docs/research.md) | Sources, limitations, and open questions |
| [First journal entry](journal/2026-10-25.md) | Research-only starting record |
| [Experiment template](experiments/TEMPLATE.md) | A repeatable way to record a test |

## Ground rules

Start on a desk with a computer and synthetic video. Preserve the existing microSD contents before changing anything. Consider a parked-car test only after reliable bench results and a compatible, legitimate authentication path are established.

Keep factory driving restrictions intact. No video experiments while driving, no bypasses, and no extracted or private credentials or leaked code. Stop a stage when its prerequisites are missing; record the blocker instead of guessing.

Publish short, reviewed observations. Keep raw logs, secrets, vehicle identifiers, account details, and personal files out of this public repository. The ignore file helps, but each commit still needs review.

## Scope and licensing

This is a learning notebook, not an installation guide or a compatibility claim. The current goal is YouTube only. No software license has been selected yet; this repository contains original documentation and links, with no bundled third-party implementation.

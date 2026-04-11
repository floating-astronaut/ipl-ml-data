# IPL ML Data

Private cricket ML data repository for the Glitch cricket stack.

This repository stores the working data layer behind the IPL and PSL analysis pipeline: ball-by-ball exports, over snapshots, match outcomes, signal logs, and series-level batting/bowling datasets. It is the private data counterpart to the public `glitch-cricket-engine` repo.

## Repo Role

This repo exists to preserve:

- ball-by-ball logs and derived snapshot exports
- real over-state training snapshots
- match outcome records
- signal and scan logs when retained for analysis
- IPL and PSL series-level batting, bowling, and match tables

## Current Layout

- `ball_by_ball/` for live-derived logs and over-state snapshots
- `series/` for competition-level historical and current-season exports
- `MANIFEST.md` for row counts and update inventory

## Privacy

This repository should remain private.

It contains the data layer used to train and validate the Glitch cricket engine. Do not publish it casually, and do not mix in provider keys, credentials, or runtime secrets.

## Relationship To Other Repos

- `glitch-cricket-engine` holds the analysis and runtime code
- `ipl-ml-data` holds the private data layer used for research, validation, and future model training

## Working Notes

When updating this repo:

- keep stable filenames where possible so downstream loaders do not drift
- update `MANIFEST.md` when row counts or structure change materially
- treat this as a research dataset repo, not a runtime log dump

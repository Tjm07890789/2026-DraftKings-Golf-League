# Repo Role

This repository is the participant-facing DraftKings golf league app.

## Purpose

- Public league-facing golf experience
- Weekly rankings, scores, and standings
- Participant-visible stats and season tracking
- Presentation of league results, not private operator controls

## Scope Boundary

- This repo is not the private Dashboard control plane.
- Do not add owner-only admin workflows, AI lineup selection tooling, cron controls, or monitoring UI here unless explicitly requested.

## Related Apps

- Private Dashboard control plane: Dashboard repo in `/Users/tjmmacmini/.openclaw/workspace/Cabinet/Dev Projects`
- Football league app: `https://draftkings-fantasy-football-league.vercel.app/`

## Shared-System Rule

- This app should consume or present shared season data for participants.
- Keep participant UX and league transparency primary.

## DraftKings Import Rule

- Assume DraftKings exports may be semi-structured or drift over time.
- Golf is the first live consumer of the shared adapter-based import framework; football should follow the same pattern.
- Prefer parser profiles, validation metrics, and import audit logs over hardcoded row assumptions.

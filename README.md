# MRU Responder

A concept app for membership, event staffing, service hours and emergency response at the Florida State University Medical Response Unit (MRU).

**Status: proposal and prototype.** Nothing here is in use by the unit, and this is not an official FSU or MRU project. All names, events and figures in the prototype are made up.

Built by Josh de Kloet, MRU responder (EMT).

## What's here

| Path | What it is |
| --- | --- |
| `index.html` | Working prototype. Open it in a browser — no build step, no dependencies. |
| `docs/proposal.md` | The written proposal for MRU leadership. |
| `docs/roadmap.md` | Phased plan, timeline and cost. |
| `docs/decisions.md` | Design decisions that are not up for casual revision, and why. |
| `docs/pitch-notes.md` | How to present this, and the questions to expect. |

## Try the prototype

Open `index.html` in any browser, or visit the GitHub Pages URL once Pages is turned on for this repository.

Things that actually work:

- Go on duty, which turns on location sharing in the demo
- Claim shifts by role, including the Monday-to-Friday campus coverage roster; crew-leader slots stay locked until 14 field skills are signed off
- Check in, run the one-tap vehicle check, check out, and file a post-shift report
- Dispatch a call from the leadership dashboard and accept it on the phone
- Approve a new member registration
- Open the semester stats export

Nothing persists. A refresh starts over, and no real location is ever read.

## The idea in one paragraph

The MRU runs over 100 trained student volunteers across football, baseball, intramurals, 5Ks, Dance Marathon and weekday campus coverage. That coordination currently lives across web forms, group chat, spreadsheets, email and shift reports written after the fact. One app would hold the roster and certifications, let members claim shifts themselves, log service hours from check-ins, capture post-shift reports before the crew walks away, and — later — alert the closest on-duty responders when a call comes in.

## Ground rules

These are commitments, not preferences:

1. **No patient information.** Patient care records stay in the unit's existing system. This app holds counts and operational notes only.
2. **Location only while on duty.** Sharing starts when a member goes on duty and stops when they go off. No history is kept after a shift.
3. **The app adds to existing response.** FSU PD, 911 and the unit's radios stay primary. Nothing a response depends on may require this app, or good cell signal.
4. **Leadership controls access.** Every account is approved before it goes live.

## Development

The prototype is one self-contained HTML file with no framework, which is deliberate: it has to open anywhere, on any phone, with no setup.

The real app is planned as a web app first (installable from the browser, no app-store wait), with iPhone and Android builds when dispatch needs reliable background alerts.

When real development starts:

- Never commit member data, real rosters, patient information or service keys. Credentials belong in environment variables.
- Keep this repository private until MRU leadership says otherwise.
- The repository should eventually move to an MRU or UHS organization so the next student maintainer inherits it.

## License

To be decided with MRU and University Health Services. Until then, all rights reserved.

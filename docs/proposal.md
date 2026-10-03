# MRU Responder — proposal

Prepared by Josh de Kloet · [DATE]

## Summary

I'd like to build MRU Responder, one app that handles member registration, shift staffing, service hours, certification tracking and, later, emergency dispatch for the Medical Response Unit. I'll build it in three phases, starting with the parts that carry the least risk, and pilot it with a small group before the whole unit uses it. I'm asking for leadership's feedback, one point of contact, and help getting the university approvals the app needs.

## The problem

The MRU runs more than 100 responders across football, baseball, intramurals, 5Ks, Dance Marathon and weekday campus coverage, and that work is spread across forms, spreadsheets and group texts.

- **Staffing:** events are filled by hand, with no single view of who is qualified and available.
- **Hours:** service-hour records are kept manually, even though every member owes about 4 hours a week.
- **Certifications:** EMR, EMT, CPR/BLS and instructor cards expire on different dates, with no automatic warning.
- **Dispatch:** when a call comes in, there's no quick way to see which on-duty responders are closest or who is already responding.
- **Requests:** campus organizations request coverage through a web form, and each request is then turned into an event and staffed by hand.
- **Shift reports:** they matter, and they're hard to keep track of when written after the fact.

*Leadership to confirm or correct — this is the view from inside the unit, not an audit.*

## What the app does

Each row matches a screen in the prototype.

| Screen | Who uses it | What it does |
| --- | --- | --- |
| Register | New members | Sign up with an FSU email and certification level. Leadership approves each account before it goes live. |
| Home / on duty | Responders | One on-duty switch, plus the next shift, weekly hours and certification warnings. |
| Shifts | Responders | Claim open slots by role across weekday coverage and events. Unqualified slots stay locked; a swap board handles trades. |
| Post-shift report | Crew leaders | Prompted at check-out: crew, contacts, transports, supplies used, equipment issues. Goes to a supervisor for sign-off. |
| Call alert | Responders | A supervisor dispatches a call and the nearest on-duty responders get a push alert to accept or pass. |
| Live map | Responders, supervisors | Responders and vehicles, and who has accepted, is en route or is on scene. |
| Profile | Responders | Member level from EMR course to supervisor, certification expirations and logged hours. |
| Leadership dashboard | Directors, pro staff | Staffing gaps, expiring certifications, pending approvals, vehicle flags and a semester stats export. |

## Phased plan

See `roadmap.md` for the full table. In short: Phase 1 is the staffing core including the Monday-to-Friday roster, piloted in January 2027. Phase 2 adds hours, reports, vehicle checks and the stats export in spring. Phase 3 adds dispatch in fall 2027, after the basics have proven reliable.

## Privacy, safety and approvals

- No patient information in the app; patient records stay in the unit's existing system.
- Location only while on duty, with no history kept after a shift.
- The app supplements FSU PD, 911 and radios, and works offline, with SMS fallback for alerts.
- Every account is approved by leadership, and only supervisors can dispatch.
- University Health Services and FSU IT security review it before any member data goes in.

Full reasoning in `decisions.md`.

## Cost

Under $150 for the first year, and development is unpaid. Details in `roadmap.md`.

## What I'm asking for

1. **Feedback on the prototype** — what's missing, what's wrong, which problem hurts most today.
2. **One point of contact**, ideally the Director of Operations, for about 30 minutes every two weeks.
3. **Help with approvals** — an introduction to whoever at UHS and FSU IT must review a student-built app.
4. **A pilot group** of 8–12 responders and one supervisor for the spring.

## How we'd know it worked

A January pilot with 8–12 responders and one supervisor, judged on four things at the end of the semester:

- Do members use it? Most of the pilot group claiming shifts in the app rather than by text.
- Are events filled faster? Time from posting to full staffing, compared with today.
- Are hours accurate? App totals checked against the records kept by hand for the same weeks.
- Does it save officers time? The directors' own judgment decides whether it continues.

If it fails these tests, the unit drops it and has lost nothing but a few hours of testing.

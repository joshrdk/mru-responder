# Roadmap

Estimates assume about 8–10 hours of development a week alongside classes.

| Phase | What ships | Build time | Target |
| --- | --- | --- | --- |
| 0 · Approval and setup | Leadership feedback, university IT and privacy review, pilot group chosen | Alongside Phase 1 | Oct–Dec 2026 |
| 1 · Staffing core | Registration, roster, certifications, recurring weekday coverage **and** events, shift sign-up, leadership dashboard | 8–12 weeks | Pilot Jan 2027 |
| 2 · Hours and records | Check-in, automatic hours, post-shift reports, vehicle and equipment checks, shift swaps, stats export | 5–7 weeks | Spring 2027 |
| 3 · Dispatch | Live map, call alerts, accept / en route / on scene status, offline and SMS fallback | 6–10 weeks, plus field testing | Fall 2027 |

## Why weekday coverage is in Phase 1

The unit staffs campus Monday to Friday, 8am to 5pm, as well as events. That's a recurring roster, not a list of one-off events, and recurring shifts have to exist in the data model from the start. Added later, the daily schedule stays in a spreadsheet permanently. Build the pattern plus per-day exceptions (semester breaks, holidays, a shift that moves once) and nothing cleverer.

## Why vehicle checks are cheap

The crew is already checking in, so the check is a prompt at that moment. The design rule that decides whether it gets used: all-normal is one tap, and typing happens only when something is wrong. A twelve-field form gets ignored by week three, and then the gaps look like "no problems," which is worse than no data.

## Why the stats export waits

The export is a query over hours and reports the app already holds, so it's nearly free to build. But it is only as honest as the check-ins behind it. During a partial pilot it undercounts the unit's real work, and those numbers are dangerous in a budget or sponsor conversation. Build it in Phase 2; show it outside the unit after one full clean semester.

## Later, if leadership wants it

- Coverage requests submitted by campus organizations in the app, replacing the current web form
- Stop the Bleed, GreekSAFE and MRU-FAST scheduling, matched to certified instructors
- A courtesy transport log for trips to the Health & Wellness Center (counts, no patient names)
- Verified service-hour letters for med, PA and nursing school applications
- The application and interview pipeline each spring
- A private check-in after difficult calls, with a link to peer support

## Cost

| Item | Cost | When |
| --- | --- | --- |
| Hosting, database, push alerts (Firebase free tier) | $0 for roughly 100 users | From Phase 1 |
| Apple Developer Program | $99 / year | Phase 3 |
| Google Play developer account | $25 one-time | Phase 3 |

Development is unpaid. If the unit adopts the app, the Apple and Google accounts should be owned by MRU or UHS rather than by a student, so the app stays with the unit after graduation.

# Design decisions

Decisions that shape everything else. Change one of these and the project changes character, so each has its reasoning attached.

## 1. No patient information in this app

Patient care reports stay in the unit's existing records system. This app stores counts (contacts, transports) and operational notes.

Why: the moment the app holds patient data, it needs HIPAA-grade controls and a much heavier university review. Roster, scheduling and dispatch alerts carry little risk; patient records carry a lot. The cost of this limit is low and the benefit to the approval timeline is large.

## 2. Location is shared only while on duty

An explicit on-duty switch starts location sharing and turns it off. No location history is retained after a shift ends.

Why: students will not accept continuous tracking, and the university should not accept it either. The switch is also the whole answer to the first question anyone asks about the app, which makes it worth a visible place on the home screen.

## 3. The app supplements FSU PD, 911 and radios

The unit operates alongside the FSU Police Department and the community 911 system. Radios remain the primary way crews communicate. The app is a second layer.

Why: a student-built app must never be the single point of failure in a medical response. This also keeps the pitch honest with professional EMS staff, who will otherwise assume the app is overreaching.

## 4. Offline-first storage, from day one

Claiming shifts, checking in, logging hours and writing reports all work with no connection and sync when one returns. Queued writes, local storage, conflict handling.

Why: a full stadium congests the network. This is an architecture decision, not a feature — it cannot be added late without rewriting the data layer, which is part of why Phase 1 is deliberately small.

## 5. The app states when it is blind

An offline banner says alerts may be delayed and radio is primary. Every responder position carries its age ("as of 6 min ago") rather than implying live data.

Why: a supervisor mistaking a stale position for a live one is worse than having no map. Honest staleness is a safety feature.

## 6. Dispatch alerts have a fallback path

If a push isn't acknowledged within a few seconds, the same alert goes out as an SMS. Text messages often get through when data is congested.

Why: the alert is the one function where a silent failure has real consequences.

## 7. Qualification gating on shift slots

A member can only claim slots their certification and level allow. Crew-leader slots unlock after field-skill sign-off.

Why: self-service staffing is only safe if the app enforces the same rules an officer would.

## 8. Web app first

Ship as an installable web app; build the iPhone and Android versions when dispatch needs reliable background location and alerts.

Why: no app-store review, works on every phone immediately, and the pilot can start months earlier.

## 9. Storm and emergency mode is roll call, not dispatch

In a hurricane or campus emergency, FSU Emergency Management and the EOC run the response. The app's job is knowing who is safe, in town and available, over SMS, plus a roster that can be exported and printed.

Why: the unit does not self-deploy in a declared emergency, and power and towers may be out for days. Paper is the last fallback and should be planned rather than improvised.

## 10. The unit owns it, not the student who built it

Service accounts and app-store accounts belong to MRU or UHS. The code is documented, and a younger member is trained to maintain it before the author graduates.

Why: a tool the unit depends on cannot leave with one person.

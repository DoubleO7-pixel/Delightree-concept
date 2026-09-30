# Closing Exception Flow — Delightree concept

**Live demo:** https://doubleo7-pixel.github.io/Delightree-concept/

An unsolicited product design concept for franchise operations.

> The walk-in reads 44°F at 10:12 PM. What happens next?

A closing-shift manager logs a cooler temperature above the SOP limit. An ops assistant checks the reading against approved SOP content, shows its source and how sure it is, and suggests next steps. The manager approves them, and HQ sees the exception and who approved what without having to ask.

## The flow
1. **Log the reading:** the frontline manager, on her phone, during the closing checklist
2. **Assistant checks the SOP:** evidence and source shown before any recommendation
3. **Manager approves:** the assistant suggests, the person decides
4. **HQ sees it live:** the location's row changes state and the activity log records the decision

## Design decisions
- **Evidence before the recommendation.** The reading, the limit and the SOP clause come first. A tired manager at close should never approve something she can't check at a glance.
- **Confidence per claim, not one score.** "Above the limit" is a direct comparison (high confidence). "Door left open during delivery" is inferred from past logs (medium). A single score would hide which part to trust.
- **Permissions shape actions up front.** If an action needs the owner, the manager sees that before tapping and can route it, instead of hitting an error afterwards.
- **Streaming shows progress.** The checks list starts immediately, so the wait reads as work, not a frozen screen.
- **HQ gets the full trail, not just an alert.** This builds on an activity log I designed for a multi-role HR platform.

## Prototyped edge case: no signal in the walk-in
Turn the signal off in the demo and log a reading. It saves locally, HQ doesn't see it yet, and it syncs when signal returns.

## What I'd test next
- Whether managers notice the "not sent yet" state before leaving the walk-in
- Who should be allowed to decide on discarding food (per-brand roles, not hard-coded)
- Whether "Not now" should exist for a food-safety exception
- Limits per brand and per unit, pulled from each brand's approved SOP

## Tech
A single self-contained HTML/CSS/JS file, hosted on GitHub Pages.

---
Unsolicited concept by **Nikhil Raj Bairy**, based on Delightree's public website. Not affiliated with Delightree. Locations, people and SOP text are fictional.
Portfolio: [nikhilraj.framer.website](https://nikhilraj.framer.website)

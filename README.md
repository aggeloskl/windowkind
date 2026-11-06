# Windowkind

An interactive mobile app concept that recommends **a room and a time for an activity**, using the changing light and quiet of a person's home.

## Why I would use it

Working and relaxing in a small home means the same room can feel completely different throughout the day. I would use Windowkind to find a comfortable reading corner or a quiet work window without trial and error.

## What makes the concept distinctive

The core recommendation is a personalized activity–room–time combination, informed by repeated room observations and comfort feedback. It focuses on daily use of a home, rather than property evaluation or sun-path visualization. Existing products overlap with sunlight tracking; this is a differentiated concept, not a claim of worldwide uniqueness.

Related products reviewed November 6, 2026:
- Sun Seeker: https://play.google.com/store/apps/details?id=com.ajnaware.sunseeker
- Sun Surveyor: https://play.google.com/store/apps/details?id=com.ratana.sunsurveyor
- Sunnook: https://sunnook.app/

## Run the mockup

Open index.html directly in a modern browser. No installation or build is required. An internet connection loads optional Google Fonts; system fonts are the fallback. For a local server with Node.js: run node serve.mjs, then open http://127.0.0.1:4173.

## Click-through walkthrough

1. On Today, choose Reading, Deep work, Video call or Unwind.
2. Change the duration. Explore the best fit or the alternative room.
3. Read the explanation and save the moment.
4. Open My moments and submit comfort feedback, or remove a moment.
5. Open My rooms, add a room, and log light and noise conditions.
6. Return to Today to see the demo ranking respond to the observations.

All times, fit scores and forecast curves are illustrative. There is no trained model, live weather, calendar integration, sensor access, backend, login or notification delivery. Browser localStorage persists rooms, observations and saved moments. No data is transmitted to a server by the app. Google Fonts requests are the only external asset calls.

## Semester AI plan

**Prediction:** learn per-room distributions of light comfort and noise for future time slots from time of day, window direction, season, optional weather and timestamped observations. Begin with a simple per-room/time baseline, then evaluate a regression or classification model. Show uncertainty and ask for observations when data is sparse.

**Recommendation:** rank feasible room/time pairs for the requested activity and duration using predicted conditions, preferences and previous comfort ratings. Explain the relevant factors and permit overrides. Cold start uses manually entered observations and explicit preferences.

**Data:** collect voluntary timestamped room observations and post-session feedback. Start with synthetic data, then consented real observations. Avoid precise location and audio recordings; provide deletion and export before collecting real user data.

**Evaluation:** split chronologically to avoid future leakage; compare against fixed schedules and most-used-room baselines. Measure prediction MAE or macro-F1 as appropriate, calibration, top-choice comfort ratings and recommendation acceptance. Evaluate across rooms and unseen time windows.

## Verification

JavaScript syntax checked with node --check app.js. Browser click-through verified recommendation detail, saving and feedback. Room creation and a 390 px mobile layout also checked in-browser.

## Files

- index.html: app structure
- style.css: responsive visual design
- app.js: simulated ranking, navigation, forms, local persistence
- serve.mjs: optional development server

## GitHub handoff

The assignment requires a private GitHub repository and a collaborator invitation for tedaueb. Sites hosting is separate and does not satisfy this requirement. Repository creation and invitation require GitHub access; do not mark the assignment submitted until both are verified.

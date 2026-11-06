# Windowkind

## The idea

Windowkind recommends a room and time for an activity based on the changing light and quiet in your home. Choose reading and a 30-minute session, compare rooms and days, then save a moment that suits you.

## Why I would use it

The same room changes through the day. I would use Windowkind to find a comfortable spot for reading, focused work or a video call without trial and error.

## What makes it distinctive

Each suggestion combines an activity, a room and a time, learning from room observations and comfort ratings. Sun-path apps exist; Windowkind focuses on choosing rooms for everyday home activities.

- Sun Seeker: https://play.google.com/store/apps/details?id=com.ajnaware.sunseeker
- Sun Surveyor: https://play.google.com/store/apps/details?id=com.ratana.sunsurveyor
- Sunnook: https://sunnook.app/

## Try the mockup

Open index.html in a modern browser, or run node serve.mjs and visit http://127.0.0.1:4173. No installation is required.

1. On Today, choose an activity and duration.
2. Select Today, Tomorrow or Saturday to compare example times.
3. Open a suggestion, read why it fits, and save it.
4. In My moments, rate comfort or remove the saved moment.
5. In My rooms, add a room or log light and noise.

Times, scores and charts are examples. There is no trained model, live data, sensor access, account connection or backend. Changes stay in this browser. Google Fonts is optional.

## Semester AI plan

**Prediction:** estimate light comfort and noise by room and time slot from time of day, window direction, season and voluntary observations. Begin with a per-room and time baseline, then evaluate a regression or classification model. Show uncertainty when data is sparse.

**Recommendation:** rank feasible room and time combinations for the activity and duration using predicted conditions and past comfort ratings. Explain the relevant factors and let users override suggestions.

**Data:** start with synthetic data, then consented observations. Avoid precise location and audio recordings. Provide export and deletion before collecting real data.

**Evaluation:** use chronological train and test splits, and compare with fixed schedules and the most-used-room baseline. Measure prediction error, calibration, comfort ratings and recommendation acceptance.

## Verification

Checked JavaScript syntax and the main click paths: day and activity selection, duration, recommendation detail, saving, feedback and room management. Checked the 390 px phone layout.

## Files

- index.html — app structure
- style.css — responsive design
- app.js — interactions, example ranking and local storage
- serve.mjs — optional local server

Δες το [README στα ελληνικά](README.md).
# AB-29 Training — Personal training log

A self-contained black-and-gold training tracker. Upload `index.html` to GitHub Pages; no installation or build is needed.

## Put it online with GitHub Pages

1. Create a GitHub repository for your tracker.
2. Upload `index.html` into the top level of the repository and commit it.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select your branch (usually `main`) and **/(root)**, then save.
6. GitHub will show your published address on that page once deployment finishes. Open that address on your training phone and bookmark it.

Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## Use the tracker

- **Train:** choose a session, start, record your weight/reps or time/distance, and tick off each set or step. Your inputs and current exercise save as you go. Finish to add the session to History.
- **Sessions:** edit the six starter templates or create your own. Targets are instructions; changing the target text does not change the number of logging rows. Set the **Sets / steps** field as well.
- **History:** review earlier sessions, export a backup, or restore one. The workout screen shows the most recent completed sets for an exercise with the same name.
- You can finish a partially completed workout. It will clearly retain the sets that were not completed.
- The rest timer uses elapsed clock time. It does not send background notifications. Workout duration is elapsed time between starting and finishing, including breaks or time away.

## How memory works

Data is stored in this browser's local storage, for the site's address. No training data is uploaded to GitHub. There is no account, online database or automatic cross-device sync.

Use the same address and browser each time. Clearing website data, using private browsing, changing device/browser or moving to a different domain can make your history unavailable. Export backups regularly using **History → Export backup**, and keep them in your own cloud drive. Restore replaces the current tracker data after confirmation. A backup includes custom sessions, history and any workout in progress.

Opening this file directly can work for a preview, but browser storage for local files varies. Use the GitHub Pages address for ongoing training. Export any preview history and restore it at the published address. The page has no external dependencies; offline reopening is not guaranteed because this version has no offline installation support.

For automatic phone/laptop syncing, a later version can add sign-in and a hosted database with private per-user access. The HTML would still be hosted on GitHub Pages. That requires separately configured storage; this version does not pretend to provide cloud sync.

## Garmin

This version is not connected to Garmin. Garmin provides an Activity API for receiving activity data and a Training API for sending structured workouts and plans through its developer programme. A real integration requires developer access and a separate cloud service; the backup JSON from this tracker is not a Garmin import file.

Garmin documentation: https://developer.garmin.com/gc-developer-program/overview/

The starter sessions are editable examples, ready to replace with your preferred programmes and equipment.

## Your session library update

The dropdown now includes **Push, Pull, Upper and Legs**, transcribed from IMG_8935–IMG_8948. Each exercise has an expandable screenshot reference with the original sets, weights, reps, RPE and rests. Today's logging fields remain blank until you enter your actual results. RPE is optional and saved in history. Rest buttons beside each lifting set match the screenshot.

- Push: 6 exercises / 18 sets.
- Pull: 6 exercises / 19 sets.
- Upper: 7 exercises / 23 sets.
- Legs: 6 exercises / 19 sets.

The two Pull screenshots show different pulldown and chest-supported-row results. Both are retained in the reference notes; their dates are not visible, so neither is labelled as the latest. Blank weights and RPE stay blank. The screenshots do not establish whether dumbbell weights are per hand or combined, so the values are reproduced without conversion. Session durations are estimates. Screenshot references remain historical references when you edit future session targets.

New running sessions: Recovery 25, Easy 40, 6 × 400 m, Tempo blocks, and Long easy 60. New HYROX sessions: Engine builder, Sled & legs, Run under fatigue, and Half-distance simulation. These are original, editable training templates with warm-ups and cool-downs. Use the hard sessions as alternatives in your week and leave recovery between them. The HYROX simulation uses scaled distances in race station order; it is not an official race or division prescription. Loads are chosen by you. Cardio/station steps can record time, distance, load, reps and RPE.

Background references: [HYROX race format](https://hyrox.com/about-race/) and [Boston Athletic Association training guidance](https://www.baa.org/races/boston-marathon/info-for-athletes/boston-marathon-training/). The individual added workouts are not represented as official plans from either organisation.

Replace the existing `index.html` in the same GitHub Pages repository to update. On opening the updated page, missing new templates are added automatically; saved history, an active workout and edited sessions are preserved. Refreshing does not add duplicates. Older backups still restore, with the new session library added. Export a backup before updating as a precaution.


## Automatic workout emails

Your supplied Web3Forms access key is configured. When you finish a session, the tracker saves it locally and submits a report to Web3Forms. The recipient is the address registered to that key, intended to be adam.brook94@gmail.com. The HTML cannot verify or override that recipient.

Reports include exercise targets, every set (including uncompleted rows), weights, reps, time, distance, RPE, timestamps, elapsed duration, notes, screenshot references and the complete session as JSON in the email body. No paid attachment feature is required.

Open History → Workout emails to change the key or switch automatic sending off. Keep the page open until submission finishes. History shows Web3Forms acceptance rather than claiming inbox delivery. Failed submissions can be retried. For unconfirmed network failures, check your inbox first to avoid duplicates. Refreshing never automatically resends old sessions.

The default form key is included in the HTML for GitHub Pages use. Any override is saved in the browser separately from workout backups. Sending requires internet access and a valid Web3Forms form configuration.

Automatic submission, full report content, error handling, retries and duplicate prevention were checked using simulated Web3Forms responses. Actual inbox delivery has not been verified.

Workout Builder

A self-contained, single-file workout timer and routine builder for kettlebell and bodyweight training. Build routines from a categorized exercise library, save them, and run them with a beep/voice-announced interval timer — all in the browser, no backend required.

Live app: hosted via GitHub Pages at https://<your-username>.github.io/<repo-name>/

Features
Exercise library — ~180 built-in exercises across three color-coded categories (Kettlebell, Calisthenics, Warmups), each tagged with one or more targeted areas (Arms, Legs, Core, Shoulders, Chest, Mobility, Warmup, Full Body). Searchable, filterable by category and area, sortable alphabetically or by category. Add your own custom exercises with a name, category, areas, and description.
Workout builder — assemble a routine by adding exercises from the library, set a duration per exercise, reorder with drag-and-drop or up/down buttons, and mark any exercise to hold indefinitely (repeats its beep on interval until manually skipped, instead of auto-advancing — useful for planks and other timed holds of unknown length).
Saved workouts — save, edit, duplicate, and delete routines. Ships with four seeded default workouts (Morning Workout, Morning Workout Extended, 20-Minute Kettlebell Circuit, Stretch Routine) which can be restored to their original state at any time via Restore default workouts.
Run timer — beep on each transition, spoken exercise names via the browser's on-device text-to-speech, adjustable volume, a distinct end-of-workout tone, and a Skip control that advances immediately (including out of an indefinite hold).
Screen Wake Lock — keeps the screen from auto-locking from inactivity while a workout is running. If the screen is manually locked or you switch apps, the timer automatically pauses and announces "Workout paused" (and "Workout resumed" when you come back) using a small pre-rendered voice clip, so the countdown never silently drifts out of sync.
Offline-friendly — once loaded, no network calls are required to use the app.

Getting started

This is a static single HTML file — there is no build step.

Usage

The app has four tabs:

Tab	Purpose

Library	Browse, search, and filter exercises. Tap + to add one to your current draft. Add custom exercises via the form at the bottom.
Builder	Name and assemble a workout from your draft. Reorder, set durations, mark a hold, then Save workout or Run now.
My Workouts	Run, edit, duplicate, or delete saved workouts. Restore default workouts resets the four seeded routines without touching anything else you've built.
Run	The active timer: Start/Pause/Skip/Reset, beep and voice-announce toggles, volume, and a "Test voice" diagnostic.

Data & privacy

All workouts and custom exercises are stored in the browser's localStorage, scoped to the domain the app is hosted on. Nothing is sent to a server. This also means:

Data is per-browser, per-device — it will not sync across devices or browsers automatically.
Clearing site data/cache for the hosted domain will erase saved workouts and custom exercises.


Browser support & known limitations
Voice announcements use the browser's built-in speechSynthesis API and only play reliably while the tab is open and in the foreground — this is a platform restriction, not a bug in the app.
Screen Wake Lock (navigator.wakeLock) is supported in current Chrome/Edge/Safari on both desktop and mobile; on unsupported browsers it fails; the app still works, just without that protection.
The "Workout paused/resumed" cues use a small set of pre-rendered audio clips (Web Audio API), so they play reliably even in the exact moment the tab is backgrounded — unlike live speech synthesis at that same moment.
Tested primarily on mobile Chrome. Other modern browsers should work but haven't been extensively verified.

Credits

The "Workout paused" / "Workout resumed" voice cues were generated offline using the openly licensed Amy voice from the Piper text-to-speech project.

License

No license specified — personal project. Ask before reusing.

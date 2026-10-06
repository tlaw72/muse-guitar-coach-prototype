# Muse Guitar Coach

A lightweight interaction prototype for a persistent, multimodal guitar teacher powered by Muse.

**This is a concept prototype.** It uses simulated feedback and does not upload media or call a model API.

## Product idea

A learner records or uploads a guitar practice session. Muse analyzes the synchronized video and audio, grounds feedback to exact moments, and turns recurring mistakes into a short practice plan. Later sessions are compared with earlier ones so the coaching becomes personal rather than starting over every time.

The prototype demonstrates three parts of that loop:

1. Capture a longer practice session and state the learner's goal.
2. Review timestamped feedback on rhythm, pitch, fingering, and posture.
3. Receive targeted drills and track improvement across sessions.

## Why this is useful feedback for Muse

This experience depends on model and product capabilities that are difficult to evaluate in a short chat:

- Longer synchronized video and audio input
- Temporal grounding to musically meaningful moments
- Joint reasoning about what is heard and what is visible
- Consistent coaching across multiple sessions
- Actionable exercises rather than a generic performance summary
- Privacy controls and predictable retention for personal recordings

## Try the prototype

Open `index.html` in a browser, or use the published GitHub Pages link in the repository description. Select **Load sample session**, then move between **Review** and **Practice plan**.

## What a real implementation would need

- Chunked/resumable media upload for 10–30 minute sessions
- Audio/video synchronization preserved through inference
- Timestamped structured output such as `sample-feedback.json`
- User-controlled long-term memory for goals and recurring issues
- Clear deletion, retention, and privacy controls
- Evaluation against teacher annotations for timing, note, technique, and posture feedback

## Success criteria

- At least 80% of surfaced issues point to a relevant timestamp
- Feedback distinguishes audible mistakes from visible technique issues
- Each session produces no more than three prioritized exercises
- Progress claims cite comparable evidence from previous sessions
- The user can delete both recordings and derived coaching memory

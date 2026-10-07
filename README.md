# Muse Live Guitar Coach

A lightweight interaction prototype for a persistent, real-time multimodal guitar teacher powered by Muse.

**[Open the live prototype](https://tlaw72.github.io/muse-guitar-coach-prototype/)**

**This is a concept prototype.** It simulates a live camera-and-microphone lesson and does not transmit media or call a model API.

## Product idea

A learner starts a live lesson and practices naturally while Muse listens and watches. Muse gives short, well-timed cues without constantly interrupting, keeps a rolling replay buffer for evidence, and turns recurring mistakes into a focused practice plan. Later lessons build on earlier ones instead of starting over every time.

The prototype demonstrates three parts of that loop:

1. Start a live camera-and-microphone lesson and state the learner's goal.
2. Receive low-latency cues about rhythm, pitch, fingering, and posture while playing.
3. Replay the relevant few seconds, then receive targeted drills when the lesson ends.

## Why this is useful feedback for Muse

This experience depends on model and product capabilities that are difficult to evaluate in a short chat:

- Continuous synchronized video and audio streaming
- Low-latency temporal grounding to musically meaningful moments
- Joint reasoning about what is heard and what is visible
- Interruption-aware coaching that knows when to speak and when to listen
- A rolling evidence buffer and consistent coaching across lessons
- Actionable exercises rather than a generic performance summary
- Privacy controls for live media, temporary buffers, and retained coaching memory

## Try the prototype

Open `index.html` in a browser, or use the published GitHub Pages link in the repository description. Select **Start simulated live lesson**, then move between **Live coaching** and **Lesson plan**.

## What a real implementation would need

- A low-latency, long-running audio/video session transport
- Audio/video synchronization preserved throughout streaming inference
- A short rolling buffer for replaying the evidence behind a cue
- Turn-taking that avoids speaking over the learner's playing
- Structured live events such as `sample-feedback.json`
- User-controlled long-term memory for goals and recurring issues
- Clear indicators and controls for capture, retention, and deletion
- Evaluation against teacher annotations for timing, note, technique, and posture feedback

## Success criteria

- Useful coaching cues arrive within two seconds of the relevant musical phrase
- At least 80% of surfaced issues point to the correct moment in the rolling buffer
- Feedback distinguishes audible mistakes from visible technique issues
- Muse delivers no more than one live cue at a time and does not interrupt every mistake
- Each lesson ends with no more than three prioritized exercises
- Progress claims cite comparable evidence from previous lessons
- The user can discard the temporary replay buffer and delete derived coaching memory

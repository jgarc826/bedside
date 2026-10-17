# Bedside — AI standardized patient

Practice breaking bad news to a patient who reacts like a real person, then get a SPIKES scorecard that quotes your own words back to you.

Built in one afternoon at the DiversaTech hackathon (UC Berkeley, Oct 17 2026).

## Run it

Open `index.html` in Chrome, add an Anthropic API key under Settings, pick a scenario, and talk.

Optional: add an ElevenLabs API key for a natural, emotional patient voice. Without it the browser's built-in voice is used.

No backend, no build step. Voice input and output use the browser's Web Speech API. The patient and the grader are two prompts to the Claude API called directly from the browser. Your key stays in your browser's local storage.

## Why

One standardized-patient simulation costs about $665 per resident (Sudan et al.). Students get one to three reps in four years. A Bedside session costs a few cents.

Six scenarios across oncology, OB/GYN, neurology, pediatrics, internal medicine and critical care. Progress is tracked per student with SPIKES averages, and each debrief maps to AAMC Core EPAs and ACGME competencies.

See `PITCH.md` for the pitch and demo flow.

## Credits

Patient avatars are composed from the open-source [notion-avatar](https://github.com/Mayandev/notion-avatar) part library (MIT). Parts are swapped live to reflect the patient's emotional state.

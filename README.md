# Hi, I'm Bede

I'm the founder of **ConvertEcho**, and we build AI voice agents that help service business owners stay on top of their calls and leads while they're busy doing the work. They call new leads within minutes of a form fill, answer every call day and night, qualify the caller, and book the job straight into the CRM calendar.

Each build handles the whole job, from the first ring to the booked appointment and the notes in the CRM. If something goes wrong, like a booking that doesn't go through, the system catches it and lets a person know, so no lead gets lost.

**Stack:** LiveKit Agents, OpenAI GPT-Live-1, Telnyx AI Assistants, Retell AI, n8n, GoHighLevel, Redis

## Voice agent builds

### Self-hosted on LiveKit and GPT-Live-1

- **[Desert Comfort HVAC: AI receptionist](https://github.com/Bedeeric98/desert-comfort-hvac-receptionist-livekit)**: Answers day and night, rates how urgent the AC problem is from the indoor temperature, quotes the matching fee and books the visit. Code backstops catch what the model misses, every webhook is authenticated, and a watchdog alerts if the agent goes quiet.
- **[Desert Comfort HVAC: speed to lead](https://github.com/Bedeeric98/desert-comfort-hvac-speed-to-lead-livekit)**: Dials new leads two minutes after they submit a form and stays silent until a person answers, so it never talks into a voicemail. Leads who don't pick up get a second call, a text and a third call.

### Telnyx AI Assistants

- **[SunPath Solar: speed to lead](https://github.com/Bedeeric98/sunpath-solar-speed-to-lead-voice-agent)**: Calls solar leads, qualifies them on home ownership, roof control and electricity bill, and books a consultation. It recovers on its own when the end-of-call webhook never arrives, and scans every transcript for manipulation attempts.
- **[Windy City Plumbing: appointment reminders](https://github.com/Bedeeric98/windy-city-plumbing-appointment-reminder-voice-agent)**: Confirms, reschedules or cancels appointments during the call. A guard stops a misheard answer from cancelling a real appointment.

### Retell AI

- **[Rodriguez & Martinez Law: inbound agents](https://github.com/Bedeeric98/retell-rodriguez-martinez-law-voice-agent)**: Looks up every caller before the agent speaks. New callers are qualified against the firm's rules and the statute of limitations, then booked. Existing clients are greeted by name and warm-transferred to their lawyer.
- **[Lone Star Insurance: renewal calls](https://github.com/Bedeeric98/retell-lone-star-insurance-voice-agent)**: Calls clients 60 to 90 days before renewal, checks for life changes and whether their coverage still fits, and books a policy review with their agent when it doesn't.
- **[Permit-expediting receptionist for a Florida permitting company](https://github.com/Bedeeric98/retell-permit-receptionist-voice-agent)**: Spots urgent cases such as stop-work orders, violation notices and deadlines two weeks away or sooner, and warm-transfers them with a briefing for the specialist. Everyone else is qualified for a callback.
- **[Lead qualifier for a commercial drywall contractor](https://github.com/Bedeeric98/retell-construction-lead-qualifier-voice-agent)**: Works out what each caller needs, collects the project scope for single-family, multi-family or commercial work, and logs every qualified call to Google Sheets.

## How I test

I've run 300+ live test calls across three builds and keep a 34-scenario regression suite built from the bugs those calls found. I also built a QA rubric with an audio-based LLM judge, calibrated it against 10 hand-scored calls, and used it to score test calls and track down real bugs. The method is in [voice-agent-evaluation](https://github.com/Bedeeric98/voice-agent-evaluation).

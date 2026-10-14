# Select a focused test set

Use only dimensions relevant to the product and tenant. Keep scenarios synthetic
unless sourced from authorized history, and vary followup messages based on the
actual bot reply instead of treating a conversation as disconnected prompts.

| Area | Useful pressure or regression case |
| --- | --- |
| Pricing | Direct request, repeated demand, unauthorized discount, billing period |
| Tone | Rude refusal, boastful challenge, anxious beginner, repeated reassurance |
| Booking | Already-stated availability, rejected dates, month/year boundary, unavailable date |
| Eligibility | Exact boundary ages, parent pressure, attempted paid/coach exception |
| Knowledge | Known answer, genuinely unknown policy, conflict with new owner instruction |
| Handover | Person requested, unresolved billing, private training, no unsupported response deadline |
| Followup | Busy now, specific future time/timezone, opt out, person already replied |
| Short replies | Greeting, direct booking intent, no minimum word count, details only when asked |
| Persistence | Remember name, age, selected program, rejected times, and corrected preference |
| Identity | Consistent business role; truthful response if explicitly asked about automation |

For style changes, test the original exchange and a different set of dates so an
example does not become fixed availability. Test an explicit request for detail to
ensure brevity instructions have not suppressed useful answers. A short month is
useful at month boundaries; a year may be needed at a year boundary. These are
tenant style choices, not universal GHL requirements.

Fifty cases can reveal recurring failures without proving that all action effects
work. More cases are useful when they add missing coverage or test variability;
repeating easy greetings alone adds little confidence.

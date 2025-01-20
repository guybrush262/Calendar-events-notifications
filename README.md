I created an automation that checks your calendars event and advise me at home (if I am home and it's "day" time) or on the phone (if I'm not home or I'm out of home).
If in the event is reported a location, the notification is done 15min + commute time before the event start time, otherwise just 15min before the event start time.

The following integrations are propedeutical for doing that:
- Google Calendar
- Google Maps Travel Time

So I created:
- "input_text.ultimo_evento_notificato" in which the last notified event is reported. Updated through the automation.
- "sensor.commutetime_evento_calendario" in Google Maps Travel Time to record the commute time from my current location to the next calendar event one.
   
Then I integrated everything in the automation.

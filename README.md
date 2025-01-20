I created an automation that checks my calendars event:
- if I am home and it's "day" time, it advises me on the home speaker (I used a separated script, because in this way it advises me in the room that I am thanks to the presence detection sensors), or
- I'm not at home or it's night time, it advises me on the phone app
In particular, if in the event is reported a location, the notification is done 15min + commute time before the event start time, otherwise just 15min before the event start time.

The following integrations are propedeutical for doing that:
- Google Calendar
- Google Maps Travel Time

So I created:
- "input_text.ultimo_evento_notificato" in which the last notified event is reported. Updated through the automation.
- "sensor.commutetime_evento_calendario" in Google Maps Travel Time to record the commute time from my current location to the next calendar event one.
   
Then I integrated everything in the automation.

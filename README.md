# Caendar Events Notifications in Home Assistant

The automation checks the calendar events and:
- If I am home and it's "day" time, it advises me on the home speaker (I uses a separated script, because in this way it advises me in the room that I am thanks to the presence detection sensors); or
- I'm not at home or it's "night" time, it sends me a notification to the phone.

In particular, if a location is reported in the calendar event, than the notification is done 15min + commute time before the event start time, otherwise just 15min before the event start time. This lets me have 15 minutes to prepare to go out: e.g. if the event location is 23 minutes far by car, the notification would happens 38 minutes before the event start.
Moreover, the automation notifies about the weather condition.

The following integrations are propedeutical for doing that:
- Google Calendar
- Google Maps Travel Time

So I created:
- "input_text.last_notified_event" in which the last notified event is reported. Directly updated through the automation.
- "sensor.commutetime_calendar_event" in Google Maps Travel Time to record the commute time from my current location to the next calendar event one.
- "weather.pirateweather" weather alert with Pirate Weather.
   
Then I integrated everything in the automation.


Ancillary scripts that I use are:
- script.assistente_interruzioni_vocali (introduction message to the notification)
- script.speaker_notifica_tts_con_presenza_casa (home notification in the room that I am)
- script.smartphone_notification (simple phone notification)

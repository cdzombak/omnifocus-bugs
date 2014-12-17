(Apologies for the highly technical nature of this inquiry…)

When generating a Scripting Bridge header for OmniFocus (for scripting the app from Objective-C instead of AppleScript), I get three warnings about undefined types. I think I can still use the affected methods, but it’s probably worth fixing these in a future update:

> sdef /Applications/OmniFocus.app/ | sdp -fh --basename OmniFocus
sdp: warning: property "assigned container" of class "inbox task" refers to undefined type 'item'; assuming type 'id'.
sdp: warning: property "value" of class "tree" refers to undefined type 'item'; assuming type 'id'.
sdp: warning: property "container" of class "style" refers to undefined type 'item'; assuming type 'id’.

Chris Dzombak

## Auto reply

Your message has been assigned an ID of [OG #1282957].

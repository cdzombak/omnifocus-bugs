(Apologies for the highly technical nature of this inquiry…)

When generating a Scripting Bridge header for OmniFocus (for scripting the app from Objective-C instead of AppleScript), I get three warnings about undefined types. I think I can still use the affected methods, but it’s probably worth fixing these in a future update:

```
> sdef /Applications/OmniFocus.app/ | sdp -fh --basename OmniFocus
sdp: warning: property "assigned container" of class "inbox task" refers to undefined type 'item'; assuming type 'id'.
sdp: warning: property "value" of class "tree" refers to undefined type 'item'; assuming type 'id'.
sdp: warning: property "container" of class "style" refers to undefined type 'item'; assuming type 'id’.
```

Chris Dzombak

## Auto reply

Your message has been assigned an ID of [OG #1282957].

## Human reply, 2014-12-18

Hey Chris, thanks for writing to us, and happy Thursday! 

Unfortunately we aren't able to offer specific scripting support, but if you run into trouble you can always peruse our forums and see if other users can help! <https://discourse.omnigroup.com/c/omnifocus/omnifocus-applescript>

I've filed a bug report with the warnings you ran into to let our engineering team know about them, thanks for sending them to us!

If you have any other questions or suggestions, please don't hesitate to let me know. Thanks for your support, we really appreciate it!

Best,

Christina J.
Support Human
The Omni Group

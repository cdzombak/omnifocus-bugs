## Initial Email

**Subject:** Copy as Link doesn't work - OmniOutliner 4.5 (v177.7.2.0.255747) Feedback (pro license XYZ)

In this version of OmniOutliner (OmniOutliner 4.5 (v177.7.2.0.255747)), copying a row as a link doesn’t seem to work.

Action: right-click a row and select “Copy as Link”

Actual result: my clipboard is cleared but there is not a URL on the clipboard

Expected result: a URL like “omnioutliner:///xyz” is copied to the clipboard

Thanks,
Chris Dzombak

## Auto Reply

Your message has been assigned an ID of [OG #1548239].

## Human Reply

Hey Chris, thanks for writing to us, and happy Thursday! 

Apologies for the trouble here! I wasn't able to replicate this issue here, though that doesn't mean this isn't happening to you! Can you tell me which version of OS X you're currently running? 

If possible, would you be able to send me a screen recording that shows this in action?  

You should be able to create a screencast using QuickTime Player.  To do that, click the Spotlight menu bar helper icon in the top right corner of your screen, search for QuickTime and launch it from the search results.  Then select File > New Screen Recording from the menu bar and click the red record button.  At that point you should be able to choose whether to record the entire screen or just a specified portion of it.  Once recording has begun, select a row, copy as link and attempt to paste that link elsewhere int the document. When you’re done, click the stop recording icon in the menu bar, and use QuickTime Player’s "File > Save…” option and send the resulting file in to me by uploading it to our secure upload site here: <https://upload.omnigroup.com>

This Apple support article also contains more detailed information about how to take a screen recording:
<http://support.apple.com/kb/PH5882>

Let me know after you’ve uploaded your video and I'll see if I can determine what's going wrong here.

Looking forward to your reply!

Best,

## My Reply

Happy Thursday!

A screen recording is available here: https://dropbox.dzombak.com/omni/2016-03-17%20outliner%20copy%20as%20link.mov

While recording that, I noticed I actually can paste the link back into OmniOutliner but _not_ into applications expecting plain text (like nvALT or Sublime Text). I typically only use these links in plain text documents. I suspect this difference will be useful in debugging.

I am running OS X 10.11.3.

Thanks,
Chris

## Human Reply

Chris,

Thanks for sending that over! I've filed a bug about this behavior for our engineers to investigate, but I'm not sure if it's ultimately something we'd be able to address; it sounds like those third party target apps aren't looking for the "type" of content on the pasteboard, which is why when you paste in those apps nothing happens. 

As a potential workaround, you could paste the link in OmniOutliner and copy that content and paste in another app? I tested this out and it works with sublime text and nvALT. I realize it's not the best workflow, but wanted to offer that idea in case it helps in the meantime!

If you have any other questions or suggestions, please don't hesitate to let me know. Thanks for your support, we really appreciate it!

Best,

## My Reply

Thanks, _name_.

I do hope this is something that can be addressed. I can copy and paste text from other apps as expected, and even copying a link from OmniFocus into these apps works as I expect. OmniOutliner is the outlier.

Thanks,
Chris

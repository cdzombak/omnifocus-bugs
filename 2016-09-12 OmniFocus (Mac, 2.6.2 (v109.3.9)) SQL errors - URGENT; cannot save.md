## Initial Tweets

<blockquote class="twitter-tweet" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/OmniFocus">@OmniFocus</a> and if I try to quit, it asks me if I want to save my document; saying Save results in <a href="https://t.co/oUHOx0uy6o">pic.twitter.com/oUHOx0uy6o</a></p>&mdash; Chris Dzombak (@cdzombak) <a href="https://twitter.com/cdzombak/status/775421797877460993">September 12, 2016</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Initial Email

**Subject:** OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save

I am seeing SQL errors like the attached (screenshots) after I make changes in OmniFocus today. Changes that trigger this are things like moving an item, completing one, or opening a new window.

Trying to quit OmniFocus alerts me that my OmniFocus document hasn’t been saved. Clicking Save results in another, similar error.

Additionally, recent changes on my Mac are *not* syncing to my iOS devices.

Chris Dzombak

![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 15.13.03.png)
![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 15.41.59.png)
![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 15.51.13.png)
![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 15.51.18.png)
![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 15.51.24.png)

## Auto Reply

_An autoresponse was not received._

## Human Reply

_This ticket was assigned OG #1633470 with this message._

Hi Chris,

I'm sorry for the trouble here! 

Are you running any clean-up applications on your Mac? Apps like MacKeeper and CleanMyMac delete OmniFocus' cache while it's running, creating problems like the one you're experiencing. We generally recommend that customers don't use clean-up apps, as their benefits are questionable, but regardless you should never run a clean-up while OmniFocus is running.

Unfortunately, you'll need to quit and restart OmniFocus to get around the error, but once you've done that you shouldn't see it again. 

If you are not running a clean-up application on your Mac, I'd like to have you try deleting the OmniFocus cache yourself. OmniFocus will recreate it upon launch. Here are the steps to do so:

1. Quit OmniFocus
2. Switch to the Finder
3. Hold down the Option key and go to Go>Library from the top menu bar in Finder
4. In the new Finder window that appears navigate to: Library > Caches
5. Inside the Caches folder delete this folder: com.omnigroup.OmniFocus
6. Relaunch OmniFocus

I hope this helps! Please let me know if you have questions or get stuck. 

Sincerely,

## My Reply

> Are you running any clean-up applications on your Mac? Apps like MacKeeper and CleanMyMac delete OmniFocus' cache while it's running, creating problems like the one you're experiencing. We generally recommend that customers don't use clean-up apps, as their benefits are questionable, but regardless you should never run a clean-up while OmniFocus is running.

No, I’m not using any such tools.

> 1. Quit OmniFocus

When I try to quit, it asks me first,

> Do you want to save the changes made to the document “OmniFocus”?

If I click Save, it then asks me,

> This document’s file has been changed by another application since you opened or saved it.
> The changes made by the other application will be lost if you save. Save anyway?

Since I don’t know what would’ve touched this document aside from OmniFocus, I opt to Save anyway, since the document OmniFocus is working with is correct.

This results in 4 more of the "The document “OmniFocus” could not be saved. Unable to run SQL for statement 'BEGIN EXCLUSIVE’.” message and OmniFocus doesn’t quit.

What should I do?

## Human Reply

Hi Chris,

Hmmm,  I'm not sure what might have caused the cache problem if another app isn't a likely culprit. Were you perhaps doing any other system maintenance, or running two copies of the app simultaneously temporarily?

I've asked around and it doesn't seem like there's a way to get around the Save dialog other than force-quitting OmniFocus. It sounds likely that you'll lose some recent work—I really am sorry about that. For what it's worth, I've never seen this error outside of the situations I've previously described so I don't expect you to encounter it again. We can definitely look into the problem further if you send us your Console.log. Judging by your Twitter profile I'm guessing you're familiar with the process, but in case you're not: Open Console (in your Applications > Utilities folder) and then File > Save a Copy As... and attach the result to a reply.

Thanks again, and sorry again—

## Tweet from Ken

<blockquote class="twitter-tweet" data-conversation="none" data-lang="en"><p lang="en" dir="ltr"><a href="https://twitter.com/cdzombak">@cdzombak</a> The only time I’ve seen this happen is when another app reaches into our sandbox and deletes our SQL database. Use a cleaning app?</p>&mdash; Ken Case (@kcase) <a href="https://twitter.com/kcase/status/775462798360850432">September 12, 2016</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## My Reply

> Were you perhaps doing any other system maintenance, or running two copies of the app simultaneously temporarily?

I wasn't doing any maintenance, and I am pretty sure I wasn't running two copies of OmniFocus (certainly not intentionally).

> I've asked around and it doesn't seem like there's a way to get around the Save dialog other than force-quitting OmniFocus.

Thanks for confirming that step was necessary. I force-quit OmniFocus and removed its Caches directory (`com.omnigroup.OmniFocus2.MacAppStore`, for the MAS version of the app). As expected, this lost my changes from the mid-afternoon onward.

Now, all my OmniFocus attachments seem to be 0 bytes in size. (Screenshots attached.) This previously happened to me on August 25, for no apparent reason; see OG #1626010.

As I did then, I went ahead and tried "rebuild database", which seems to have helped.

I will emphasize that seeing this many problems in such a short timespan has substantially eroded my confidence in OmniFocus.

I've attached OmniFocus logs from the Console covering the affected timeframe (this afternoon and evening).

Thanks,
Chris

![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 20.37.10.png)
![](2016-09-12 OmniFocus (Mac, 2.6.2 (v109.3.9)) SQL errors - URGENT; cannot save/Screen Shot 2016-09-12 at 20.37.17.png)

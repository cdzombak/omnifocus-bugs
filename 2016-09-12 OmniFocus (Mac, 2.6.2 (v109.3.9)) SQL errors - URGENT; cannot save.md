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

## Human Reply

Hi Chris,

Thanks for the extra info, and for your patience. As you might have gathered from Ken's tweet, this really isn't something we have seen before without the influence of a "bad OS citizen" so my hope is that we can get to the bottom of it and restore your confidence.

An engineer and I looked at the console logs and it seems like at least the zero-byte attachments are caused by OmniFocus not being able to read the root transaction inside your database in order to get their true sizes. This results in console messages containing errors like:

   Unable to open zip archive 00000000000000=pIo9PZq5k8M+jZo4rSn9805.zip.

If you inspect this file manually, are you unable to unzip it? It should found in the location:

   ~/Library/Containers/com.omnigroup.OmniFocus2/Data/Library/Application Support/OmniFocus/OmniFocus.ofocus

Using Go > Go To Folder... in Finder (or ⇧⌘G) is probably the easiest way to get there. 

Sincerely,

## My Reply

> An engineer and I looked at the console logs and it seems like at least the zero-byte attachments are caused by OmniFocus not being able to read the root transaction inside your database in order to get their true sizes.

That makes some sense — over the past couple of months I have seen sporadic "disconnected root transaction" error messages on various devices. I typically click "repair" on that dialog when it appears.

In this case, I resolved it by telling OmniFocus on the Mac to rebuild its database (per directions from OG #1626010, the first & most recent time this happened to me).

> As you might have gathered from Ken's tweet, this really isn't something we have seen before without the influence of a "bad OS citizen" so my hope is that we can get to the bottom of it and restore your confidence.

I really wish I had anything more to share — I wasn't doing anything out of the ordinary, just going about my usual morning/early-afternoon routine of reading email and adding & rearranging things in OmniFocus.

If you can think of anything else you want me to provide, please let me know,

Thanks,
Chris

## Human Reply

Hi Chris,

Thanks for that extra info. The timeframe of a few months is interesting, because we added some code to "re-stitch" disconnected transactions around that time. We're actually removing that code in the next release due to some problems other than the one you're seeing, so I'll definitely be interested to hear if you see this again in v2.7 and higher. If this problem was due to the same circumstance that the removed code was originally put in place to address, you should start to see alerts that prompt you to replace your local database instead. If you do see that, could you reply to this ticket and let me know? The debug information that comes along with that error might help us track down the root cause of your recent trouble.

Thanks again! 

## My Reply

I will keep an eye out for alerts like that.

That's interesting, because before thsi spring, I can recall being asked on a few occasions to replace the database on one or another of my devices.

Is it possible there's some recurring or persistent glitch in _my_ database in particular that's causing this to happen every couple of weeks/months?

## Human Reply

Hi Chris,

It's more likely to be a specific usage pattern than a corrupted database, but I'd be happy to take a look to make sure. If you're syncing with our server, the easiest way to do that is for you to give me explicit permission to download a copy of your user account directory from the DAV server directly. A reply to this email indicating that permission is all we need there.

Sincerely,

## My Reply

I am syncing with your server and I'll give you permission to do that to check for any sort of corruption.

> It's more likely to be a specific usage pattern than a corrupted database

Do you have any hints about usage patterns to avoid, in order to avoid things like this?

Thanks!
Chris

## Human Reply

Hi Chris,

`###` is stuck in meetings all day, so I'm jumping in. I don't see any obvious problems with the database structure on the server. However, it is encrypted, so I can't check anything beyond the sync transaction history and the registered sync clients. 

Did you get a chance to try manually unzipping this file? N.B.: It'd be best to make a copy of the file and move it to a different location before trying, so as not to affect the active database.

~/Library/Containers/com.omnigroup.OmniFocus2.MacAppStore/Data/Library/Application Support/OmniFocus/OmniFocus.ofocus/00000000000000=pIo9PZq5k8M+jZo4rSn9805.zip

One theory is that there might be some compression problem in that file, so if you get any errors trying to open that file, please let me know before proceeding. It should contain at least a "contents.xml" file, and likely also a folder named "data". The "data" folder will only be there if you have embedded attachments in the database.

If that file does expand without any problems, I'd suggest using this procedure to compact and rebuild the database, which should also reset all the sync history. 

Please note -- this procedure will compact and rebuild the database on one of the Macs and then replace all the other databases with the rebuilt one, so before proceeding you'll want to be certain that is okay.

These instructions are specific to OmniFocus 2.6.2 or later for Mac.

- Export the OmniFocus database by selecting: File > Export...
- Make sure to change the File Format popup menu to "Backup Document (OmniFocus)"
- Double-click that file
- When the new window opens in OmniFocus click "Revert to this backup" in the upper right corner 
- Wait for it to finish
- It should automatically push out to your other devices, but if prompted on the other sync clients choose to "Keep Sync Database"

Regarding usage patterns, to prevent runaway accumulation of sync transaction files OmniFocus automatically unregisters sync clients if they don't sync for 3 weeks. We added some code (since removed in 2.7) that would try to re-stich sync clients that had only recently been unregistered. Do you have any devices that potentially didn't sync with OmniFocus for about 22 days? 

Sorry again for all the trouble here. Please let me know if you have any questions!

Best regards,

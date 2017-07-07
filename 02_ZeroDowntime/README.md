### CHAPTER 2

# ゼロダウンタイム

Any improvement that you can make toward the reduction of your batch size that consequently leads to a faster feedback loop is important.
When you begin this continuous improvement, sooner or later you will reach a point at which you can no longer reduce the time between releases due to your maintenance window—that short timeframe during which you are allowed to drop the users from your system and perform a software release.

Maintenance windows are usually scheduled for the hours of the day when you have the least concern disrupting users who are accessing your application.
This implies that you will mostly need to perform your software releases late at night or on weekends.
That’s not what we, as the people responsible for owning it in production, would consider sustainable.
We want to reclaim our lives, and if we are now supposed to release software even more often, certainly it’s not sustainable to do it every night of the week.

Zero downtime is the property of your software deployment pipeline by which you release a new version of your software to your users without disrupting their current activities—or at least minimizing the extent of potential disruptions.

In a deployment pipeline, zero downtime is the feature that will enable you to eliminate the maintenance window.
Instead of having a strict timeframe with in which you can deploy your releases, you might have the freedom to deploy new releases of software at any time of the day.
Most companies have a maintenance window that occurs once a day (usually at night), making your smallest release cycle a single day.
With zero downtime, you will have the ability to deploy multiple times per day, possibly with increasingly smaller batches of change.
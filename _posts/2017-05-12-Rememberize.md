---
layout: post
title:  "Rememberize"
author: "Steven"
---





Rememberize is an app that allows you to create lists that can help you learn a new language, study for a test, hold your thoughts, or form new habits. Each item in the list acts as a flashcard that will be shown in the notification area every time you open your lock screen. This helps users remember and memorize lists by using a spaced repetition learning technique.

[Download App](https://play.google.com/store/apps/details?id=com.tuccilabs.rememberize)

## Why I built it?

I tried to build an app that people really needed to help them learn things on the go. The biggest problem with other productivity apps is that they require you to go into the app and spend time browsing around. The issue is that users are not willing to open their apps every time when they are moving around or working. People glance at their phones all the time to look at the time, but they do unlock the phone and open apps when they are moving. Rememberize solves this problem, by showing a quick and simple notification on the lock screen for users to quickly read, retain, and swipe. Once the notification is swiped, a new notification will appear showing another list item for them to read.

##  The Challenges

The app is incredibly simple but powerful. Though the app works great there was definitely a bunch of challenges I faced while developing it.

Integrating Google’s Material Design was important to the whole user experience. Android users expect great design and common patterns they find in other great apps, so building Rememberize had to make users feel like they already knew what was going to happen with they performed an action.

Incorporating dynamic colors and themes was an unbelievably hard thing to do in Android. Changing the color of text fields, scrollbars, and list fades is almost down right impossible to do on the fly. Android allows users to have a defined color palette in xml, but modifying the colors of components that are not defined in the xml is tedious and requires some ugly workarounds.

Since users would use the notifications differently depending on each list, I had to create exhaustive settings for each list. Programming all the different settings and how those settings interact with each other caused lots of headaches, but it was worth the time and effort implementing this feature.

Like any project, there are always the small things that seem easy when thinking about it, but on further inspection small things that should have taken a day, took weeks. Overall I am extremely happy about the end product. I plan on continually fixing bugs, making the user experience better, and I have some big features coming in the next version.

## The Outcome

{:.row}

![](/assets/rememberize/feature.jpg){: .col-12}
![](/assets/rememberize/lock screen.jpg){: .col-4 }
![](/assets/rememberize/edit list.jpg){: .col-4 }
![](/assets/rememberize/single list.jpg){: .col-4 }
![](/assets/rememberize/list settings.jpg){: .col-4 }
![](/assets/rememberize/search.jpg){: .col-4 }
![](/assets/rememberize/edit list item.jpg){: .col-4 }


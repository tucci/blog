---
layout: post
title:  "Today's Holiday"
author: "Steven"
---



<!-- [Download App](https://play.google.com/store/apps/details?id=com.tuccilabs.rememberize) -->

The Today’s Holiday app catalogues over 1000 weird and wacky holidays. It allows users to find holidays either by searching or by selecting a specific day. The today’s holiday app is a great way to discover new holidays you never you existed.

## Why I built it?

I came up with the idea for Today’s Holiday because I saw there was a day called “Talk like a pirate day”. I thought this was pretty ridiculous but really funny, so I wondered if there were more days like this. When I researched, I found a lot. There was so many that everyday there was something. I look on the Google play store for an app that catalogued all these days and there was none. So I made my own app that lists all the holidays.

##  The Challenges

While building this app I came across the difficult problem of trying to find all the holidays. I had to look all over the internet for the days and which days they fell on. Doing this manually was time consuming and painful, so I had to create a web scraper to grab some holidays and output them in a json file. Since I grabbed holidays from multiple sources, a lot of the holidays were duplicated or written in a different way.

For example, a holiday would be named National Cookie day and International Cookie day. This was extremely annoying to fix. I tried my best to use regular expressions to filter similar holidays out, but still it wasn’t perfect. In the end I add to manually go through 1000 holidays to remove duplicates. Even today, there are some duplicate holidays that I missed that are in the app. I plan to fix these issues when I have time or when I update the app.

Another big issue with holidays is that certain that they do not happen on the same day each year. Some holidays only happen on the second Monday of a certain month or third Saturday, and so on. Solving this problem was frustrating, but I knew it had to be done. I looked to see if the native java classes had this functionality built in, but there was nothing. So I had to create my own algorithm to handle these special cases.

Anything to deal with dates or time in programming is always a hassle, but these things do not stop me from building products that I want and love.

## The Outcome

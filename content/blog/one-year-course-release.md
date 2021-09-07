---
title: "The Five Most Important Persons"
date: 2021-09-04T09:15:58+02:00
slug: ""
description: ""
keywords: []
draft: true
tags: []
math: false
toc: false
---

Post Course Launch - Learnings After One Year

Running the first paid online course for a year

It's been a year since I've launched my first paid 

Continue reading to learn about my journey, mistakes and things I would have done differently.

DISCLAIMER: All the linked tools are in use and I paid the price to figure out which one fits perfect (for me). I'll get a small cut if you decide to use them. 

Lean technical setup yet full control over the audience.

## The Initial Strategy

Develop a real-world course application. Enhance it with an excellent test suite and talk about it.

And with real-world I mean a sophisticated application that connects to various infrastructure componenents. This is where it becomes tricky. Everyone can test the `add` method of a `MyCalculator` class. But how to write a end-to-end test that involves a OIDC Login, database access and REST API call to a remote system?

There isn't much content out there that talks about testing. All those articles that talk about shiny new technology and tools to develop applications rarely touch this topic.

That's not helpful at all. You visit such a article, copy the interesting parts to apply it to your project at work ...

and now, what?

How do I now test this?

I strongly believe that as soon as you have the knowledge about the different tools & libraries and recipes at hand, testing become joyful.

It's the HOW that's important here.

Packed with this mission, my plan was to incrementally work on this project.

As I haven't done anything similar before, recording everything upfront would be hell of work. And as testing and agile teaches, you want early feedback. 

Let's see how this journey went out.

## Finding a Topic To Talk About

I've been writing blog articles for over three years. There wasn't any clear direction as I wrote about several Java Framework. 

I had no niche topic yet.

Over the years, I found my niche by blogging more and more about the same topic: testing Spring Boot applications.

After writing `text/plain` for some years, the next natural step is to record a first video. 

I gave it a shot and uploaded a video on YouTube. The audio was suboptimal, but it was a big step out of the comfort zone. I got to know what it takes to record and edit nice-looking videos.

## Creating The Course Content

I've recored everything on an Ubuntu 20.04 and used the following tools:

For the microphone I was using:

- Link

Perfectionism will kill your progress

Get some first touchpoints with recording video and audio on YouTube.

For this course I did only record my screen and my voice. No fancy greenscreen setup. This can come.

The benefit of this approach is that you can have as a many mispellings and just have to reiterate.

For each course chapter - I'm structuring my courses like Module -> Chapter -> Lessons - I did some initial brainstorming using a Markdown file. There I pointed out what techniques and recipes I want to teach.

Next I opened my IDE and started developing the application and the core.

JUST ... SHIP ... IT

If it's bad, you'll figure it out early and can adjust. That's way better than procrastinating or trying to get a pixel-perfect lessons that nobody will watch because the topic is not convincing.

## Selling the Course Content

Having the course idea and some early lessons in place, now it's time to sell the content, isn't it?

I'd actually suggest to create a minimal version of your landing page including some basic salescopy first.

This helps to get an early target audience. Even though you don't have your full checkout process in place, put a form for your newsletter on your landing page and tag those subscribers coming from that landing page. These might be your first customers.

Creating the sales page first also helps to think about the benefits and gains of your course ahead. This gives clarity when you do your detail planning.

And now?

As I'm heavily using the plugin suite of Thrive Theme (costing $277 a year - If you're using WordPress, it's a must-have), using their online course plugin Thrive Apprentice seemed like a natural choice. It uses the WordPress user management for access control and you can connect various eCommerce providers that'll grant access after the purchase via a webhook.

I'm using SendOwl for this purpose which is intuitive, simple and fulfill all my needs (monthly $26 costs)

"Deploy your features with more confidence while joyfulling testing your application due to recipes"

"Early-Bird" offers. With each new batch of course lessons being uploaded, I slighty increased . If you've joined early you'd get the course for almost the price of an eBook.

- Creating the Landing Page
  

- Writing engaging salescopy
  

- Get early testimonials from the ecosystem (other well-known content creator)

Social proof from the ecosystem you're in. Check your Twitter bubble or other content creators for your niche. This will add a natural proof for your content. You're new, why should a stranger trust you?

Include a money-back guarantee. I've made bad experience myself with a money-back guarantee from another content creator in my field.

But whome to sell?

Well, selling something to a audience of size zero is.

Back then I already had a newsletter audience of 2000 people. Those people however all had different interests as my blogging areas was quite broad. That's why the unsubscribe rate once I announced this course (multiple times) was quite high. Which is okay. They weren't my target audience.

Seeing the sales coming in, I also started to create ads on various platforms. 

But this doesn't work for a ($150+) product. THe chance that a cold lead (someone who doesn't know you) will click the ad and immediately buy is quite low.

Finding the right balance for hard selling. I was (and still am) super convincend that my online course on Testing can help so many developers deploy and write code with more confidence. That's why it might have seemed a little bit aggressive in the early days. I might have screwed some visitors or newsletter subscribers. That's the price you pay for learning. 

As the sales were low in the beginning.

I still remember the exact feeling when I hit the release button for the first chapter. I left my room, had dinner with my family and checked my phone two hours later.

WTF? There are already 5 sales ...

Man, what a feeling. Someone from somewhere on the globe just bought my course at this early stage. 

## How Long It Takes

In total, the course has now 127 video lessons. All of them vary from 5 to 15 minutes.

I've never used a perfectly written script to record the videos. It as more or less half-freestyle with some notes and the target source code on a second screen.

This approach makes the recordings a little bit longer as there will be misspellings, outside noice.

As a rule of thumb, for a 30 minute video, I've recorded 45 minutes and the editing took me another 45 minutes. That makes it 90minutes of recording and editing work.

This doesn't include any preparation work, coding upfront, which will also at least take the same amount as the video is long.

You do the math.

I used my morning hours to plan the videos and record them. 

Seeing more and more coure participants, this was also a natural motivation to keep going. 

If I would have the end goal of 9hour content in mind and started my journey with the goal to record everything at once, that would have been impossible.

## Learnings After One Year

Get a first version out as soon as possible

If you're selling to EU customers, rather pick a merchant of record to sell your stuff. Take some minutes to read about VAT handling of digital goods and you'll thank me later. I'm still handling VAT for myself and the effort is reasonable. Both SendOwl and Quaderno work quite well together.

- Don't try to have the perfect tech setup from day one

- People will ask for a refund, that's fine. I have a refund rate of 1%. Most of those refunds expected a different course structure. 

- Don't expect your course participants to go throug the course immediately. That was one of the interesting findings. I for myself usually always started a course I've bougth right away. That's not the case for everybody. I still see participants that did not even start with lesson one. That's okay - they might start when they have time.

- Affiliate marketing is king. There are tons of bloggers out there that might want some extra money each month to pay their hosting/tooling bills. 

- Have compelling free content around your course topic to attract new leads.

- Small steps, start with the landing page, gather leads and re-iterate

- Support purchase power parity.

We live in a world with different purchase power and wages. Buying a course for $179 as a developer working in the valley might be totally fine. That's not the case for all other countries around the globe.

I didn't have this from day one and several visitors asked for it. My main excuse was that my eCommerce setup doesn't support it. 

I've made $ 34.674 in revenue after one year. The margin is also quite high as my only expenses are some hosting fees, marketing costs, and affiliate commissions.

The learnings were HUGE. Conversion rate, A/B testing, checkout process, learning how to sell, learning how to advertise, how to work on customer complaints etc.

Do it increcementally and start with the sales page. If you already have an audience, show them your plan and ask for their email if they'd like to get updates on it. This will give you a early indicator if there's interest in this topic.

## What I Would Have Made Differently

- Start with PPP from day one
  
The only excuse I had back then was that my eCommerce provider did not support something out-of-the-box. After some investigation, it's only required some customization on my end and I had a good-enough solution in place.

- Embed more hands-on exercises and quizzes 

I enjoy learning new techniques and tools by watching online courses. For most of the courses I've worked through I prefer to code along the speaker and immedietly try out things. When it came to exercises, I usually ignored them as they were to simple or somehow already covered by me coding along. That was the main reason to not include any specifc coding task after each lesson. Personal preference and the additional effort to come up with great exercise material.

If you are eager to learn this topic, you'll try to apply the learnings as soon as possible. Otherwise it's shallow learning and if you're not motivated, exercises might also not help much.

Code along in your pace if you prefer. I would have done this somehow differently. One of the best ways to transfer knowledge is to actually apply the learnings.

> Tell me and I forget, teach me and I may remember, involve me and I learn - Benjamin Franklin


- Start earlier

I guess this is a learning we all make after we've accomplished something outside our comfort zone. Seeing how "easy" it was in retrospect, makes us wondering why we did not start earlier.

There's so much to learn here.

## What's next?

In our fast pace development world (fortunately the Java ecosystem is not that fast pacing as JavaScript) content ages and get outdated over the years. New libraries, tools and techniques pop up that make some lessons outdated or not a best practices anymore.

That's why I'm constantly trying to be up-to-date. As the testing topic is also the main focus area of my blog that's no problem. Furthermore, projects for clients also ensure it get enough hands-on.

Whenver there's something new and worth mentioning, I'll add a new lesson to the course. If there's something otudated or I would do something entierley different, then I'll replace a video.

I also gain more knowledge over time which is worth adding to the course.

Compared to an eBook, keeping an online course up-to-date can be more effort. There's no search in replace functionality for already recorded videos. You have to find the correct spot and then either record a new video or cut the outdated scene. But fortunately, in the area I'm creating content for, there's maturity and stable APIs and libraries. 

As some course participants asked for a `plain/text` version of the online course, to find recipes and techniques more easily, I'm currently in the process of creating an eBook from the online course.

That's also a great way to attract a wider audience as not everybody enjoys learning from courses and rather prefers to read a book on the beach.

The next online course is also waiting to be created. On top of the Stratospheric eBook (From Zero to Production with Spring Boot and AWS), which I've written together with Tom Hombergs and Björn Wilmsmann, we're creating a course. Equipped with my learnings from this course launch

Now it's your turn - go for it (and let me know how it worked out)!

Philip

TODO:

- find out the release dates
- affiliate links for Vimeo, Quaderno, SendOwl, ThriveThemes
- update to latest Hugo
- check Google Analytics setup
- basic imprint and privacy policy
- cool thumbnail

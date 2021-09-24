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

Learnings From Selling My First Paid Online Course

How Much I Made After One Year Selling My First Online Course

How I Made $40k from Selling My First Online Course

--

Structure: Explain the strategy and plan and then learnings & tips

It's been a year since I've launched my first paid online course. There's a lot of things I've learned along the long the way and mistakes I've made. 

This article gives you an in-depth overview about this journey, my technical setup, the way I've planned, recorded, my sales and marketing efforts.

Background: On [my main blog](https://rieckpil.de/) I'm creating content about Java, Testing, Spring Boot and AWS. In August 2020, I launched my first paid online course: the Testing Spring Boot Applications Masterclass. This online course is an in-depth resources for deploying Spring Boot applications with more confidence thanks to an excellent test suite. The course discusses various recipes and trips & tricks to test real-world Spring Boot applications.

DISCLAIMER: Finding out the right tools and software was quite an effort. The marked links (*) are affiliate links. All the linked tools are in use, and I paid the price (mostly time) to figure out which one fits perfect (for me). I get a small cut if you decide to buy them via one of these links.

Let's get started.

## The Initial Strategy

To better understand my journey, let's take a brief look at by content creation history:

Back in November 2017, I published my [first blog article](https://rieckpil.de/summary-of-the-container-conf-2017/). While the following few articles where rather random (both in the topic and timing), I soon established the habit to constantly write about something. Since then, I've been writing articles for a range of topics mainly about Java and its framework ecosystem. Many of the blog posts where the result of my learnings at work or hands-on tutorials that I wish I had found on Google when I learned a new technology (especially Java EE).

At the end of 2019 I reached the milestone of 100 published articles on my site.

After writing `text/plain` for some years, I thought the next natural step is to also create video content.

I gave it a shot and uploaded a [first video on YouTube](https://www.youtube.com/watch?v=GM5ftYM_W90) in May 2019. The audio quality was bad and the video had black bars as I didn't record 16:9. That didn't matter to me at all as I was happy to leave the comfort zone and have _something_ uploaded. I was quite sure that the quality of every upcoming video will improve anyway.

> Perfection is the enemy of progress

With these two content platforms (blog & YouTube) in place, I continued creating content for a variety of topics. There wasn't a clear target audience I wanted to reach. Whenever a topic worth talking about popped up, I sat down and wrote about it. I usually switched frameworks between the articles and hence wasn't targeting a specific set of Java developers. 

In the last two years I naturally discovered my own content niche. I started focussing more on one specific topic instead of serving all Java developers: Testing Java and specifically Spring Boot (a common framework) applications.

The benefit of this niche is that almost nobody talks about testing in their articles. They showcase shiny new features or tools but nearly never tackle the testing part. 

That's quite frustrating if you want to apply their ideas to your project at work. You copy the relevant sections, making sure it compiles, and then hit a road block.

You know ahead that your colleagues will ask you as soon as you want to integrate your code changes: "Where are the (damn) tests?".

After creating some articles for this niche (Testing Java and specifically Spring Boot applications), I discovered that there's almost no online course that teaches this topic in a comprehensive manner and using real-world example.

Everyone can test the `add` method of a `MyCalculator` class. But how to write an end-to-end test for a modern frontend that involves a OIDC login, database access, fetching data from REST API in the background?

In short, I wanted to develop a real-world course application, enhance it with an excellent test suite and talk about it.

And with real-world I mean a sophisticated application that connects to various infrastructure components. This is where testing becomes tricky.

The intent to create an online course and strategically create blog posts around this topic wasn't there from day one. This came somehow naturally.

I strongly believe that as soon as you have the knowledge about the different testing tools & libraries and recipes at hand, testing becomes joyful.

It's the HOW that's important here.

Packed with this mission, I was highly motivated to get this project going. As I haven't done anything similar before, recording everything upfront would be hell of work. 

That's why I decided to use an iterative approach and incrementally create this course while getting feedback early on. #agileDoneRight

## Creating The Course Content

As a first step, I developed the real-world course application up-front. For the application's tech stack, I used React with TypeScript and a Spring Boot Java backend. That should mirror most of today's architectures (SPA connecting to a backend) out there.

To make the setup more advanced, I added Keycloak (identity provider for OIDC), PostgreSQL to store data, a remote REST API, and an AWS service for messaging to the mix. 

In parallel, I started to sketch out the different course modules (module -> chapter -> lesson). Throughout the course I wanted to tackle unit, integration and end-to-end testing. This gave me the natural course structure of starting at the bottom of the testing pyramid with unit testing and then working upwards until we finally write end-to-end tests in the last module.

Once the application was ready, I had already had a rough idea of what I want to showcase and talk about. I ensured to have enough code parts to demonstrate various testing techniques: secured endpoints, message listeners, database access with native queries, plain business logic to verify, etc.

While I could (and maybe should) have written the tests for the application alongside the development, I first wanted to have a working application that falls under the category of real-world and does some non-trivial tasks.

As the goal of the online course was all about testing applications, I did not record the creation of the sample application. At various lessons I explained the relevant code parts and gave an architectural overview at the beginning of the course. The overall application was sophisticated in the setup and yet simple enough to grasp.

Here's a short excerpt of the course application's main use case: Creating book reviews:

![Recorded E2E test of the main user journey](/main-user-journey-e2e-test-recording.gif "Recorded E2E test of the main user journey")

(this is an automatically recorded outcome of a end-to-end Java tests)

With my iterative course creation strategy I started with the first milestone to release the first two modules (roughly 15 course lessons). Those two modules were all about getting used to the course application and an introduction to the various unit testing libraries.

This initial goal got me started to outline the first lessons greater detail. I noted down the best practices, tips and pitfalls I wanted to show. I did not plan each an every lesson in detail and rather found a natural position to cut the recorded video. 

Next, I opened my IDE and started developing all the tests that I'll be writing and talking about in the recording. Once finished, I committed the changes to my private GitHub repository and removed the code to the bare skeleton again.

This "dry run" without recording helped me during the actual recording session. I was using two screens and on one screen I was recording my IDE and developed the tests step-by-step. On the second screen I opened the target outcome by cloning the same project twice.

I ensured to have the ahead coding quite close to the actual recording to not forget my plans.

This initial batch of work (roughly 15 lessons each 5-15 min long) kept me busy for three weeks. I usually used the morning hours to record 60 - 90 minutes of content. In the afternoon, I brainstormed the next lessons and edited the videos once the entire batch was recorded.

After uploading the outcome of each iteration, I started with the next one. I followed the exact same strategy until I had all 8 modules with 127 videos in total recorded.

If it's bad, you'll figure it out early and can adjust. That's way better than procrastinating or trying to get a pixel-perfect lessons that nobody will watch because the topic is not convincing.

## The Technical Setup For Recording

The benefit of this approach is that you can have as a many mispellings and just have to reiterate.


I've developed the course application and recorded everything on an Ubuntu 20.04 with following tools:

Recording & Editing:

- Sound
- Recording
- Editing

Development:
- private repository on GitHub
- plain `.md` files inside the repository to structure the modules and lessons
- IntelliJ IDEA:
  - use the Presenter View to record your videos (make yourself familiar with the basic IDEA shortcuts to navigate as you're otherwise lost in that view)
  - download and active Presentation Assistant plugin to show the shortcuts you're using (a lot of course students will ask):

![Presentation Assistant Plugin Example](/presentation-assistant-idea-plugin-example.png "Presentation Assistant Plugin Example")


For the microphone I was using:

- Link

As I was only recording my screen and audio, there was no need for a greenscreen, high-resolution camera and a lightning setup. If I would have set up additional equipment for recording more than just my screen, this would have postponed the time I'd have a _good enough_ recording setup.

IMHO for a technical course that's optional. Sometimes the face of the course instructor also blocks important parts on the screen. I'm anyways only hacking letters in the keyboard without much gesture. 

For a first welcome video where you greet your new course participants it might make sense to show your face to establish a stronger _connection_ with the audience.

Once I had the entire recordings for the next batch ready, I started the editing process. As a first step I extracted the audio from the recording and opened it in Audacity. There I might same adjustments to the sound (e.g. remove background noise). I took the Audacity export back to kdenlive and replaced the old audio.

Next, I started the video editting. I didn't add any fancy animations or transitions to the videos and only focussed on removing the misspellings and separating videos. So a 90 minute recording block usually resulted in 50 minute content which was splitted in up to 4-5 separate videos.

## The Technical Setup For Hosting the Course

I then uploaded the rendered videos to [Vimeo](https://share.vimeo.com/mail75) for the integration in the online course later on.

While I've worked through several courses on Udemy and similar platform myself, I encountered soon that these platforms are not the best when it comes to small course creators. While they do some marketing for your course and clearly have a big audience that search for various topics every day, their payment structure is not what I was looking for.

I was looking for an alternative. Lean technical setup yet full control over the audience.

As my blog is running on WordPress and I'm heavily using plugins of the [Thrive Suite](https://thrivethemes.com/affiliates/ref.php?id=12012), I started to investigate their online course plugin: Thrive Apprentice.

With Thrive Apprentice, I could leverage the WordPress user management to have a login area and control access to my course. The visitors also stay on my side and I have full control over the content. 

For [Thrive Apprentice](https://thrivethemes.com/affiliates/ref.php?id=12012) you need both a eCommerce Provider and a hosting solution. For the eCommerce provider, I've picked [SendOwl](https://www.sendowl.com?r=db519) as their offerings and pricing are quite reasonable (current plan is $26/month).

Once I've signed up for my [SendOwl](https://www.sendowl.com?r=db519) account, I connected both my Stripe and PayPal account to have the most common payment options.

The workflow to gain access with this setup works as the following: 

1. The potential course participant visits the landing page
2. Once they click on "Buy Now" they're redirected to a pre-checkout page (on my blog) and have to either create or log in to a course account
3. They're redirected to a SendOwl checkout page and enter their payment information
4. SendOwl redirects the user to a "Thank You" page on my blog with further information on how to get started
5. In the background (and if the user gave consent), they're added to my mailing list (Mailchimp) including order information
6. Once the order is completed, SendOwl sends a webhook to my WordPress instance and Thrive Apprentice grants access to the purchased course
7. The user can now work with the course and gets a "Welcome" email delivered to their inbox

The decision for hosting the video course lessons fell to Vimeo. They offer a feature to protect the playback of videos only on allowed hosts. This is a bit more _secure_ compared to uploading the videos to YouTube and making them private. 

## Selling the Course Content

Having the course idea and some early lessons in place, now it's time to sell the content, isn't it?

I'd actually suggest to create a minimal version of your landing page including some basic sales copy first.

This helps to get an early target audience. Even though you don't have your full checkout process in place, put a form for your newsletter on your landing page and tag those subscribers coming from that landing page. These might be your first customers.

Creating the sales page first also helps to think about the benefits and gains of your course ahead. This gives clarity when you do your detail planning.

And now?

As I'm heavily using the plugin suite of Thrive Theme (costing $277 a year - If you're using WordPress, it's a must-have), using their online course plugin Thrive Apprentice seemed like a natural choice. It uses the WordPress user management for access control and you can connect various eCommerce providers that'll grant access after the purchase via a webhook.

I'm using SendOwl for this purpose which is intuitive, simple and fulfill all my needs (monthly $26 costs)

"Deploy your features with more confidence while joyfulling testing your application due to recipes"

"Early-Bird" offers. With each new batch of course lessons being uploaded, I slighty increased . If you've joined early you'd get the course for almost the price of an eBook.

- Creating the Landing Page

For the landing page I used Thrive Architect (part of Thrive Suite) which comes with ready-to-use landing page templates.

- Writing engaging sales copy

When it comes to pricing, you'd. I used other courses in my niche as an orientation and wanted to stand out with a premium course on this topic. Nothing in the Udemy price level. 

Later on, I also added more product variations to support a S/M/XL kind-of product variety. The M-product should be your selling target

- Get early testimonials from the ecosystem (other well-known content creator)

Social proof from the ecosystem you're in. Check your Twitter bubble or other content creators for your niche. This will add a natural proof for your content. You're new, why should a stranger trust you?

Include a money-back guarantee. I've made bad experience myself with a money-back guarantee from another content creator in my field.

## How Will Buy this Stuff?

Well, selling something to a audience of size zero is.

Back then I already had a newsletter audience of 2000 people. Those people however all had different interests as my blogging areas was quite broad. That's why the unsubscribe rate once I announced this course (multiple times) was quite high. Which is okay. They weren't my target audience.

Seeing the sales coming in, I also started to create ads on various platforms. 

But this doesn't work for a ($150+) product. THe chance that a cold lead (someone who doesn't know you) will click the ad and immediately buy is quite low.

Finding the right balance for hard selling. I was (and still am) super convincend that my online course on Testing can help so many developers deploy and write code with more confidence. That's why it might have seemed a little bit aggressive in the early days. I might have screwed some visitors or newsletter subscribers. That's the price you pay for learning. 

As the sales were low in the beginning.

I still remember the exact feeling when I hit the release button for the first chapter. I left my room, had dinner with my family and checked my phone two hours later.

WTF? There are already 5 sales ...

Man, what a feeling. Someone from somewhere on the globe just bought my course at this early stage. 

## A Note on Effort

In total, the course has now 127 video lessons. All of them vary from 5 to 15 minutes.

I've never used a perfectly written script to record the videos. It as more or less half-freestyle with some notes and the target source code on a second screen.

This approach makes the recordings a little bit longer as there will be misspellings, outside noice.

As a rule of thumb, for a 30 minute video, I've recorded 45 minutes and the editing took me another 45 minutes. That makes it 90minutes of recording and editing work.

This doesn't include any preparation work, coding upfront, which will also at least take the same amount as the video is long.

You do the math. As you'll see later on, the time invest really paid off. 

In the first month or even year you might not get the traction as expected. Don't compare the invested time with your hourly rate or salary. An online course is an asset that'll (hopefully) make money while you sleep. 

I used my morning hours to plan the videos and record them. 

Seeing more and more coure participants, this was also a natural motivation to keep going. 

If I would have the end goal of 9hour content in mind and started my journey with the goal to record everything at once, that would have been impossible.

## Learnings After One Year

Get a first version out as soon as possible. This first version doesn't have to be perfect but will let you test your setup end-to-end. This works way better than preparing a "big bang" release and figuring out in the last minute that something with the payment setup is not working.

If you're selling to EU customers, rather pick a merchant of record to sell your stuff. Take some minutes to read about VAT handling of digital goods and you'll thank me later. I'm still handling VAT for myself and the effort is reasonable. Both SendOwl and Quaderno work quite well together.

- Don't try to have the perfect tech setup from day one

In the end, it's important that you're confident and have a simple (and reproducible) recording setup. You should be able to hit record in a matter of minutes without much preparation work. If you have to set up an entire conference studio for your first online course, chances are high you're procrastinating due to the effort.

I can highly recommend getting some first touch points with video and recording and editing on YouTube. YouTube is a great playground. There won't be any refunds and only helpful comments to improve.

This applies to both the technical setup for recording and selling your course. There are many decisions to make and I'd recommend that with a solution that fits your current needs. You can buy a green screen later.

- People will ask for a refund, and that's fine. 

It still remember the first month after the launch of the first version. I was so nervous about the first 30 day period and thought many would ask for a refund. This did not happen. After one year, I have a refund rate of 0.75%. Most of those refunds were due to a different expectation.

- Don't expect your course participants to go throug the course immediately. That was one of the interesting findings. I for myself usually always started a course I've bougth right away. That's not the case for everybody. I still see participants that did not even start with lesson one. That's okay - they might start when they have time.

- Affiliate marketing is king. There are tons of bloggers out there that might want some extra money each month to pay their hosting/tooling bills. 

- Have compelling free content around your course topic to attract new leads.

- Luck with the first course

I got lucky that this course hit the needs of an audience. It might have also flopped. That's fine, as long as you're finding this out early in the process.

- Small steps, start with the landing page, gather leads and re-iterate

- Support purchase power parity.

We live in a world with different purchase power and wages. Buying a course for $179 as a developer working in the valley might be totally fine. That's not the case for all other countries around the globe.

I didn't have this from day one and several visitors asked for it. My main excuse was that my eCommerce setup doesn't support it. 

I've made $ 34.674 in revenue after one year. The margin is also quite high as my only expenses are hosting fees, marketing costs, and affiliate commissions. If I'd slightly reduce my monthly costs for living, I could live from that money. That's a big relief!

The learnings were HUGE. I learned so much about tracking and optimizing conversion rates, A/B testing, checkout process, online marketing learning how to sell, learning how to advertise, how to work on customer complaints etc. This plays back to my job as a software developer

Do it incrementally and start with the sales page. If you already have an audience, show them your plan and ask for their email if they'd like to get updates on it. This will give you a early indicator if there's interest in this topic.

- Don't try to get everything perfect from day one

It's a lot of topics to handle when selling courses in the internet. You have to ensure the participants have a smooth checkout process, the access is working and your landing page has a reasonable page speed to be accessed all over the world. You can easily get lost in various parts of creating, advertising and selling your content. I usually stop when I have a good enough solution and come back later to the topic. I did not start with the most compelling (and might still have areas of improvements there) sales copy but improved it over time. There's so much do. Start small, and iterate. Don't get frustrated if somethings not working from day one. You can't find the root cause for your not-so-optimal page speed? Give your best and otherwise sleep a night over it. 

- Use IDEA shortcuts and live templates to avoid blocker while typing

## What I Would Have Made Differently

- Start with PPP from day one
  
The only excuse I had back then was that my eCommerce provider did not support something out-of-the-box. After some investigation, it's only required some customization on my end and I had a good-enough solution in place.

- Embed more hands-on exercises and quizzes 

I enjoy learning new techniques and tools by watching online courses. For most of the courses I've worked through I prefer to code along the speaker and immediately try out things. When it came to exercises, I usually ignored them as they were to simple or somehow already covered by me coding along. That was the main reason to not include any specific coding task after each lesson. Personal preference and the additional effort to come up with great exercise material.

If you are eager to learn this topic, you'll try to apply the learnings as soon as possible. Otherwise it's shallow learning and if you're not motivated, exercises might also not help much.

Code along in your pace if you prefer. I would have done this somehow differently. One of the best ways to transfer knowledge is to actually apply the learnings.

> Tell me and I forget, teach me and I may remember, involve me and I learn - Benjamin Franklin

- Start earlier

I guess this is a learning we all make after we've accomplished something outside our comfort zone. Seeing how "easy" it was in retrospect, makes us wondering why we did not start earlier. Most of my _fear_ when creating content (both text and videos) in the Internet was what will others think when they see it. I never actively showed them my project and let them natuarlly find out. In the end, I don't care at all what they think. As long as I'm having fun doing it and see benefit for a greater audience I'm set. If you would ask me now for advice when the right timing for creating your first article, first YouTube video or online course, the answer would be simple: "Right now".

- Spend less on display ads

Well, I did not spent that much on ads on Google, Facebook, Twitter and Facebook but I'd definetly do it differently. While 50% of the money spent was also required to learn how the different advertisment platform works, with the rest I was trying to make sales. I always had this desired picture in place where you have your online course funnel and if you feed with enough visitors, a small percentage will finally convert and you somewhat a perpetuum mobile. You make more money on your course sales than your CPA (Cost per Acquistion) is. While this is defiently achievable, I did not come close to it. What definitely did not work for me was sending cold leads to a $100+ product and expect them to convert. What did work however, is to get some initial leads and move them up the value ladder. There are more or less four types of potential course participants:

1. The potential course participant is not aware that they have a problem (aka. I don't write tests)
2. The potential course participant is aware that they have a problem (aka. I try to write tests but fail to get the setup correct and am constantly frustrated)
3. The potential course participant is aware of you as a content creator (aka. I know that Philip is creating some content about Java and Spring and have read one or two articles from him)
4. Being aware that you sell an online course that helps fixing this problem (aka. I know that Philip offers the Testing Spring Boot Applications Masterclass, that will help me write better tests -> Ka-Ching $$$)

- Read more on this topic and connect more to other content creators

You don't have to explore everything on your own. Most of the stuff has already been done by others. Ask them for adivce and help. Ask them what they'd done differently if they'd start from scratch again. Read other and join communities like Blogging For Devs. Get around like-minded people for both tips and motivation.

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

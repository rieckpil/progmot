---
title: "How I Made $35k Selling My First Online Course - A Retrospect"
date: 2021-10-22T10:09:00+02:00
slug: "/creating-and-selling-my-first-online-course"
author: "Philip"
summary: "A one-year retrospect after creating and selling my first online course: my strategy, the actual journey, mistakes, and recommendations."
description: "A one-year retrospect after creating and selling my first online course: my strategy, the actual journey, mistakes, and recommendations."
cover:
  image: "/img/featured-images/online-course-one-year-retrospect-midjourney.png"
  alt: "Selling My First Online Course One-Year Retrospect"
  caption: "Selling My First Online Course One-Year Retrospect"
  relative: false
keywords: []
draft: false
tags: []
ShowToc: true
trackingPixel: "e80f19774bbb4287ac0997f254da2828"
---

_**TL;DR:** This 6500 word long article is a one-year retrospect after launching my first paid online course. Learn about my initial strategy, the actual journey, the mistakes I've made, and my recommendations._

It's been a year since I launched my first paid online course: the [Testing Spring Boot Applications Masterclass](https://rieckpil.de/testing-spring-boot-applications-masterclass/). There's a lot of things I've learned along the way, and mistakes I've made.

This article gives you an inside view of this project. We'll cover the technical setup, how I've planned and recorded the video lessons, and my sales and marketing efforts.

A short note about my background: On [my main blog](https://rieckpil.de/), I create content about Java, Testing, Spring Boot, and AWS. In August 2020, I launched the Masterclass as my first paid online course. This online course is an in-depth resource on deploying Spring Boot applications with more confidence. The course showcases various recipes, tips & tricks, and best practices for testing real-world Spring Boot applications.

_**Disclaimer**: Figuring out which tools to use for such a project was quite an effort. Especially as I started from scratch. I spent various evenings screaming at my misbehaving checkout setup. I'll reference the hardware, tools, and software I'm actively using at multiple places in this article. The marked links (*) are affiliate links. I paid the price (mostly time) to figure out this lightweight course selling setup - so you don't have to._

Let's get started.

## The Initial Strategy

To better understand my journey, let's take a brief look at my content creation history.

Back in November 2017, I published my [first blog article](https://rieckpil.de/summary-of-the-container-conf-2017/). While the first few articles were somewhat random (both in the topic and timing), I soon established the habit of writing about something consistently. Since then, I've been writing articles for various topics, mainly about Java and its ecosystem.

Many of the blog posts result from my hands-on experience at work, or are tutorials I wish I had found on Google when I learned a new technology (especially Java EE).

At the end of 2019, I reached the milestone of 100 published articles on my site.

After writing `text/plain` for three years, I thought the next natural step would be creating video content.

I gave it a shot and uploaded my [first video on YouTube](https://www.youtube.com/watch?v=GM5ftYM_W90) in May 2019.

The audio quality was bad, and the video had black bars as I didn't record 16:9. However, that didn't matter, as I was happy to leave my comfort zone and have _something_ uploaded. I was sure that the quality of every upcoming video would improve anyway.

> Perfection is the enemy of progress

With these two content platforms (blog & YouTube) in place, I continued creating content for various topics. There wasn't a clear target audience I wanted to reach.

Whenever a topic worth talking about popped up, I sat down and wrote about it. I usually switched frameworks between the articles and hence wasn't targeting a specific set of Java developers.

In the last two years, I have naturally discovered my content niche. I started focusing more on one specific topic instead of serving all Java developers: Testing Java and specifically Spring Boot (a well-known framework) applications.

The benefit of this niche is that almost nobody talks about testing in their articles. They showcase shiny new features or tools, but nearly never tackle the testing part.

That's quite frustrating if you want to apply their ideas to your project at work. You copy the relevant sections, make sure it compiles, and then hit a roadblock.

You know ahead that your colleagues will ask you as soon as you want to integrate your code changes: "Where are the (damn) tests?".

After creating some articles for this niche, I discovered that there was almost no online courses that comprehensively teach this topic, whilst using real-world examples.

Everyone can test the `add` method of a `MyCalculator` class. But how do you write an end-to-end test for a modern application involving an OIDC login, database access, and fetching data from REST API in the background?

My plan was to develop a real-world course application, enhance it with an excellent test suite, and talk about it. And with real-world, I mean a sophisticated application that connects to various infrastructure components. This is where testing becomes tricky.

I strongly believe that testing becomes joyful as soon as you know of the different testing tools & libraries, and recipes at hand.

It's the HOW that's important here.

Packed with this mission, I was highly motivated to get this project going. As I have done nothing similar before, except some sporadic YouTube videos, recording everything up front would be a hell of work.

That's why I decided to use an iterative approach and incrementally create this course while getting feedback early on. #agileDoneRight

## Creating the Course Content

As a first step, I developed the real-world course application.

The course application is all about creating and managing book reviews.

For the application's tech stack, I picked React with TypeScript and a Spring Boot Java backend. That should mirror most of today's architectures (SPA connecting to a backend) out there.

To make the setup more advanced, I added Keycloak (an open source identity provider), PostgreSQL to store data, a remote REST API, and an AWS service for messaging to the mix:

![Technical Architecture of the Masterclass](/img/tbsam-technical-architecture.png#center "Technical Architecture of the Masterclass")

In parallel, I sketched out the different course modules (module -> chapter -> lesson). Throughout the course, I wanted to tackle unit, integration, and end-to-end testing. This gave me the natural course structure of starting at the bottom of the testing pyramid with unit testing, and then working upwards until we finally write end-to-end tests in the last module.

Once the application was ready, I had a rough idea of what I wanted to showcase and talk about. I ensured there were enough non-trivial code parts to demonstrate various testing techniques: secured endpoints, message listeners, database access with native queries, plain business logic to verify, etc.

While I could (and maybe should) have written the tests for the application alongside the development, I first wanted to have a working application to see the bigger picture.

As the goal of the online course was all about testing applications, I did not record the creation of the sample application. In various lessons, I explained the relevant code parts and gave an architectural overview at the beginning of the course. The overall application was sophisticated in the setup and yet simple enough to grasp within minutes.

Here's a short excerpt of the course application's primary use case: Creating book reviews:

![Recorded E2E test of the main user journey](/img/main-user-journey-e2e-test-recording.gif#center "Recorded E2E test of the main user journey")

(The GIF above is an automatically recorded outcome of an end-to-end test)

With my iterative course creation strategy in mind, I started with the first milestone and wanted to release the first two modules (roughly 15 course lessons). These two modules were all about getting used to the course application and an introduction to unit testing.

This initial goal got me started to outline the first lessons in greater detail. I noted down the best practices, tips, and pitfalls I wanted to show. I did not set hard boundaries for the lessons ahead and wanted to find a natural position to cut the recorded video afterward.

Next, I opened my IDE and developed all the tests I wanted to write and talk about.

Once finished, I committed the changes to my private GitHub repository and removed the code I had just developed to a bare skeleton.

This "dry run" without recording helped me during the actual recording session. I was using two screens, and on one screen, I recorded my IDE and developed the tests step-by-step. On the second screen, I opened the target outcome by cloning the same project twice.

I could frequently look at the second screen to not get lost while coding.

This initial batch of work (roughly 15 lessons, each 5-15 min long) kept me busy for three weeks. I usually used the morning hours to record 60 - 90 minutes of content. I brainstormed the following lessons in the afternoon and edited the videos once the entire batch was recorded.

After finishing an iteration of usually 1 - 2 modules, I started with the next one. I followed this strategy until I had all eight course modules with 127 videos lessons recorded.

## The Technical Recording Setup

I've developed the course application and recorded everything on an Ubuntu 20.04 desktop PC and used the following tools:

Recording & Editing:

- [Kazam](https://wiki.ubuntuusers.de/Kazam/) for audio and screen recording
- [Audacity](https://www.audacity.de/) for sound editing
- [kdenlive](https://kdenlive.org/de/) for video editing and rendering
- Microphone: Auna Mic

Application development:

- a private repository on GitHub
- plain `.md` files inside the repository to structure the modules and lessons
- IntelliJ IDEA as the IDE:
  - I used IntelliJ's Presenter View to record the videos for a bigger font size and less clutter on the screen
  - In addition, I used the Presentation Assistant plugin to automatically show the shortcuts I'm using (a lot of students will ask):

![Presentation Assistant Plugin Example](/img/presentation-assistant-idea-plugin-example.png "Presentation Assistant Plugin Example")

As I was only recording my screen and audio, there was no need for a green screen, a high-resolution camera, or a lighting setup.

Had I set up additional equipment for recording more than just my screen, this would have postponed the time I'd have a _good enough_ recording setup.

The benefit of recording only audio and the screen is that you can focus on writing code. You don't have to coordinate with the camera and can stare at your screen or microphone. If you misspelled a sentence, you can reiterate with ease.

For a first welcome video where you greet your new course participants, it might make sense to show your face to establish a stronger _connection_ with the audience. For the rest of a technical course, IMHO, that's optional.

Sometimes the face of the course instructor also blocks essential parts on the screen. As I'm only typing on my keyboard, there isn't much gesture anyway.

It's better to get started with a setup you feel comfortable with than procrastinating or getting pixel-perfect lessons that nobody will watch because the topic is not convincing.

Once I had the entire recordings for a batch ready, I started the editing process.

As a first step, I extracted the audio from the recording and opened it in Audacity. There I made some adjustments to the audio, like removing background noise. I replaced the original audio with the edited soundtrack from Audacity within kdenlive.

Next, I started the actual video editing.

I did not add any fancy animation or transition to the videos and only focused on removing the misspellings and separating videos. A 90-minute recording block usually resulted in 50 minutes of content split up into 4-5 separate video lessons.

## The Technical Hosting Setup

While I've worked through several courses on Udemy and similar platforms myself, I soon encountered that these platforms are not the best fit for me. While they do some marketing for your course and have a lot of search traffic, their payment structure is not what I was looking for.

I wanted a lean technical setup that gives me full control over the course and audience.

As my blog is running on WordPress, and I'm heavily using the [Thrive Suite*](https://rieckpil.de/a/thrive-themes), I investigated their online course plugin: Thrive Apprentice.

With Thrive Apprentice, I could leverage the WordPress user management to have a login area and control access to my course. The visitors also stay on my side, and I have full control over the content.

For [Thrive Apprentice*](https://rieckpil.de/a/thrive-themes), you need both an eCommerce provider, and a video hosting solution.

For the eCommerce provider, I chose SendOwl, as their features and pricing (my current plan is $26/month) are reasonable.

Once I'd signed up for my SendOwl account, I connected my Stripe and PayPal accounts to have the most common payment options.

Thrive Apprentice supports various video hosting platforms. I went for Vimeo and picked their paid plan for $6/month.

Compared to YouTube, you can add more fine-grained security settings for your videos with Vimeo. This makes unintended downloads and sharing more complicated. The integration with Thrive Apprentice works by simply copying the video link.

Using these tools, the final workflow to access the Masterclass is as follows:

1. The potential course participant visits the [landing page](https://rieckpil.de/testing-spring-boot-applications-masterclass/)
2. Once they click on "Buy Now", they're redirected to a pre-checkout page (on my blog) and have to register a new course account
3. They're redirected to a SendOwl checkout page and enter their payment information
4. SendOwl redirects the user to a "Thank You" page on my blog with further information on how to get started
5. In the background (and if the user gave consent), they're added to my mailing list (Mailchimp), including order information
6. Once the order is completed, SendOwl sends a webhook to my WordPress instance and Thrive Apprentice grants access to the purchased course
7. The user can now work with the course and gets a "Welcome" email delivered to their inbox

It took me some test purchases until I had the proper configuration for this setup, but since then, it's working fine.

SendOwl even offers a deep integration with Mailchimp to recover abandoned carts.

The integration to my main mailing list also helps to segment my audience. I can see if a subscriber has enrolled for the course or got stuck in the checkout.

This helps to send marketing campaigns more efficiently to the right subscribers by using tags:

![Mailchimp SendOwl Integration Example](/img/mailchimp-order-information-from-sendowl.png#center "Mailchimp SendOwl Integration Example")

## Selling the Content

Having the course idea and some early lessons uploaded to Vimeo, now it's time to sell the content, isn't it?

From a timeline perspective, I first created a minimal version of the landing page, including basic sales copy.

This helped me gather my thoughts and think about the benefits and the USP (unique selling proposition) of the course ahead. Figuring out a minimal sales pitch also gave clarity on what to focus on when I planned the course lessons.

The landing page at this time was the bare minimum (no checkout) and a static site on my blog advertising my current idea. I put a newsletter signup form on this early version of the landing page to capture potential customers.

This pre-landing page also acted as a basic market research opportunity. I used it to validate that the course idea arouses interest. Just because I thought the course topic was valuable, that didn't imply that someone out there was willing to pay for it.

For the [landing page](https://rieckpil.de/testing-spring-boot-applications-masterclass/) I used Thrive Architect, a visual drag-and-drop page editor that is part of the [Thrive Suite*](https://rieckpil.de/a/thrive-themes). I picked one of their ready-to-use landing page templates to get started quickly.

While I haven't any screenshots of this early version anymore, here's an overview of the final page:

![Landing Page of the Masterclass](/img/tsbam-landing-page-overview.gif#center "Landing Page of the Masterclass")

As this was my first landing page for a paid product, I tried my best to write engaging sales copy. I added social proof via testimonials about myself from well-known content creators in the Java space as I didn't have any course testimonials yet.

As soon as the first feedback from course participants came in, I asked for their permission and also placed them as testimonials on the page.

Most developers don't know you. You're a stranger on the Internet. Why should anyone take your course?

I shared the pre-landing page and my course idea on various channels (Twitter, LinkedIn, mailing list, etc.). After collecting potential leads for almost two weeks, I got 50 prospective leads.

This was enough evidence for me to get started.

To come up with a final price, I used other courses in my niche as an orientation and wanted to stand out with a premium course on this topic. Nothing in the Udemy price level. The first target price that came to my mind and seemed reasonable was $159 for the entire course.

Once the first video lessons were uploaded to Vimeo, I modified the landing page and activated the checkout process.

Paying the full price for the course up front while getting access to a subset of the lessons wasn't a viable strategy. I came up with the idea of early-bird discounts similar to an early access program.

With every iteration of the course, I slightly increased the price. Those that joined early got access to the entire course for almost the price of an eBook. But they had to wait until all lessons were available.

I added scarcity effects with a countdown that informs how long the current early-bird discount is available, to drive more sales.

In the end, I had nine of these early-bird batches:

- 80% discount from 8th of August - 16th of August
- 70% discount until the 23rd of August
- 65% discount until the 30th of August
- 60% discount until the 13th of September
- 55% discount until the 20th of September
- 50% discount until the 27th of September
- 40% discount until the 4th of October
- 37.5% discount until the 11th of October
- 30% discount until the 25th of October

At each stage, new course users could join for a reduced price and get all upcoming course lessons for free. This early-bird program also reduced the feedback cycle as I got important feedback early on and could improve the upcoming lessons.

{{< newsletter-advertisement >}}

## Going Live With the First Lessons

Selling something to an audience of zero people is hard.

When I launched the first landing page, I already had an existing audience thanks to my mailing list, blog, Twitter account, and YouTube channel.

Those people, however, all had different interests as my existing content was a diverse mix of topics. Not all of them were my perfect target audience: Java developers working with Spring Boot that want to improve their testing skills to deploy their application with more confidence.

Nevertheless, some early adopters were among my existing audience, which gave me an additional boost and confirmation that there's demand for such a course.

After the small _market research_ phase, where I collected email addresses of potential leads on my pre-landing page, I started to advertise the course actively. As I was (and still am) highly convinced that my online course can improve the technical skills of many developers, I used all channels to raise attention about each early-bird phase.

In the beginning, my newsletter updates and Tweets might have seemed a little salesy as I was highly motivated to get the word out. I screwed some visitors and newsletter subscribers as they weren't expecting this much advertisement.

That's the price you pay for learning how to balance sales talk and content delivery.

The unsubscribe rate of my mailing list also started to increase. At first, it was hard to see subscribers leaving the mailing list whenever I wrote about the current progress or informed about the remaining days for the current early-bird batch.

In the end, as I can't please everyone and wanted to shift my content niche, it was fine that some subscribers _disappeared naturally_.

Since then, I started to focus on creating new content that is somehow related to my niche. This helped me get potential leads naturally as they subscribed with the intent to learn more about testing.

On the 8th of August 2020, the time had come to go live with the first video lessons and an 80% discount.

I still remember the exact feeling when I hit the release button for this first early-bird batch. I was both nervous and super excited. While I tested the entire checkout process multiple times, I was still worried that something would go wrong.

As I didn't want to nervously stare at my inbox for the first complaints or orders (who knows what will happen), I left my room and had dinner with my family to distract myself.

I almost forgot about the launch and checked the Stripe (payment processor for credit cards) dashboard two hours later...

WTF?

There are already five sales - YEEEEEES!

Damn, what a feeling.

Someone from somewhere around the globe just bought my course at this early stage. And they even paid for it!

At the end of the release day, there were nine paying customers:

![Incoming Sales on the Course Launch Day](/img/tsbam-first-day-course-launch-sales.png#center "Incoming Sales on the Course Launch Day")

I never thought that many people would enroll in the course at this stage. I was expecting 20 customers in the first month.

From release day onwards, I used almost every day to work on the remaining course lessons. It took me two and a half months to finish the course.

## A Note on Effort

On the 25th of October 2020, when I uploaded the last lessons and closed the final early-bird batch, the course had 127 video lessons.

I never had a target for the total course length in mind. I recorded as many videos as required to explain the various unit, integration, and end-to-end testing concepts.

In total, the course users will watch 10 hours of high-quality content on testing Spring Boot applications. Most of the video lessons are five to ten minutes long.

If I had started this project with the goal of 10 hours in mind, and wanted to record everything at once, that would have been almost impossible. I'd had to lock myself in my room for two months straight and then come out with a big bang release. The iterative approach helped me keep going.

It's hard to tell how much effort went into this entire adventure as I didn't stop and record the time.

As a ballpark figure, let's say that for 30-minutes of video content, I've recorded 45 minutes. Editing the raw content took me another 45 minutes. This makes it approximately 90 minutes for a final  content block of 30-minutes.

However, this number does not include preparation work, coding efforts upfront, ideation, and marketing efforts afterward.

If I had to guess the total hours, it would be **between 100 and 120 hours to create this course from scratch**.

The additional time I had due to working remotely made this workload possible, next to a full-time job as a developer. I didn't have to spend 2 hours every day for the commute and could focus on the course first thing in the morning. In addition, I spent some Saturdays and Sundays to make this course happen.

Now it's time to start with the one-year retrospect.

## One-Year Retrospect - What Went Well

Looking back at the first year of this adventure, let's talk about what I would recommend and where I got lucky.

### Releasing Early and Often

The iterative approach with small increments helped to experiment and keep being motivated.

Getting the first version of your course out as soon as possible gives you confirmation and feedback early on.

This first version need not be perfect, but will let you test your setup end-to-end. This works way better than preparing a "big bang" release and then figuring out that something with the payment setup is not working at the last minute.

### Working With a Good Enough Tech Setup

You must be confident and have a simple and reproducible recording setup. You should be able to hit the record button in a matter of minutes with little preparation work.

If you have to set up an entire conference studio for your first online course, chances are high you're procrastinating due to the effort.

I can highly recommend getting some first touchpoints with video recording and editing on YouTube. YouTube is a great playground. There will be no refunds and (usually) only helpful comments to improve.

This applies to both the technical setup for recording and selling your course. There are many decisions to make, and I'd recommend that you start with the simplest solution that fits your current needs.

You can buy a green screen later.

### Single Digit Refund Rates

Money-back guarantees are a must-have for digital content. I'm offering a 30 days back no-questions-asked policy. I've had [some bad experience with the refund policy of another content creator](https://rieckpil.de/review-baeldungs-rest-with-spring-masterclass/) in the past and didn't want to be alike.

I still remember the first month after the launch of the first version, I was so nervous about the first 30-day period and thought many customers would ask for a refund.

This did not happen.

After one year, I have a refund rate of 0.75%. Most of those refunds were due to different expectations.

### Affiliate Marketing is King

There are tons of bloggers out there that might want some extra money each month to pay their hosting/tooling bills. I reached out soon to various other bloggers in the Java ecosystem and asked them to become an [affiliate](https://rieckpil.de/affiliate-program/).

If the affiliate partner embeds their link into an article that talks about the topic you teach, the conversion rates can be excellent.

Those affiliate links will also add social proof, and more developers will get to know you.

SendOwl comes with an easy-to-use affiliate setup. One of my affiliate partners is making $200+ almost every month.

### Attracting New Leads With Compelling Free Content

As soon as your existing audience knows about your product, you need to attract new leads.

One of the best ways to do this is by creating high-quality content around the course topic.

Once I found my niche, I doubled down on the testing topic and primarily created articles and videos for this domain.

Your blog visitors will soon associate your blog with your niche. Even if they don't convert on their first visit (which they rarely do), they know that they can come back to find a solution for problem X.

And the next time they're looking for deep dive content on your topic, they know where to look first for an online course.

### Starting With Market Research

I got lucky that there was a demand for this course. It might have also flopped.

That's fine, as long as you're finding this out early in the process. Creating the landing page first can help to identify if there's demand. You can also use a poll and send it to your existing audience.

If you don't have an audience (yet), try to engage with your target audience on Twitter, Reddit, YouTube, etc.

### Living Off the Earnings

I guess most of you are eagerly waiting for the raw numbers :moneybag:

I've made $35.369,44 in revenue after one year:

![Sales report overview after one year](/img/tsbam-earnings-after-one-year.png#center)

The margin is high as my only expenses are hosting fees, marketing costs, and affiliate commissions.

If I slightly reduced my monthly costs for living, I could live off that money.

That's a huge relief!

In the first months, you might not get the traction as expected. Don't compare the invested time with your hourly rate or salary.

An online course is an asset that'll (hopefully) make money while you sleep.

### Steep Learning Curve

There's a lot to learn, not only about the topic you teach.

I learned so much about marketing, writing sales copy, tracking, conversion rate optimization, A/B testing, checkout processes, online marketing, how to work on customer complaints etc.

This additional knowledge also helps me improve as a software developer, as I now see things from a different angle.

I'm no longer just a techie and code monkey, I understand what it takes (at least the basics) to run an online business as I'm selling products on my own.

### Starting Small

This steep learning curve is a double-edged sword.

There are so many topics to handle when selling digital products on the Internet:

- your participants have a smooth and working checkout process
- the access to the course content is working
- your landing page has a reasonable page speed
- work on complaints
- create invoices
- do accounting work
- etc.

You can easily get lost in various parts of creating, advertising, and selling your content.

I usually stop when I have a good enough solution and come back later with a fresh mind and more hands-on experience.

There's so much to do. Start small, and iterate.

Don't get frustrated if something's not working immediately.

Can't find the root cause for your not-so-optimal page speed? Give your best and otherwise sleep a night over it.

It has to be joy, not work :wink:

## One-Year Retrospect - What to Improve

As the goal of every retrospective is to improve, let's talk about my mistakes and the things I would do differently now.

### Use a Merchant of Record

... and thank me later.

If you're selling to EU customers, pick a merchant of record to sell your digital products. Take a few minutes to [read about VAT handling](https://www.quaderno.io/resources/eu-vat-guide) of digital goods (especially for EU customers), and you'll thank me later. I didn't read enough about this topic and started without such a middleman.

I'm handling VAT for myself. The effort is manageable.

When working with SendOwl, I can highly recommend Quaderno to stay tax compliant, create nice-looking invoices and exports for your tax advisor.

If I would start over again, I'd pick a provider that handles all tax implications. Possible providers are CopeCart or Digistore24.

That's more time to focus on improving the course.

### Adjust Your Expectations for the Participation Rate

I first thought my content was not good enough when I looked at the total views of the last module.

I expected everyone to finish the course right after they purchased it, or at least in time (whatever this means). This is because this is what I usually do when I enrol on a new course.

It seems that this is not the case for everyone.

There are still course participants that did not even start with lesson one.

That's okay - they might be busy and will start when they have time.

### Use IDEA Live Templates to Avoid Blockers While Recording

During various recording sessions, I got lost.

I sometimes forgot how to implement the test, what package to import or what I wanted to show.

IntelliJ IDEA, the Java IDE I'm using, provides a feature to help: [live templates](https://www.jetbrains.com/help/idea/using-live-templates.html).

With these templates, you prepare code skeletons and insert them with auto-completion.

However, when using these templates, it's important to find the right balance of magically inserting the code and typing everything from scratch.

You can't just paste 15 lines of code and assume the course participant gets what you're doing.

### Support Purchase Power Parity from Day One

We live in a world with different purchasing power and wages.

This $159 online course is affordable for someone working for working in silicon valley. That's not the case for all other countries around the globe.

A developer earning only a quarter of the US median wages thinks twice before enrolling in this course. For some developers, the course for its base price is not affordable at all.

Many companies adjust the prices for their products and services to the purchasing power of each country. This way, the relative costs for a product (e.g., 5% of the median monthly salary) should be the same for everyone.

In the early days of the course, several potential customers asked for coupon codes because the price was too high for them. Back then, my main excuse for not integrating automatic price adjustments was that my eCommerce provider did not support something out-of-the-box.

After some investigation, I came across a [small library from Robin Wieruch](https://github.com/rwieruch/purchasing-power-parity) that helped me integrate purchase power parity (PPP) with some additional coding effort on my end.

As I want to reach many people with the content I create, supporting PPP is a no-brainer for me in retrospect. Since the integration of PPP, the total orders have also increased.

I've seen creators that are afraid that someone will abuse this mechanism.

Creating a VPN tunnel to another country is a matter of seconds. Someone might trick this system and get the content for only a subset of the target price for their country. Nevertheless, I'm still able to see the origin of the payment and can identify _frauds_.

This has never happened so far, and even if it happens, I'm convinced that Karma will do its job.

### Embed More Hands-On Exercises and Quizzes

I've worked through several online courses and enjoy learning new techniques and tools this way. I generally prefer to code along with the course instructor and immediately try out things in my IDE.

Whenever there were exercises or assignments at the end of each lesson, I usually ignored them as they were sometimes too simple or somehow already covered by me coding along.

This personal preference was the main reason not to include any specific coding task after each lesson. I thought that if customers are eager to learn this topic, they'll try to apply the knowledge as soon as possible by default.

Otherwise, it's shallow learning, and if you're not motivated, exercises might also not help that much.

Not everyone shares this viewpoint, and some course participants have already asked for a more guided approach. Looking back, I would have thought more about exercises, quizzes, and assignments.

For learning new things, the best way to put it is in the words of Benjamin Franklin:

> Tell me and I forget, teach me and I may remember, involve me and I learn - Benjamin Franklin

As I did not create a physical product that is already shipped to customers, I can still add these exercises afterward.

### Start Earlier

I guess everybody has this learning curve after accomplishing something outside of their comfort zone.

Seeing how _easy_ it was in retrospect makes me wonder why I did not start earlier. Most of my _fear_ when creating content on the Internet was what others think when they see it.

When I created my blog and uploaded my first video on YouTube, I never actively showed anyone my project, and let them naturally find out. I don't care at all what they think, except if it's constructive feedback.

As long as I'm having fun doing it, and see the benefit for a greater audience, I'm happy.

There's only one good time for creating your first article, YouTube video, or online course: right now.

### Spend Less on Display Ads or Spent It Better

Seeing the sales coming in, I created ads on various platforms like Google Search, Twitter, Facebook, and LinkedIn.

I thought that if I just had enough firepower (a.k.a. money) for ads, I'd create a money machine.

Living the dream where the CPA (cost per acquisition) is less than the generated revenue: a money perpetuum mobile.

That didn't work - at least not for cold leads and a $150+ product.

The advertising domain was new, and the (sometimes complex) user interfaces to create new campaigns confused me. I had to burn some cash until I had the campaign setup right and targeted the right audience.

My first ads on Facebook, Twitter, and LinkedIn, were trying to create sales for the Masterclass. While these ads brought visitors to my site, nobody immediately converted. This is understandable for cold leads and a $150+ product.

After spending over $2k+ for various platforms, I'm no longer advertising the Masterclass directly. This money might seem huge, but almost 50% was spent learning how display ads work.

I'm still running display ads, but follow a different approach. I use the ads to make my target audience aware of my content and what my site is all about. If they like the content, they might sooner or later convert into a course participant for my Masterclass.

While this is a slower sales process, it's more sustainable, and right now, I generate leads for one of my free testing courses for about $0.50.

From the Traffic Secrets book I learned that there are more or less four types of leads:

1. The potential course participant is not aware that they have a problem: a.k.a. - I don't write tests
2. The potential course participant is aware that they have a problem: a.k.a. - I try to write tests but fail to get the setup correct, and I'm constantly frustrated
3. The potential course participant is aware of you as a content creator: a.k.a. - I know that Philip is creating some content about Java and Spring and have read one or two articles from him
4. Being aware that you sell an online course that helps to fix this problem: a.k.a. - I know that Philip offers the Testing Spring Boot Applications Masterclass, which will help me write better tests -> Ka-Ching $$$

### Connect With More Content Creators

You don't have to explore everything on your own. You don't have to make all the mistakes on your own.

Most of the stuff has already been solved by other content creators - ask them actively for advice and help. Ask them what they'd do differently if they'd start from scratch again. Ask them which tools they use and how their setup works.

I'm sure most creators are happy to share insights and help you get started.

Read retrospective articles like this and join communities like [Blogging For Devs](https://bloggingfordevs.com/). Surround yourself with like-minded people for both support and motivation.

### Don't Get Drained Into a Sales Dopamine Cycle

Seeing passive money coming in almost daily, I soon started to check my mails after work eagerly (I never check my emails first thing in the morning). Subconsciously, I got drained into frequently checking my sales due to a small dopamine rush from each new order. It's similar to the urge to check the Twitter feed, HackerNews, or Reddit.

Each new customer gave me some gratification and relief until the point when there were no new customers for several days. I felt unhappy.

Initially, I tried to run temporary discount campaigns to see at least some sales coming in. That wasn't worth the effort as it screwed existing customers just for the purpose that I see this lousy sales graph go up.

That's not worth it.

If your product is good and you have an established sales funnel, it's only a matter of time until new course users join.

These sales ambitions might drain your creative resources, and you start focusing on the wrong ends: a.k.a. - getting more sales vs. making a great product.

## What's Next?

In our fast-paced development world (fortunately, the Java ecosystem is not as fast-paced as JavaScript), content ages and gets outdated over the years. New libraries, tools, and techniques pop up that make existing course lessons outdated.

That's why I'm constantly trying to be up-to-date. As the testing topic is also the main focus area of my blog, that's no problem. My freelance projects for clients also ensure I get enough hands-on experience.

Whenever there's something new or worth mentioning, I'll add a new lesson to the course. If there's something outdated, or I would do something different, I'll replace a video.

Compared to an eBook, keeping an online course up-to-date is more effort. There's no search and replace functionality for already recorded videos. You have to find the correct spot and record a new video, or cut the outdated scene. But fortunately, in the area I'm creating content for, there's maturity and stable APIs and libraries.

Some course participants asked for a `plain/text` version of the online course to have a quick lookup reference for recipes and techniques. This is why I'm currently creating an eBook based on the online course.

It's also a great way to attract a wider audience, as not everybody enjoys learning from videos and prefers to read a book on the beach.

The next online course is also waiting to be created. On top of the [Stratospheric eBook](https://stratospheric.dev/) (From Zero to Production with Spring Boot and AWS), which I've written with [Tom Hombergs](https://reflectoring.io/) and [Björn Wilmsmann](https://bjoernkw.com/), we're creating an online course. Equipped with my insights from this course launch, I'm looking forward to this project.

Now it's your turn - go for it and let me know how it worked out!

PS: If you plan to mirror this setup and have further questions, feel free to [reach out](https://twitter.com/rieckpil).

Happy creating,\
Philip

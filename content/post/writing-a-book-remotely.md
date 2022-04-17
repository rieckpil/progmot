---
title: "Writing and Self-Publishing a Non-fiction Book With Strangers"
date: 2022-04-19T10:00:00+02:00
slug: "/writing-and-self-publishing-a-non-fiction-book-with-strangers"
author: "Philip"
summary: "A one-year retrospect after co-authoring and self-publishing a technical ebook about Spring Boot and AWS with co-authors I met on Twitter."
description: "A one-year retrospect after co-authoring and self-publishing a technical ebook about Spring Boot and AWS with co-authors I met on Twitter."
cover:
  image: "/img/featured-images/writing-a-book-remotely.png"
  alt: "Writing and Self-Publishing a Non-fiction Book With Strangers"
  caption: "Writing and Self-Publishing a Non-fiction Book With Strangers"
  relative: false
keywords: []
draft: false
tags: []
ShowToc: true
---

This article describes a one-year journey of writing [Stratospheric - From Zero to Production with Spring Boot and AWS](https://stratospheric.dev/) as a co-author with two other co-authors that I met on Twitter. We've never met in person before and managed to successfully write a 450+ pages in-depth guide on developing and deploying Java Spring Boot applications on AWS (Amazon Web Services).

In short, this article covers:
- How we self-published this ebook while writing the manuscript in Markdown
- How we promoted and sold the ebook
- How we organized ourselves to write the ebook asynchronously while having an 8-hour time lag
- General tips, recommendations, and lessons learned for co-authoring a technical ebook

The whole project was (and still is) a lot of fun. I learned a ton about AWS and got the chance to connect and work with knowledgeable and nice people.

The three co-authors are: [Tom](https://twitter.com/TomHombergs/) (🇩🇪 living in 🇦🇺), [Björn](https://twitter.com/bwilmsmann/) (🇩🇪), [Philip](https://twitter.com/rieckpil) (🇩🇪 - that's me).

Let's get started 🚀

## How We Found Each Other 👥

> Luck is what happens when preparation meets opportunity.

While scrolling through my Twitter feed, I saw a fellow technical blogger reaching out to other bloggers to exchange knowledge and ideas.

{{< tweet user="TomHombergs" id="1278635778722000902" >}}

{{ < tweet-single 1278635778722000902>}}

We next met with the intention of sharing our experience as tech bloggers. During the second or third meeting of this kind, Tom asked for fellow bloggers who'd interested in taking a closer look at AWS and Spring Boot and who may want to write about it.

Björn and I, participating in this meeting, raised our hands. We've never met each other before and only partially knew each other from reading each other's blogs and Tweets.

We organized a separate meeting to discuss more details and to get to know each other.

## Our Goals For This Project ⭐️

Before we started to work on this project, we met several times to get to know each other and align our goals and expectations. While all three of us were working full-time for clients/an employer, we set the common understanding that this would be a fun side project.

We all have had some experience with AWS but wanted to learn more about this particular cloud provider in depth. When developing features for clients or customers, we usually never had the time to explore the variety of AWS services available.

One primary goal of this remote writing project was to get better at developing Java applications on AWS. As Spring Boot was our default technology stack back then, the choice came naturally to write about this niche.

While there are many books on AWS in general, none talks about the full cycle of bringing a Java Spring Boot application to production on AWS.

Showcasing shiny features and machine learning capabilities of AWS is great, but many teams still struggle to design an automated CI/CD pipeline to push their changes automatically to AWS.

Furthermore, the development journey doesn't stop when merging the code changes and moving a Jira ticket to the done column. Now, the fun part begins as our code runs in production.

If we are in the lucky position to maintain and operate our own services (DevOps done right), we will have to deal with the following questions, which will arise sooner or later:

- How do I know my service is healthy and operating as expected?
- What's the current average response time for my most important API endpoint?
- What happened with the application yesterday night? Our support team got a user complaint.
- Where can I find and filter the logs from last Sunday?
- etc.

In short, this brought us to the following high-level goals for our readers that also influenced our manuscript:

1. Learn about AWS and IaC (Infrastructure as Code) with the AWS CDK.
2. Develop a Spring Boot application with meaningful features (e.g., email notifications or OAuth2 login) while integrating as many AWS services as possible.
3. Becoming familiar with best practices for running Spring Boot applications in production on AWS: monitoring, alerting, observability, etc.

Apart from these project goals, I had the following personal goals:

1. Learn more about AWS.
2. Improve writing skills and tick off 'writing a book' from our bucket list.
3. Create awareness of myself to attract potential clients as a freelancer.

Packed with these ideas, we then got started with the project.

## How We Got Started 🛫

We then started to meet constantly every two weeks via Zoom and created a Slack workspace for communication and coordination. We organized ourselves in a Scrum-like setup and planned our two-week _sprints_ with a Trello board. These bi-weekly Zoom calls were a mix of a daily review and a planning session.

There wasn't any story point or product owner, we were all intrinsically motivated to get stuff done and used
positive peer pressure, as everyone was reporting what they achieved in the last two weeks.

As a first step, we wanted to develop a small proof of concept application to explore which areas we could write about. We wanted our readers to complete the journey from knowing only a bit about AWS to having an automated CI/CD pipeline that deploys their application to production.

We picked what we felt most comfortable with for the tech stack: Java and Spring Boot with Spring Cloud AWS.

Besides exploring AWS services on the go, we all had stories and best practices for various AWS services to share that the other co-authors could learn from.

Once we had a working sample application running on AWS and we were confident that the topic we were about to write added value, we started writing the book. We first sketched out a table of contents and started working on the different chapters in parallel.

We created a new AWS account for this project, and added three IAM users for us. Next, we created a GitHub organization that acted as an umbrella container for all related code repositories for this ebook project.

We more or less split this PoC time into two areas: automating the infrastructure setup with CloudFormation and developing a sample application. Back then, we started with `.yaml` CloudFormation templates but moved quickly to the promising AWS CDK project.

As soon as we had a container cluster (ECS) with an automated CI/CD pipeline and the sample application with some basic features ready, such as a login with AWS Cognito and storing data within RDS, we started to plan the next steps.

This pilot phase took about two to three months.

Next, we had to decide how we would write this book. The main question we had to answer was: Should we talk to a publisher and pitch our idea or self-publish the whole thing?

As this project was a side-project for all three of us and not what we do full time, we all agreed that working with a formal publisher was not an option for us: Working towards given deadlines and having to deliver a final piece on a fixed date was something we clearly wanted to avoid.

Furthermore, Tom already self-published his first book and then got a technical publisher on board to offer a print version and more distribution channels. Based on his experience and the common understanding, that this project may also fail, we went for the self-publishing approach.

For self-publishing books in the tech space, [Leanpub](https://leanpub.com/) seemed to be the de-facto default choice.

Leanpub is highly appealing to self-publishing tech authors as they offer the following:

- writing the manuscript in Markdown or bringing your own PDF
- automatic formatting/layout for Markdown manuscripts
- automatic file generation for other ebook formats like Mobi and ePub
- integration with GitHub/Dropbox for the manuscript
- fair pricing with 80% royalties for the authors
- payout via PayPal and support for multiple authors
- no payment/tax implications for the author: Leanpub acts as the merchant of record and takes ownership for the payment and tax handling (something I should have also favored for [my first online course](https://progmot.com/post/creating-and-selling-my-first-online-course/))

Leanpub is also built around the "Publish Early, Publish Often" concept. They favor the approach of giving access to a book early while it's still in development and continuously adding new chapters to it.

Each [Leanpub ebook landing page](https://leanpub.com/stratospheric) provides information about the completeness and when the last changes were published:

![Stratospheric Completeness Bar](/img/stratospheric-ebook/leanpub-completness-bar-stratospheric-example.png#center "Stratospheric Completeness Bar")

Leanpub even allows creating preview versions of the ebook, a feature we heavily used to see a rendered version of our recent changes. This helped us quite a lot when preparing a new ebook version.

We went for Leanpub because it's tech-friendly, easy-to-setup and offers fair royalties that the platform can automatically split between co-authors.

Having signed up for Leanpub, it was now time to finalize the technical setup to then get our hands dirty and start writing.

Working daily with GitHub, we chose a private GitHub repository for backing our manuscript markdown files. This allowed for a more seamless flow compared to uploading the files to a shared DropBox folder. We get versioning, automations with GitHub Actions, collaboration tools, and a great feedback mechanism via pull requests with GitHub.

We used the following branching strategy for the ebook:

- `main`: generate ebook releases on Leanpub
- `preview`: generate previews on Leanpub
- `personal-feature-branch`: every co-author works in isolation on their next chapter

Every co-author would work on their own branch and push their chapters to their dedicated branch. Once completed, we created a pull request to merge into the `preview` branch. This triggered our review process, where all other co-authors reviewed the new section one after the other.

What's great about this review process is that we could leverage the review features of GitHub. This allowed the reviewer to directly make suggestions like fixing a typo or structuring the sentence. These suggestions could be then added automatically by the review owner:

![Providing Feedback via GitHub Pull Requests](/img/stratospheric-ebook/github-pull-request-suggestion-example.png#center "Providing Feedback via GitHub Pull Requests")

This way of working felt way more convenient than using a PDF reader, making comments and annotations to the file, and then sending it over to the owner of the changes.

After the review had been completed by both co-authors (six-eyes principle), we integrated the change into the `preview` branch to collect multiple chapters for the next release. Once every two months or so, we created the next work-in-progress release by merging the changes to the `main` branch.

All that's left to do then is to click the release button inside Leanpub to build a new digital version of our ebook. Theoretically, we could even automate this and publish a new release for the `main` branch on each commit.

## Getting the First Readers aka. Early Feedback 📖

Given the fact that we had figured out how to sell the ebook and how to write it, we now had to start, well, actually writing the ebook.

We found how to split the work and who would write what based on our own interests naturally. While Björn and I were more focused on implementing features for the sample application and connecting various AWS services, Tom was more into the CI/CD and infrastructure setup.

While we had a rough idea and an early draft for our planned table of contents, we adjusted our plans along the way.

Working on a new chapter/feature usually involved some background fact-checking, consulting the AWS documentation and other blogs, developing the code changes, and then writing the chapter.

For some concrete examples, these are chapters we worked on:
- Getting Started with the AWS CDK
- OAuth2 Login with AWS Cognito
- Storing Entities to PostgreSQL using RDS
- Structured Logging with Amazon CloudWatch
- etc.

While we had implemented similar features in the past, we still spent a reasonable amount of time reading the AWS documentation and related blog posts to ensure our previous assumptions were correct.

We also ensured every co-author worked independently on their own topic (like OAuth2 login or RDS setup) to avoid any misunderstandings.

Everybody was working on a dedicated chapter, so there wasn't any conflict or idle time due to waiting on someone else's input. Writing the new chapter consisted both of doing research, adjusting the sample application, and writing the manuscript.

As we were incrementally releasing a new version of the ebook, we tried to work on the modules and chapters in sequence. It should be more or less an append-only of chapters and no inline adding of chapters so that the readers who get a copy early on can continue reading the book where they left off once there's a new version available.

In parallel to our first release preparation, we created a basic [landing page](https://stratospheric.dev/) and signed up for a mailing list provider (ConvertKit back then). To keep things simple, we bought an HTML Bootstrap theme and used GitHub pages to quickly launch this landing page and add the mailing list signup form to allow potential readers to get more information about our progress:

![Stratospheric Landing Page](/img/stratospheric-ebook/stratospheric-landing-page-scroll-through.gif#center "Stratospheric Landing Page")

As there weren't any earnings, we kept the costs low to only invest more $$$ once we saw adoption of our book.

In a true Lean Startup / MVP fashion, this signup form also acted as a preliminary litmus test to see how many developers are interested in bringing this book over the finish line.

Before releasing the first version, we had to finalize our ebook title and find a logo and a cover.

As the book is all about getting ready for the cloud and effectively deploying applications to production in the cloud, the icon of a launching rocket seemed suitable. We started with the placeholder project name `aws101`. However, as this was clearly violating the trademarks of AWS, we had to find another name.

After some brainstorming for possible names, we ended up with `Stratospheric`. Much like the rocket icon, that term is fits the "cloud" metaphor quite nicely.

We ordered two design examples for the logo on Fiverr and picked the best one:

![Stratospheric ebook Cover](/img/stratospheric-ebook/stratospheric-ebook-cover.png#center "Stratospheric ebook Cover")

On the 8th of November 2020, we released the first manuscript. It took us approximately two months to publish the next revision from this day forward.

We started with a base price of $10, which we increased with each revision. Remember, that we get 80% royalties to be split equally among all authors.

## Iterate For 6-7 Month ✍🏻

What followed were multiple months of meeting every two weeks, discussing the next steps, and writing the book. This step-by-step approach allowed us to react to early reader feedback and stay motivated as we could release something out to the world.

I've used this same iterative approach with an [early bird audience for my first online course](https://progmot.com/post/creating-and-selling-my-first-online-course/).

While you may have the best ebook or product, if your potential readers and customers are not getting in front of it, it may be a waste of time.

As all three of us run a blog anyway, have an audience on Twitter, and some of us a mailing list, we started off with an existing target audience.

To spread the news about our project, we tweeted about our current progress occasionally. To stay in touch with existing and potential readers, we tried to get as many of them on our landing page to sign up for our mailing list.

We used both our social media channels and the mailing list to provide teasers and give constant updates about our progress. We wrote a mailing list update and slightly increased the price whenever we released a new version. This created scarcity for the existing audience to get the copy early while the manuscript was still in development.

Furthermore, we rotated among all co-authors to mix up the person in charge of writing the mailing list update.

Those who got their ebook early got it for the lowest price, which is fair as they trusted our project from day 1.

While we originally planned to use AWS CloudFormation templates for our infrastructure setup, we decided to rework the existing setup and use the AWS Cloud Development Kit (CDK). The AWS CDK was already getting more and more traction at the time, and this would also be a huge USP as not much of the available literature is already using the CDK.

On a high level, we ended up with these main modules for the ebook:

**1. Getting Started with AWS**

Getting used to AWS, its interfaces, its services, the management console, and how to automate the infrastructure deployment. This includes an introduction to the AWS CDK, our [custom CDK constructs Java library](https://github.com/stratospheric-dev/cdk-constructs), and some design decisions for building a CI/CD pipeline with GitHub Actions.

**2. Building the Sample Application**

Next, we dive into the actual application development. We showcase building must-have features while connecting to various AWS services:

- OAuth2 Login and user management with AWS Cognito
- email delivery with SES
- real-time browser notifications with WebSockets and Amazon MQ
- asynchronous workload operations with AWS SQS
- storing data in a relational database with RDS

We showcase the integration with AWS and Spring Boot based on meaningful feature implementations and enrich our sample Todo application with every chapter.

**3. Operating and Monitoring and Applications in Production on AWS**

Production is where the fun begins. We don't stop after developing the last feature and also cover monitoring and operating our Spring Boot application in production. This includes topics like structured logging, Amazon CloudWatch alerts, emitting metrics, creating operational dashboards, etc.

Looking back, these were the times we released a new _work in progress_ ebook version:

- Revision 0.1: 2020-11-08 (first release)
- Revision 0.2: 2020-12-20
- Revision 0.3: 2021-02-14
- Revision 0.4: 2021-04-10

![Stratospheric ebook Cover](/img/stratospheric-ebook/stratospheric-pre-release-version-overview.png#center "Stratospheric Pre Releases")

Revision 0.4 was our last pre-release, and we got our book to 80% at that time.

While we almost constantly released a new version every two months, the remaining 20% was the hardest part and took the longest (as usual, Pareto principle applies) ...

## Publishing Version 1.0 🥳

The last release was the one that took the longest. As is well-known, not only in project management, the remaining 20% of a project is where the most time is spent...

... this was also true for us.

We had some final content to write, but our most considerable effort went into final proofreading and alignment of the manuscript.

With three people on the team, everyone was doing their screenshots, custom diagrams, header structure, etc., slightly differently. However, we wanted to have a common, consistent style throughout the book.

Furthermore, everyone had a different understanding on when to use a *bold*, _italic_ statement, or when to use an info box, for example. This was something we wanted to unify across the book.

Next, we also replaced some of our architecture and information diagrams with nice-looking [Excalidraw](https://excalidraw.com/) diagrams:

![Stratospheric Excalidraw Image Example](/img/stratospheric-ebook/stratospheric-excalidraw-example.png#center "Stratospheric Excalidraw Image Example")

These finalization parts took almost two months as we also read the ebook from start to finish several times. We took the task of proofreading ourselves and did not hire someone to do this.

In total, we ended up with 450 pages of high-value content about Spring Boot and AWS.

The version 1.0 was to be both feature-complete as well as polished. We knew that our ebook journey didn't stop there but wanted to move the completion needle on Leanpub to 100%.

As the finalization of the manuscript went closer, we thought about the best possible way to announce and release version 1.0.

We were invited to the [German AWS Podcast](https://german-aws-podcast.libsyn.com/33-von-null-auf-produktion-mit-spring-boot-und-aws) by [Dennis Traub](https://twitter.com/dtraub) (AWS Developer Advocate) and could talk about our own AWS cloud journey and advertise the ebook a bit.

On top of this podcast, we decided to organize an online release party and invited both the existing ebook readers from our audience and other interested people.

We prepared a one-hour agenda for this release party, where we talked about the book's content, showcased the sample application, and the CI/CD workflow. We also had some time left for a Q&A session.

From the ~50 accepted invitations, twenty people showed up on a Sunday afternoon to celebrate the release with us.

After this 50 minutes of content, we released the final version of Stratospheric together with the audience by hitting the "Publish Now" button in Leanpub _together_ live during the video call.

{{< tweet user="rieckpil" id="1421811091152191488" >}}

{{ < tweet-single 1421811091152191488 >}}

We recorded this release party for those that couldn't make it to the live event on the 1st of August 2021 and [uploaded the video on YouTube](https://www.youtube.com/watch?v=oaWEKvVXucU):

{{< youtube oaWEKvVXucU >}}

We were all super happy with the outcome of the release party and with our progress. At that time, we already had 500 readers and got more and more attention.

## Life After the 1.0 Release 🏗

> A book is never finished; it's abandoned. (Gene Fowler)

While still being euphoric about releasing finish the first version of this book within one year, we knew that our journey wouldn't stop here. Right after the release party, we all took some time off and focused more on spreading the news about the release rather than planning what was next.

Since the release of version 1.0 in August 2021, we have seen tremendous adoption. The feedback from the readers is also excellent. We also created a Slack channel for Q&A and general communication for the ebook community.

Both Spring Boot and AWS are more or less mature, at least in the areas that we talk about: SQS, SES, RDS, web development, etc. Still, there's much going on for the library that we're using for integrating AWS services ([Spring Cloud AWS](https://awspring.io/)). Furthermore, we also learn even better practices or different ways of doing things.

Thanks to the agile nature of Leanpub and given the fact that we didn't have to ship a physical book to our readers, we are still able to update the ebook post-delivery. Leanpub has a feature to notify the readers about a new version that they can then download for free.

While we had no strict roadmap in mind, we all agreed to keep this book up-to-date to avoid a stale book.

Whenever there's a new update for our ebook, we also send out a small release information email to our newsletter to give a short overview of the changes:

![Stratospheric Post Release Mailing List Update](/img/stratospheric-ebook/stratospheric-post-release-mailing-list-update.png#center "Stratospheric Post Release Mailing List Update")

On the financial side, we don't get rich from selling this book. It's some additional pocket money for us in the range of $150-300 for every author each month.

To increase the visibility of our ebook, we listed it on Amazon Kindle. While Amazon's royalty rules are not that generous compared to Leanpub, we primarily publish on Amazon as well to get in front of more developers. Amazon is one of the most significant search interfaces after Google and YouTube.

We thought about a printed ebook version, but for now, we postponed this move as we believe our audience is more interested in reading technical books on their devices anyway. However, at least I'd like to have a physical copy of this book on my bookshelf sometime in the future.

Based on the feedback received so far, we also decided to build an online course on top of the ebook to provide some more in-depth coverage of various areas. Given my [existing experience with creating and launching technical online courses](https://progmot.com/post/creating-and-selling-my-first-online-course/), this will be a great opportunity to apply my lessons learned from my first courses.

Getting to the end of the book, some publishers started to reach out to us. They wanted to publish Stratospheric from their publishing house and bring it to various marketplaces.  The additional outreach may be significant, but the royalties are fairly small compared to Leanpub, especially when split into three equal parts.

To stay independent, we opted against a publisher and published the ebook ourselves on Amazon to at least have  the enormous search traffic coming from this major e-commerce platform. We know that Leanpub is a niche site, and not all developers are aware of this great source of technical books. However, given our existing audience from our blog, newsletter, Twitter, etc. we can easily make our potential readers aware via those channels.

At the time of writing this article, we have 800 readers, which is a great success 🥳

## Recommendations, Tips & Tricks, and Lessons Learned 🎩

What follows is an unordered list of hints and tips about this journey. If you plan to start a similar project, make sure to learn from our _mistakes_ and recommendations.

### Write Together, Not Alone

Writing a book together has a lot of benefits. It motivates you to keep going when you would otherwise have quit when working on your own.

We committed to delivering something every two weeks and had some high-level ideas regarding when the next release would be published. This goal-based approach allowed us not to veer off, but work towards the next milestone.

Especially if you're writing your first book, going it alone might feel like an insurmountable pile of work. Together, you get there step-by-step and can use the group's momentum.

Furthermore, when co-authoring a book, you'll also improve your writing skills by getting constant feedback from other co-authors.

We all had some background in writing technical content, which helped us a lot. Starting such a project with three people who have never written any technical blog before might be burdensome.

### Use an Iterative Approach

With an iterative approach, you don't have to lock yourself for a year in a wooden cabin in Norway and come back with a finished book.

Start small. Deliver small increments, do baby steps, and get feedback early.

We had a rough plan of what we wanted to cover but also adjusted a lot along the way.

Leanpub is the perfect platform for this. Especially if you are a developer, you'll really enjoy writing your manuscript in Markdown. No annoying formatting issues inside Word when trying to center images or tables.

Leanpub does the layouting and file generation jobs for you. All you have to do is ship the manuscript.

Pick a publisher that supports early-access programs if you don't want to go down the self-publishing route.

You might be super convinced about your idea and think it's the most genius book ever. However, this doesn't necessarily reflect reality. Get some early feedback mechanisms in place that help you quantify the interest. A mailing list or a dedicated Twitter account can be such a tool.

### Use Simple Tools

Keep it simple. Use free plans and share the login with your co-authors if necessary.

You can scale the tools and costs with your ebook's success.

We purchased a Bootstrap-based HTML theme for our landing page for some bucks and adjusted it to our needs. During the project's inception phase, and while the ebook still wasn't at 100% completion, we primarily used the landing page to attract potential readers. Our landing page had (and still has) a newsletter subscription form to keep potential readers around.

We started with the free plan of ConvertKit and recently migrated to MailerLite. The MailerLite pricing and plan structure was better for our needs.

Some other tools/services that we used:
- Grammarly for fundamental proofreading and typos
- Writing the ebook in our editor of choice. I personally used IntelliJ IDEA most of the time. I tweaked the editor settings to wrap the lines so that I can write more naturally without having to scroll endlessly horizontally or buy a curved monitor.
- Fiverr for designing creatives, the logo, and the ebook cover
- GitHub for collaboration and review
- Google Sheet to keep track of our costs
- Slack for internal and external (with the community) communication

### Find a Schedule to Keep Momentum

What helped us to keep the writing flow going was a fixed schedule. We met every two weeks for one hour and did a status update before planning the next steps.

What worked for us was:
- A Trello board with four columns: backlog, in progress, to review, done
- Meetings via Zoom
- Document writing standards within the repository
- Use GitHub Actions for basic automation

What personally worked for me was taking the first hour every morning to work on this project.

### Automate What Can Be Automated

As we all had a software developer background and mindset, we tried to automate everything that we could. We could even have automated the ebook publishing process using Leanpub's API.

GitHub Actions makes such automations almost effortless.

Adding links for further resources is both a curse and a blessing. It allows the interested reader to dive deeper into a topic. However, the links disappear over time and may no longer be accessible as the content might have moved, or the site may have been shut down.

We automated the hyperlink verification with a small GitHub Action and an npm package that checks all links (also internal manuscript links) on each commit:

```
name: Check for broken links
on: [push, pull_request]
jobs:
  broken-link-check:
    runs-on: ubuntu-latest
    name: Check for broken links in all Markdown files
    steps:
      - name: Check out source code
        uses: actions/checkout@v3

      - name: Set up Node 16
        uses: actions/setup-node@v3
        with:
          node-version: 16
          cache: 'npm'

      - name: Install NPM packages
        run: npm install

      - name: Check for broken links
        run: npm run check-links
```

### Reach Out for Advertisement

Start talking about your ebook on podcasts, conferences, and tweet about it as soon as possible.

We reached out to an AWS developer advocate during the inception phase to find possible ways of collaborating.

AWS has sponsored us with some gift vouchers so that we could run the infrastructure (almost) for free. We even were able to contribute a two-part article on the AWS Open Source blog to gain some traction for our project:

- [Getting started with Spring Boot on AWS: Part 1](https://aws.amazon.com/blogs/opensource/getting-started-with-spring-boot-on-aws-part-1/)
- [Getting started with Spring Boot on AWS: Part 2](https://aws.amazon.com/blogs/opensource/getting-started-with-spring-boot-on-aws-part-2/)

The [German AWS Podcast](https://german-aws-podcast.libsyn.com/33-von-null-auf-produktion-mit-spring-boot-und-aws) by [Dennis Traub](https://twitter.com/dtraub) (AWS Developer Advocate) was a fantastic way of spreading the word, too.

After finishing the book, AWS even sponsored us for $2500 on GitHub.

### Get an Email Address for Every Author

That's an optional recommendation, but we had a good experience with having a dedicated email for each co-author and a basic catch-all email like `info@yourbookname.com`.

We've registered our domain within Amazon Route 53. We've built a simple self-made email forwarding with Amazon SES, S3, and AWS Lambda. If you're curious about the implementation, check out the [source code on GitHub](https://github.com/stratospheric-dev/stratospheric/tree/main/utility/email).

### Work With Checklists

Whenever there was something that we couldn't or didn't want to automate, we created a checklist for it.

This way, we didn't forget a step for tasks we only performed occasionally.

As an example, this is our checklist for publishing a new ebook version:

![Stratospheric Sample Checklist](/img/stratospheric-ebook/stratospheric-sample-check-list-example.png#center "Stratospheric Sample Checklist")

### Rotate the Responsibilities

To avoid a single point of failure within the co-author team and mix things up, we rotated the various responsibilities.

Everyone should release a new ebook version every now and then.

We also have an "author of the week" keeping an eye on our feedback channels. That person also is the first responder and coordinator for GitHub issues, Slack notifications, and emails.

### Centralize the Feedback Channels

Right after the first readers got their copy, we started to get an increasing amount of messages via various channels:

- private DMs on Twitter
- Emails to our ebook email address and/or private email address
- Slack messages
- Feedback via Leanpub
- GitHub issues
- etc.

The various channels made it hard for us to keep track of all inquiries. Coordinating the response amongst the co-authors is difficult if someone gets a private Twitter DM.

Furthermore, many of these feedback channels lack transparency. If we wrote an answer to a specific question via email, no other reader would benefit from the response as the conversation only happens within two inboxes.

Back then, we decided to channel all feedback via public GitHub issues. Everyone can follow the status of the issue, can chime in, and see a list of already answered technical questions or feedback.

To streamline the feedback channel via GitHub issues and to ensure each issue contains some minimal required information (e.g., version of the ebook), we've created two GitHub issue templates: one for general feedback on the book and one for technical questions/issues with the sample application.

The GitHub issue template is backed by a YAML file and describes the required input fields:

`.github/ISSUE_TEMPLATE/BOOK-FEEDBACK.yml`

```yaml
name: Feedback for the ebook
description: "Everything related to the ebook: typos, layout issues, broken links, explanation gaps, inconsistencies, testimonials, etc."
labels: [ "ebook-feedback", "triage" ]
body:
  - type: markdown
    attributes:
      value: |
        Thanks for taking the time to provide feedback and improve the overall quality of Stratospheric!
  - type: textarea
    id: what-happened
    attributes:
      label: "What can we improve?"
      description: "Try to be as specific as possible - for example: On page 47, there's a typo in the word 'Strotospheric'."
    validations:
      required: true
  - type: input
    id: version
    attributes:
      label: Version
      description: "Which ebook version are you referring to? You can find the version as part of the changelog (one of the last pages). Pick 'latest' if you can't find it."
    validations:
      required: true
  - type: textarea
    id: suggested-change
    attributes:
      label: Suggested Changes
      description: What would you suggest to change or what do you expect as a reader?
```

The rendered version of this template looks like the following:

![Centralized Feedback via GitHub Issues](/img/stratospheric-ebook/stratospheric-ebook-create-github-issue.png#center "Centralized Feedback via GitHub Issues")

Whenever a reader now asks a question via any other channel, we redirect them to [GitHub](https://github.com/stratospheric-dev/stratospheric/issues) and ask them to submit their message there.

### Define Rules for Typesetting and Structural Elements

This would have helped us save some time for the final polishing and is one of our main lessons learned.

Three different authors have three different opinions on when to use bold or italic script. Sometimes there are even four opinions if you forget which rules you applied yesterday.

Examples of this include:

- When to use *bold*?
- When to use _italics_?
- When to use an info box?
- How to structure the headers?
- How to take a screenshot and which screenshot to take?
- What is an acceptable number of links on a book page?
- etc.

We did not cover and align those rules in detail during our early manuscript reviews. During the final proofreading session, we encountered the issue of non-consistent sentence highlighting.

As a result, we now have some basic standards on when and how to highlight sections or single words.

If you're starting from scratch, take some time with your co-authors to set clear definitions and create a one-pager for your typesetting rules.

### Have Fun

That's the most important takeaway. Find people you enjoy working with and from whom you can learn.

It's a side project, enjoy the experience, and learn as much as you can. It's your spare time. If it feels like a job, don't do it.

Don't expect to become rich by writing a book but instead, use this opportunity to establish a brand in your niche or use it as a way of establishing credibility and authority. I'm fairly certain co-authoring an ebook is more relevant than any basic certification for a specific topic.

## About the ebook Authors 🙋‍♂️

### Tom Hombergs

Tom is a seasoned software engineer with a passion for building systems in the simplest way possible. He is regularly blogging about Java, Spring, and AWS and is the author of [*Get Your Hands Dirty on Clean Architecture*](https://leanpub.com/get-your-hands-dirty-on-clean-architecture), giving hands-on advice on implementing a hexagonal architecture.

Find out more about Tom on [reflectoring.io](https://reflectoring.io) and his [Twitter profile](https://twitter.com/TomHombergs).

### Björn Wilmsmann

Björn Wilmsmann is an independent IT consultant who helps companies transform their business into a digital business. He designs and develops business solutions and enterprise applications for his clients. Björn provides hands-on training in technologies such as Angular and Spring Boot.

Find out more about Björn on [bjoernkw.com](https://bjoernkw.com) and his [Twitter profile](https://twitter.com/bwilmsmann).

Additional kudos belong to Björn, as he helped me finalize and proofread this article.

### Philip Riecks (That's Me)

Under the slogan _Testing Java Applications Made Simple_ Philip provides recipes and tips & tricks to accelerate your testing success and make testing joyful (or at least less painful). Apart from blogging, he's a course instructor for various Java-related online courses and is active on YouTube.

Find out more about Philip on [rieckpil.de](https://rieckpil.de) and his [Twitter profile](https://twitter.com/rieckpil).

If you have further questions or want some more details about a specific topic, let me know in the comments 👇🏻

PS: You can get a copy of the Stratospheric ebook at a discount [here](https://stratospheric.dev/).

Have fun writing your own book,\
Philip

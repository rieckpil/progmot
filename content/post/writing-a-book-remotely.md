---
title: "Writing a Book Remotely Without Ever Meeting In Person Before"
date: 2022-04-12T09:27:17+02:00
description: "TODO"
keywords: []
cover:
draft: false
tags: []
math: false
toc: false
---

Ideas for the main title:
(looking for a more positive word for lessons learned, Retrospective?)
- Lessons Learned: Writing a Technical eBook Remotely Without Ever Meeting In Person Before
- Lessons Learned: Writing a Technical eBook Remotely
- Interconnected World: Writing a Technical eBook Remotely
- How To Write a Technical eBook Remotely Without Every Meeting
- How we managed to write a book about AWS remotely

This article describes a one-year journey of writing [Stratospheric - From Zero to Production with Spring Boot and AWS](https://stratospheric.dev/) as a co-author with two other co-authors that I met on Twitter. We have never met in person before and managed to successfully write a 450+ in-depth guide on developing and deploying Java Spring Boot applications on AWS (Amazon Web Services).

In short, this article covers: ,
- How we self-published this eBook while writing the manuscript in Markdown
- How we promoted and sold the eBook
- How we organized ourselves to write the eBook in an asynchronous fashion while having 8hour time spans
- General tips, recommendations and lessons learned

The whole project was (and still is) a lot of fun. I learned a ton about AWS and got the chance to connect and work with knowledgeable and nice people.

The three co-authors are: [Tom](https://twitter.com/TomHombergs/) (🇩🇪 living in 🇦🇺), [Björn](https://twitter.com/bwilmsmann/) (🇩🇪), [Philip](https://twitter.com/rieckpil) (🇩🇪 - that's me).

Let's get started 🚀

## How We Found Each Other 👥

> Luck is what happens when preparation meets opportunity.

While scrolling through my Twitter feed, I saw a fellow technical blogger reaching out to other bloggers to organize a small knowledge exchange.

A small anecdote on how it started with a simple Tweet by Tom.

{{< tweet user="TomHombergs" id="1278635778722000902" >}}

We next met with the intention of sharing experience as tech bloggers. During the second or third meeting of this kind, Tom asked for fellow bloggers that would be interested in taking a closer look at AWS and Spring Boot and may want to write about it.

Björn and me who were participating in this meeting raised our hands. We've never met each other before. And partially knew each other from reading our blogs.

We organized a separate meeting to discuss more details and to get to know each other.

## Our Goals For This Project ⭐️

Before we started to work on this project we met several times to get to know each other and align our goals and expectations. While all three of us were working full-time for clients/an employer, we set the common understanding that this would be a fun side project.

We all have had some experience with AWS and Java in the past but wanted to learn more about this cloud provider in depth. When developing features for clients or customers we usually never had the time to explore the variety of AWS services available. 

One major goal of this remote writing project was to get better at developing Java applications on AWS. As Spring Boot was our default technology stack back then, the choice came naturally to write about this niche.

While there are many books on AWS in general, and Spring Boot, none of them talked about the full cycle for bringing a Spring Boot application to production on AWS.

Showcasing shiny features and machine learning capabilities of AWS is great, but teams also struggle to design an automated CI/CD pipeline to push their changes automatically on AWS.

Personal goals:

1. Learn about AWS
2. Improve writing skills and tick off 'writing a book' from our bucket list
3. Create awareness for ourselves to attract potential clients

This included the current experience with AWS and what our plans with this project would be.

Furthermore, the development journey doesn't stop when changing an implementation ticket to done and merging the code changes. Now, the fun part begins as our code runs in production.

If we are in the lucky position to maintain and operate our own service (DevOps done right), we will correspond with the following questions that arise sooner or later:

- How do I know my service is healthy and operating as expected?
- What's the current average response time for my most important API endpoint?
- What happened with the application yesterday night? As one of our users was complaining about errors.
- Where can I find and filter the logs from last Sunday?
- etc.

In short, this brought us to the following high-level goals for our readers that also influenced our manuscript:

1. Educate about AWS and IaaC with the AWS CDK
2. Develop Spring Boot with meaningful features (e.g., email notifications or OAuth2 login) while integrating as many AWS services as possible
3. Educate about best practices for running Spring Boot applications in production on AWS: monitoring, alerting, observability, etc.

Packed with these ideas, we then got started with the project.

## How We Got Started 🛫

(first Poc, outline chapters, start writing, some technical hints on the worklfow, why Leanpub)

We then started to met constantly every two weeks via Zoom and created a Slack workspace for communication and coordination. We organized ourselves in a Scrum-like setup and planned our two week _sprints_ with a Trello board. These bi-weekly Zoom calls were a mix of a daily review, and a planning session.

There wasn't any story point or product owner, we were all intrinsically motivated to get stuff done and used 
positive peer pressure, as everyone was reporting what they achieved in the last two weeks.

As a first step, we wanted to develop a small proof of concept application to explore which areas we could write about. We wanted our readers to complete the journey from knowing only a bit about AWS to having an automated CI/CD pipeline that deploys their application to production.

For the tech-stack, we picked what we felt most comfortable with: Java and Spring Boot with Spring Cloud AWS.

Besides, exploring AWS services on the go, every one of us had stories and best practices for various AWS services to share that the other co-authors could learn from.

Once we had a working sample application running on AWS and we were confident that the topic we were about to write added value, we started writing the book. We first sketched out a table of contents and started working on the different chapters in parallel.

We created a new AWS account for this project, and added three IAM users for us. Next, we created a GitHub organization that acted as an umbrella container for all related code repositories for this eBook project.

We more or less split this PoC time into two areas: automating the infrastructure setup with CloudFormation and developing a sample application. Back then we started with `.yaml` CloudFormation templates but moved quickly to the promising AWS CDK project.

As soon as we had a container cluster (ECS) with an automated CI/CD pipeline and the sample application with some basic features likes login with AWS Cognito and storing data within RDS ready, we started to plan the next steps.

This pilot area took about 2-3 months.

Next we needed to decide how we would write this book. The main question we had to answer was: should we talk to a publisher and pitch our idea or self-publish the whole thing?

As this project was a side-project for all three of us and not what we do full time, we all agreed that working with a formal publisher was not an option for us: working towards given deadlines and having to deliver a final piece on a fixed date was something we clearly wanted to avoid.

Furthermore, Tom already self-published his first book and then got a technical publisher on board to offer a print version and more distribution channels. Based on his experience and the common understanding, that this project may also fail, we went for the self-publishing approach.

When it comes to self-publishing book in the tech space, [Leanpub](https://leanpub.com/) is the de-facto choice.

Leanpub is really appealing for self-publishing tech authors as they offer the following:

- writing the manuscript in Markdown or bringing your own PDF
- automatic formatting/layout for Markdown manuscripts
- automatic file generation for other eBook formats like Mobi and ePub
- integration with GitHub/Dropbox for the manuscript
- fair pricing with 80% royalties for the authors
- payout via PayPal and support for multiple authors
- no payment/tax implications for the author: Leanpub acts as the merchant of record and takes ownership for the payment and tax handling (something I should have also favored for [my first online course](https://progmot.com/post/creating-and-selling-my-first-online-course/))

Leanpub is also built around the concept: Publish Early, Publish Often. They favor the approach of giving access to a book early while it's still in development and continuously adding new chapters to it.

Each [Leanpub eBook landing page](https://leanpub.com/stratospheric) provides information about the completeness and when the last changes were published:

![Stratospheric Completeness Bar](/img/stratospheric-ebook/leanpub-completness-bar-stratospheric-example.png#center "Stratospheric Completeness Bar")

Leanpub even allows creating preview versions of the eBook that we heavily used to see a rendered version of our recent changes. This helped us quite a lot when preparing a new eBook version.

We went for Leanpub because it's tech-friendly, easy-to-setup and offers fair royalties that the platform can automatically split between co-authors.

Having signed up for Leanpub, it was now time to finalize the technical setup to then get our hands dirty and start writing.

Working daily with GitHub, we choose a private GitHub repository for backing our manuscript markdown files. This allowed for a more seamless flow compared to uploading the files to a shared DropBox folder. With GitHub, we get versioning, automations with GitHub Actions, collaboration tools and a great feedback mechanism via pull requests.

We used the following branching strategy for the eBook:

- `main` -> generate eBook releases on Leanpub
- `preview` -> generate previews on Leanpub
- `personal-feature-branch`

Every co-author would work on their own branch and push their chapters to their dedicated branch. Once completed, we created a pull request to merge into the `preview` branch. This triggered our review process where all other co-authors reviewed the new section one after the other.

What's great about this review process is that we could leverage the review features of GitHub. This allowed the reviewer to directly make suggestions like fixing a typo or structuring the sentence. These suggestions could be then added automatically by the review owner:

![Providing Feedback via GitHub Pull Requests](/img/stratospheric-ebook/github-pull-request-suggestion-example.png#center "Providing Feedback via GitHub Pull Requests")

This way of working felt way more convenient than using a PDF reader, making comments and annotations to the file, and then sending it over to the owner of the changes.

After the review is completed by both other co-authors (six eye principle), we integrated the change into the `preview` branch to collect multiple chapters for the next release. Once every two month or so we then created the next work in progress release by merging the changes to the `main` branch.

All that's left to do is click the release button inside Leanpub to build a new digital version of our eBook. Theoretically, we can even automate this and publish a new release on each commit for the `main` branch.

## Getting the First Readers aka. Early Feedback 📖

(having something to show, i.e. a basic landing page, getting a cover, trouble with the naming, first versions on Leanpub)

Given the fact that we had figured out how to sell the eBook and how to write it, we now had to start writing the eBook.

We naturally found how to split the work and who would write what based on our own interests. While Björn and I were more focused on implementing features for the sample application and connecting various AWS services, Tom was more into the CI/CD and infrastructure setup.

While we had a rough idea and an early draft for our planned table of contents, we adjusted our plans along the way.

Working on a new chapter/feature usually involved some background fact checking, consulting the AWS documentation and other blogs, developing the code changes and then writing the chapter.

For some concrete examples, these are chapters we worked on:
- Getting Started with the AWS CDK
- OAuth2 Login with AWS Cognito
- Storing Entities to PostgreSQL using RDS
- Structured Logging with Amazon CloudWatch
- etc.

While we had implemented similar features in the past, we still spent a good amount of time reading the AWS documentation and related blog posts to ensure our previous assumptions were correct.

We also made sure every co-author worked independently on their own area (like OAuth2 login or RDS setup) to avoid any misunderstandings.

Everybody was working on a dedicated chapter so there wasn't any conflict or idle time due to waiting on someone else's input. Writing the new chapter consisted both of doing research, adjusting the sample application and writing the manuscript.

As were incrementally releasing new version of the eBook, we tried to work on the modules and chapters in sequence. It should be more or less an append-only of chapters and no inline adding of chapters so that the readers that get a copy early, and can continue reading the book where they left off, if there's a new version available.

In parallel to our first release preparation, we create a basic [landing page](https://stratospheric.dev) and signed up for a mailing list provider (Convertkit back then). To keep things simple, we bought an HTML Bootstrap theme and used GitHub pages to quickly launch this landing page and add the mailing list signup form to allow potential readers to get more information about our progress.

As there wasn't any earnings, we kept the costs low to only invest more $ once we see an adoption of our materials.

This signup form also acted as a preliminary litmus test for us to see how many developers are interested in bringing this book over the finish line.

Before we could release a first version, we had to finalize our eBook title, find a logo and a cover.

We started with the placeholder project name `aws101`. However, as this was clearly violating trademarks of AWS, we had to find another name. As the book is all about getting ready for the cloud and effectively deploy applications to production in the cloud, the symbol of a launching rocket seemed suitable.

After some brainstorming for possible names, we ended up with: `Stratospheric`.

We ordered two design examples for the logo on Fiverr and picked the best one:

![Stratospheric eBook Cover](/img/stratospheric-ebook/stratospheric-ebook-cover.png#center "Stratospheric eBook Cover")

On the 8th of November 2020, we released the first manuscript. From this day forward it took us approximately two months for the next revision to be published.

We started with a base price of $X. Keep in mind that we get 80% royalties but have to split those equally among all authors.

## Iterate For 6-7 Month ✍🏻

What followed were multiple months of meeting every two weeks, discussing the next steps and writing the book. This step-by-step approach gave us the ability to react to early reader feedback and stay motivated as we could release something out to the world.

I've used this same iterative approach with an [early bird audience for my first online course](https://progmot.com/post/creating-and-selling-my-first-online-course/).

While you may have the best eBook or product, if your potential readers and customers are not getting in front of it then it may be a waste of time.

As all three of us run a blog anyway, have an audience on Twitter and some of us a mailing list, we started off with an existing target audience.

To spread the news about our project, we tweeted about our current progress occasionally. To stay in contact with existing and potential readers, we tried to get as many of them on our landing page and signing up for our mailing list.

We used both our social media channels and the mailing list to tease= and give constant updates about our progress. Whenever we released a new version, we wrote a mailing list update and slightly increased the price.

To mix up the person in charge of writing the mailing list update, we rotated among all co-authors.

Those that got their eBook early, got it for the lowest price which is fair as they trusted in our project from day one.

While we originally planned to use AWS CloudFormation templates for our infrastructure setup, we decided to rework the existing setup and use the AWS Cloud Development Kit (CDK). The AWS CDK was getting more and more traction and this would also be a big USP as not many literatures uses the CDK already.

On a high level, we ended up with these main modules for the eBook:

1. Getting Started with AWS

Getting used to AWS, its interfaces, its services, the management console and how to automate the infrastructure deployment. This includes an introduction to the AWS CDK, our [custom CDK constructs Java library](https://github.com/stratospheric-dev/cdk-constructs) and some design decision for building a CI/CD pipeline with GitHub Actions.

2. Building the Sample Application

Next, we dive into the actual application development and how to build many must-have features of today's application while connecting to various AWS services: OAuth2 Login and user management with AWS Cognito, email delivery with SES, websockets for live updates, asynchronous workload operation with AWS SQS, storing data in a relational database with RDS. We showcase the integration with AWS and Spring Boot based on meaningful feature implementations and enrich our sample Todo application with every chapter.

3. Operating and Monitoring and Applications in Production on AWS

Production is where the fun begins. We don't stop after developing the last feature and also cover monitoring and operating our Spring Boot application in production. This includes topics like structured logging, Amazon CloudWatch alerts, emitting metrics, creating operational dashboard, etc.

Looking back, these were the times we released a new _work in progress_ eBook version:

- Revision 0.1: 2020-11-08 (first release)
- Revision 0.2: 2020-12-20
- Revision 0.3: 2021-02-14
- Revision 0.4: 2021-04-10

![Stratospheric eBook Cover](/img/stratospheric-ebook/stratospheric-pre-release-version-overview.png#center "Stratospheric Pre Releases")

Revision 0.4 was our last pre-release, and we got our book to 80% at that time.

While we almost constantly released a new version every two months, the remaining 20% was the hardest part and took the longest...

## Publishing Version 1.0 🥳

The last release was the one that took the longest. Like you always hear, the remaining 20% of a project is where the most time is spent...

... this was also true for us.

We had some final content to write but our biggest effort went into final proofreading and alignment of the manuscript.

With three people on the team, everyone was doing their screenshots, custom diagrams, header structure, etc. slightly different, and we wanted to have a common style through the book.

Furthermore, everyone had a different understanding on when to use a *bold*, _italic_ statement or when to use an info box. This was something we wanted to unify across the book.

Next, we also replaced some of our architecture and information diagrams with nice-looking [Excalidraw](https://excalidraw.com/) diagrams:

![Stratospheric Excalidraw Image Example](/img/stratospheric-ebook/stratospheric-excalidraw-example.png#center "Stratospheric Excalidraw Image Example")

These finalization parts took almost two months as we also read the eBook from start to finish several times. We took over the proofreading and did not hire someone to do this.

In total, we ended up with 450 pages of high-value content about Spring Boot and AWS.

The version `1.0` should be both feature complete as well as polished. We knew that our eBook journey didn't stop there, but wanted to finally move the completion needle on Leanpub to 100%.

As the finalization of the manuscript went closer, we thought about the best possible way to announce and release version 1.0.

We were invited to the [German AWS Podcast](https://german-aws-podcast.libsyn.com/33-von-null-auf-produktion-mit-spring-boot-und-aws) from Dennis Traub (AWS Developer Advocate) and could talk about our own AWS cloud journey and advertise the eBook a bit.

On top of this podcast, we decided to organize a release party and invited both the existing eBook readers and other interested persons from our audience.

For this release party we prepared a one-hour agenda where we talked about the content of the book, showcased the sample application and the CI/CD workflow and had some time left for a Q&A session.

From the ~50 accepted invitations, twenty people showed up on a Sunday afternoon to celebrate the release with us.

After this 50 minutes of content, we released the final version of Stratospheric together with the audience by hitting the "Publish Now" button in Leanpub _together_ live in the call.

{{< tweet user="rieckpil" id="1421811091152191488" >}}

We recorded this release party for those that couldn't make it to the live event on the 1st of August 2021 and [uploaded the video on YouTube](https://www.youtube.com/watch?v=oaWEKvVXucU):

{{< youtube oaWEKvVXucU >}}

We were all super happy with the outcome of the release party and with our progress. At that time, we already had 500 readers and were getting more and more attention.

## Life After the 1.0 Release 🏗

> A book is never finished; it's abandoned. (Gene Fowler)

While still being euphoric about releasing finish the first version of this book within one year, we knew that our journey wouldn't stop here. Right after the release party, we all took some time off and focused more on spreading the news about the release rather than planning what was next.

Ever since the release of version 1.0 in August 2021, we see great adoption based on readers' feedback, and also created a Slack channel for the community of the eBook for Q&A and general communication.

Both Spring Boot and AWS are more or less mature, at least in the areas that we talk about: SQS, SES, RDS, web development, etc. Still, there's much going on for the library that we're using for integrating AWS services ([Spring Cloud AWS](https://awspring.io/)). Furthermore, we also learn even better best practices or different ways of doing things.

Thanks to the agile nature of Leanpub and given the fact that we didn't have to ship a physical book to our readers, we are still able to update the eBook post delivery. Leanpub has a feature to notify the readers about a new version that they can then download for free.

While we had no strict roadmap in mind, we all agreed to keep this book up-to-date to avoid a stale book.

Whenever there's a new update for our eBook, we also send out a small release information email to our newsletter to give a short overview of the changes:

![Stratospheric Post Release Mailing List Update](/img/stratospheric-ebook/stratospheric-post-release-mailing-list-update.png#center "Stratospheric Post Release Mailing List Update")

On the monetary side of things: We don't get rich from selling this book. It's some additional pocket money for us in the range of $150-300 for every author each month.

To increase the visibility of our eBook we listed it on Amazon Kindle. While Amazon's royalty rules are not that optimal compared to Leanpub, we primarily list on Amazon to get in front of more developers. Amazon is one of the biggest search interfaces after Google and YouTube.

We thought about a printed eBook version but for now postponed this move as we think that our audience is anyway more interested to read technical books on their devices. However, (at least I) want to have a physical copy of this book in my bookshelf somewhere in the future.

Based on the feedback we got so far from our readers, we also decided to build an online course on top of the eBook to provide some more in-depth coverage of various areas. Given my [existing experience with creating and launching technical online courses](https://progmot.com/post/creating-and-selling-my-first-online-course/), this will be a great opportunity to apply my lessons learned from my first courses.

Getting to the end of the book, some publishers started to reach out to us. They wanted to publish Stratospheric from their publishing house and bring it to various marketplaces. We . The additional outreach may be great but the royalties are diminishing compared to Leanpub, especially if we have to split them into three equal parts. To stay independent we chose against a publisher and published the eBook ourselves on Amazon to have at least the big search traffic from this major ecommerce platform. We know that Leanpub is a niche site and not all developers are available of this great source of technical books. However, given our existing audience from our blog, newsletter, Twitter, etc. we make our potential readers aware via those channels.

At the time of writing this article, we have 800 readers, which is a great success 🥳

## Recommendations, Tips & Tricks, and Lessons Learned 🎩

What follows is an unordered list of hints and tips about this journey. If you plan to start a similar project, make sure to learn from our _mistakes_ and recommendations.

### Write Together, Not Alone

Writing a book together has a lot of benefits. It motivates you to keep going when you would otherwise quite when working on your own.

We committed to deliver something every two weeks and had some high-level ideas when the next release would be published. This goal-based work allowed us to not drift off and work towards the next milestone.

Especially if it's your first book, writing it alone might feel like a big pile of work. Together, you get there step-by-step and can use the momentum of the group.

Furthermore, when co-authoring a book, you'll also improve your writing skills as you get constant feedback the writing a lot by getting constant feedback.

We all three had some background in writing technical content that helped us a lot. Starting such a project with three people that have never written any technical blog before, might be a little burdensome.

### Use an Iterative Approach

With an iterative approach, you don't have to lock yourself for a year in a wooden cabin in Norway and come back with a finished book.

Start small. Deliver small increments, baby steps and get feedback early.

We had a rough plan of what we want to cover but also adjusted a lot along the way.

Leanpub is the perfect platform for this. Especially if you are a developer, you'll really enjoy writing your manuscript in Markdown. No annoying formatting issues inside Word when trying to center images or tables.

Leanpub does the lay-outing and file generation job your. You just ship your manuscript.

If you don't want to go the self-publishing route, pick a publisher that supports early access programs.

You might be super convinced about your idea and think it's the most wanted book ever. However, this doesn't necessarily reflect the reality. Get some early feedback mechanisms in place that help you quantify the interest. A mailing list or a dedicated Twitter account can be such a tool.

### Use Simple Tools

Keep it simple. Use free plans and share the login with your co-authors if necessary.

You can scale the tools and costs with your eBook's success.

For our landing page we purchased a bootstrap HTML theme for some bucks and adjusted it to our needs. During the inception phase of the project and while the eBook was not at 100, we primarily used the landing page to attract potential readers. Our landing page had (and still has) a newsletter subscription form to keep potential readers around.

We started with the free plan of ConvertKit and recently migrated to MailLite. The MailerLite pricing and plan structure was better for our needs.

Some other tools/services that we used:
- Grammarly for basic proofreading typos
- Writing the eBook in their editor of choice. I personally used IntelliJ IDEA most of the time. I tweaked the editor setting to wrap the lines so that I can write more naturally without having to horizontally scroll endlessly or buy a curved monitor.
- Fiverr for designing creatives, the logo and the eBook cover
- GitHub for collaboration and review
- Google Sheet to keep track of our costs
- Slack for internal and external (with the community) communication

### Find a Schedule to Keep Momentum

What helped us to keep the writing flow going was a fixed schedule. We met every two weeks for one hour and did a status updated and planned the next steps.

What worked for us was:
- A Trello board with four columns: backlog, in progress, to review, done
- Meetings via Zoom
- Document writing standards within the repository
- Use GitHub Actions for basic automation

What personally worked for me was taking the first hour every morning to work on this project.

### Automate What Can Be Automated

As we all had a software developer background, we tried to automate everything that we could. We could have also automated the eBook publishing using Leanpub's API.

GitHub Actions makes automations almost effortless.

Adding links for further resources is both a curse and a blessing. It allows the interested reader to dive deeper into a topic. However, the links rotten over time and may no longer be accessible as the content might have moved or the site got shut down.

We automated the hyperlink verification with a small GitHub Action and a npm package that checks all links (also internal manuscript links) on each commit:

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

Start talking about your eBook on podcasts, conferences, and tweet about it as soon as possible.

We reached out to an AWS developer advocate during the inception phase to find possible ways of collaboration.

AWS ha sponsored us some gift vouchers so that we could run the infrastructure (almost) for free. We could even sponsor a two-part article on the AWS Open Source blog to gain some traction for our project:

- [Getting started with Spring Boot on AWS: Part 1](https://aws.amazon.com/blogs/opensource/getting-started-with-spring-boot-on-aws-part-1/)
- [Getting started with Spring Boot on AWS: Part 2](https://aws.amazon.com/blogs/opensource/getting-started-with-spring-boot-on-aws-part-2/)

The [German AWS Podcast](https://german-aws-podcast.libsyn.com/33-von-null-auf-produktion-mit-spring-boot-und-aws) from Dennis Traub (AWS Developer Advocate) was also a great initiative to spread the word.

After finishing the book, AWS even sponsored us $2500 on GitHub.

### Get an Email Address for Every Author

That's an optional recommendation, but we made good experience with having a dedicated email for each co-author and a basic catch-all email like `info@yourbookname.com`.

We've registered our domain within Amazon Route 53. We've built a simple self-made email forwarding with Amazon SES, S3 and AWS Lambda. If you're curious about the implementation, check out the [source code on GitHub](https://github.com/stratospheric-dev/stratospheric/tree/main/utility/email).

### Work With Checklists

Whenever there was something that we couldn't or didn't want to automate, we created a checklist for it.

This way we didn't forget a step for tasks that we only occasionally performed.

As an example, this is our checklist for publishing a new eBook version:

![Stratospheric Sample Checklist](/img/stratospheric-ebook/stratospheric-sample-check-list-example.png#center "Stratospheric Sample Checklist")

### Rotate the Responsibilities

To avoid a single point of failure within the co-author team and to mix things up, we rotated the various responsibilities.

Everyone should release a new eBook version every now and then.

We also have an "author of the week" that keeps an eye on our feedback channels and is the first responder and coordinator for GitHub issues, Slack notifications and emails.

### Centralize the Feedback Channels

Righter after the first readers got their copy, we started to get an increasing amount of messages via various channels:

- private DMs on Twitter
- Emails to our eBook email address and/or private email address
- Slack messages
- Feedback via Leanpub
- GitHub issues
- etc.

The various channels made it hard for us to keep track of all inquiries. Coordinating the response among the co-author is difficult if someone gets a private Twitter DM.

Furthermore, many of these feedback channels lack transparency. If we wrote an answer to a specific question via email, no other reader would benefit from the response as the conversation only happens within two inboxes.

Back then we decided to channel all feedback via public GitHub issues. Everyone can follow the status of the issue, can chime in and see a list of already answered technical questions or feedback.

To streamline the feedback channel via GitHub issues and to ensure each issue contains some minimal required information (e.g. version of the eBook), we've created two GitHub issue templates: one for general feedback to the book and one for technical questions/issues with the sample application.

The GitHub issue template is backed by a YAML file and describes the required input fields:

`.github/ISSUE_TEMPLATE/BOOK-FEEDBACK.yml`

```yaml
name: Feedback for the eBook
description: "Everything related to the eBook: typos, layout issues, broken links, explanation gaps, inconsistencies, testimonials, etc."
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
      description: "Which eBook version are you referring to? You can find the version as part of the changelog (one of the last pages). Pick 'latest' if you can't find it."
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

Whenever a reader now asks a question via any other channel, we redirect them to GitHub and ask them to submit their message there.

### Define Rules for Typesetting and Structural Elements

This would have helped us save some time for the final polishing and is one of our main lessons learned.

Three different authors have three different opinions on when to use bold or italics. Sometimes there are even four opinions if you forget which rules you applied yesterday.

Examples for this include:

- When to use *bold*?
- When to use _italics_?
- When to use an infobox?
- How to structure the headers?
- How and which screenshot to take?
- What is an acceptable number of links on a book page?
- etc.

During our early manuscript reviews we did not cover and align those rules in detail. Only during the final proofreading session we encountered that there's a mix and it's not consistent throughout the book.

As a result, we now have some basic standards on when and how to highlight sections or single words.

If you're starting from scratch, take some time with your authors to define clear definitions and create a one-pager for your typesetting rules.

### Have Fun

That's the most important takeaway. Find people that you enjoy working with and that you can learn from.

It's a side project, enjoy the experience, learn as much as you can. It's your spare time. If it feels like a job, don't do it.

Don't expect to become rich by writing a book but use this opportunity to establish a brand in your niche or use it as a form of credibility. I'm pretty sure that co-authoring an eBook weighs more than any basic certification for a topic.

## About the eBook Authors 🙋‍♂️

### Tom Hombergs

Tom is a seasoned software engineer with a passion for building systems in the simplest way possible. He is regularly blogging about Java, Spring, and AWS and is the author of [*Get Your Hands Dirty on Clean Architecture*](https://leanpub.com/get-your-hands-dirty-on-clean-architecture), giving hands-on advice on implementing a hexagonal architecture.

Find out more about Tom on [reflectoring.io](https://reflectoring.io) and his [Twitter profile](https://twitter.com/TomHombergs).

### Björn Wilmsmann

Björn Wilmsmann is an independent IT consultant who helps companies transform their business into a digital business. He designs and develops business solutions and enterprise applications for his clients. Björn provides hands-on training in technologies such as Angular and Spring Boot.

Find out more about Björn on [bjoernkw.com](https://bjoernkw.com) and his [Twitter profile](https://twitter.com/bwilmsmann).

### Philip Riecks (That's Me)

Under the slogan _Testing Java Applications Made Simple_ Philip provides recipes and tips & tricks to accelerate your testing success and make testing joyful (or at least less painful). Apart from blogging, he's a course instructor for various Java-related online courses and active on YouTube.

Find out more about Philip on [rieckpil.de](https://rieckpil.de) and his [Twitter profile](https://twitter.com/rieckpil).

PS: If you have further questions or want some more details about a specific topic, let me know in the comments 👇🏻

Have fun writing your own book,\
Philip

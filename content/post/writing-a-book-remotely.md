---
title: "Writing a book remotely without ever meeting before"
date: 2020-10-11T09:27:17+02:00
slug: ""
description: ""
keywords: []
draft: true
tags: []
math: false
toc: false
---

Titles:
(more positive word for lessons learned)
- Lessons Learned: Writing a Technical eBook Remotely Without Ever Meeting In Person Before
- Lessons Learned: Writing a Technical eBook Remotely
- Interconnected World: Writing a Technical eBook Remotely
- How To Write a Technical eBook Remotely Without Every Meeting
- How we managed to write a book about AWS remotely

This article describes my one-year journey to write [Stratospheric - From Zero to Production with Spring Boot and AWS](https://stratospheric.dev/) as a co-author with two other co-authors that I met on Twitter. We never met in person before and while writing and still managed to successfully write a 450+ in-depth guide on AWS and Spring Boot.

We self-published this, promotion strategies, connecting to the readers, money side of things, how we organized ourselves, which processes we followed

Short intro about this article. What worked, how we organized ourselves.

The book is all about AWS and Spring Boot. Getting your Spring Boot application into production.

Our journey to writing a technical book remotely together without having met each other in person before.

Three co-authors: [Tom](https://twitter.com/TomHombergs/), [Björn](https://twitter.com/bwilmsmann/), [Philip](https://twitter.com/rieckpil) (that's me).

Structure:
- How we got together
- Our goals
- How we started (first Poc, outline chapters, start writing)
- Getting the first readers on it
- Iterate: Continuously improve for 6-7 month
- Publishing version 1.0: Proofreading, aligning the wording,
- Iterate aka. nach dem Release ist vor dem Release: Continue with further updates, fast changing cloud environment, online course

- Short list of tips & tricks: Email addresses, Landing page, Grammarly, Link Checker, GitHUb issue templates -> feedback will come in many ways, best is centralized and open, if you write with multiple persons, set some image/text rules ahead. You'll save time aligining the manuscript afterward.

## How We Got Together

> Luck is what happens when preparation meets opportunity.

While scrolling through my Twitter feed I saw a fellow technical blogger reaching out to other bloggers to organize a small knowledge exchange.

Small anecdote how it started with a simple tweet by Tom.

We next met with the intent to share experience as tech bloggers. During the second or third meeting of this kind, Tom asked for fellow bloggers that would be interested in taking a closer look at AWS and Spring Boot and may want to write about it.

Björn and me who were participating in this meeting raised our hands. We've never met each other before. And partially knew each other from reading our blogs.

We organized a separate meeting to discuss more details and to get to know each other.

## How it started

In our first meetings we first got to know each other better. We first wanted to ensure our expectations for this project align. While we were all three working full-time for clients/an employer, we set the common understanding that this will be a fun side project.

In the first meetings that we organized bi-weekly we were first getting to know each other better. This included the current experience with AWS and what our plans with this project would be.

We then met constantly every two weeks and

As a first step, we wanted to develop a small proof of concept application to explore which areas we can write about. We wanted our readers complete the journey from only a bit about AWS to having a automated CI/CD pipeline that deploys their application to production.

For the tech-stack we picked what we felt most comfortable with: Java and Spring Boot with Spring Cloud AWS.

Besides educating the reader about this topic, we also had a big self-interest as we were all using AWS almost on a daily basis and wanted to get to know it in more detail. Every one of us had stories and best practices for various AWS services to share that the other co-authors could learn from. Win-win!

We opened a new AWS account for this project, created three IAM users for us and a GitHub organization called to organize ourselves.

We started with the project name `aws101`. However, was this was clearly violating trademarks of AWS, we had to find another name. As the book is all about getting ready for the cloud and effectively deploy applications to production in the cloud, the symbol of a starting rocket seemed natural.

After some brainstorming for possible names, we ended up with: `Stratospheric`.

We ordered two design examples for the logo on Fiverr and picked the best:

INSERT LOGO HERE

## Getting Early Feedback

While you can have the best eBook or product, if your potential readers and customers are not getting in front of it.

As we all three are running a blog, have an audience on Twitter and some of us a mailing list, we started off with an existing target audience.

To spread the news about our project, we tweeted about our current state every now and then. To capture the email address of potential readers and to outline our goal with the book, we created a basic landing page.

Nothing fancy, a simple $50 bootstrap HTML theme that we bought, tweaked and launched via GitHub pages to the Internet.

Convertkit for the mailing provider to learn about a new one (we recently switched to MailerLite).

As there wasn't any earnings, we kept the costs low to only invest more $ once we see and adoption.

Getting people to your waiting list for the book, doesn't necassarly mean they'll also pull out their credit card once the eBook lands.

We used both our social media channels and the mailing list to teaser and give constant updates about our progress.

To mix up the person in charge of writing the mailing list update, we rotated among all co-authors.

Leanpub supports selling eBooks in their early stage. They even have a progress bar on each eBook's landing page indicating how far the content is and when it was updated. Combining this with an incremental price increase, lets readers join early and benefit from all future updates.

Show progress bar example with WIP and one with completed

We started with a base price of $X. Keep in mind that we get 80% royalties but have to split those equally among all authors.

Overall, Similar approach to my iterative course launch with early access program.

## How We Continued

After developing a the proof of concept application and having automated everything with CloudFormation, we were sure that we have enough to show and committed to writing the book.

While the AWS CDK was getting more and more traction in the meantime, we decided to rework the infrastructure setup and use the CDK instead of CloudFormation templates.

Not much in-depth content for this complex domain. We all had some experience with AWS but there were clearly parts that we're not understanding in detail

Project to learn and will learning produce something

Structure of the eBook:

1. Getting Started with AWS

Get used to AWS, its interfaces, its services and the management console (a bit as we try to automated everything with the AWS CDK). This includes an introduction to the AWS CDK, our custom CDK constructs Java library and some design decision for building a CI/CD pipeline with GitHub Actions.

2. Building the Sample Application

Next, we dive into the actual application development and build many must-have features of today's application while connecting to various AWS services: OAuth2 Login and user registration with AWS Cognito, email delivery with SES, websockets, asynchronous workload operation with AWS SQS, storing data in an relational database with RDS. We showcase the integration with AWS and Spring Boot based on meaningful feature implementations and enrich our sample Todo application with every chapter.

3. Operating and Monitoring and Applications in Production on AWS

Production is where the fun begins. We don't stop after developing the last feature but also cover monitoring and operation our Spring Boot application in production. This includes topics like structured logging, Amazon CloudWatch alerts, emitting metrics, creating operational dashboard, etc.

## Getting Started With Writing the Book

Once we had a working sample application running on AWS and were confident that the topic we're about to write adds value, we started writing the book. We first sketched out a table of contents and started working on the different chapters in parallel.


Everybody was working on a dedicated chapter so there wasn't any conflict or waiting. Writing the new chapter consisted both of doing some resarch, adjusting the sample application and writing the manuscript.

As were incrementally releasing new version of th eBook, we tried to work on the modules and chapters in sequence. It should be more or less and append-only of chapters and no inline adding of chapters so that the readers that get a copy early, can continue reading the book were they left if there's a new version available.

I've used this same iterative approach with an [early bird audience for my first online course](https://progmot.com/post/creating-and-selling-my-first-online-course/) and we saw the same benefits for this book.

As this project was or all three of us a side-project and nothing we do full time, we all agreed that working with a formal publisher is no option for us. Working towards given deadlines and having to deliver a final piece on a fixed date was something we clearly wanted to avoid.

Furthermore, Tom already had one of his eBooks published by a technical publisher and wasn't that convinced.

As Tom already had self-published an eBook on Leanpub before, we went for Leanpub as their services are appealing for self-publishing tech authors:

- write the manuscript in Markdown
- formatting comes automatically
- direct integration with a GitHub repository
- fair pricing with 80% royalties
- payout via PayPal and support for multiple authors
- Leanpub acts as the marchant of record and takes ownership for the payment and tax handling

Release early and often. They favor the approach of giving access to a book early while it's still in development.

SHOW progress bar

We choose Leanpub as it's tech-friendly, easy-to-setup and great royalties. Leanpub is a self-publishing platform mostly focussing on tech books.

The manuscript is backed by a private GitHub repository.

Leanpub allows creating preview versions of the eBook that we heavily used to see a rendered version of our recent changes.

To gain some traction and to see if there's interest in such a book, we started with a basic landing page and collecting email addresses for a mailing list.

On the XY of November 2020, we released the first manuscript. From this day forward it took us approximately two months for the next revision to be published.

The final release was on August 2021. At the end we did some final checks for consistency, wording, and typos which took a little longer.

To make the final release (version 1.0, there's no final release ever), we organized a release party and invited both the existing eBook readers as well as other interested persons from our audience.

We talked about the sample application, the way we deploy the application, how we wrote the book, gave a feature demo and hit the release button on Leanpub together.

The recording of this release party is [available on YouTube](https://www.youtube.com/watch?v=oaWEKvVXucU).

## Organization

Bi-weekly calls via Zoom to have a mix of a daily, review and planning in a one hour session.

We were using a basic Trello board with some backlog columns, a In progress and one review column.

We cross-read all out manuscript and therefore had

Grammarly was another big help to spot some low hanging typo, grammatical and syntactical issues.

Excalidraw for some nice-looking diagrams

TODO: Add Excalidraw example picture

Pull request via GitHub.

We had the following _branching strategy_ for the eBook:
- `main` -> generate eBook releases on Leanpub
- `preview` -> generate previews on Leanpub
- `personal-feature-branch`

Every co-author would work on their own branch and write their chapters. Once completed, we created a pull request to merge into the `preview`. This triggered our review process where all other co-authors reviewed proposed writings one after the other.

After the review is completed, we integrated the change into the `preview` branch to collect multiple chapters for the next release. Once every two month we then created the next work in progress release by merging the changes to the `main` branch.

TODO: Insert excalidraw

## Incrementally building

Leanpub is supporting this mode, we can publish work-in-progress version and use a percentage bar to inform potential readers how far we are in the process.

## Releasing the Book

Add a basic timeline with our release dates and how far we came.

The last release was the one that took the longest. Before we put the version `1.0` out and mark this eBook as complete on Leanpub, we wanted to polish and proofread the entire book by ourselves. This took some additional 2-3 weeks.

## After

Live since August 2021. Great adoption, we also now have a Slack channel for the community of the eBook.

Monetary information: We don't get rich. It's some additional pocket money for us in the range of $150-300 for each author.

To increase the visibility of our eBook we included it on Amazon. While Amazon's royalty rules are not that optimal compared to Leanpub, we primarly list on Amazon to get in front of more developers. Amazon is one of the biggest search interfaces after Google and YouTube.

We thought about an printed eBook but for now postponed this move as we think that our audience is anyway more interested to read technical books on their devices.

Some readers even requested more in-depth coverage and hence we decided to build an online course on top of it.

Given my [existing experience with building and launching technical online courses](https://progmot.com/post/creating-and-selling-my-first-online-course/), this will be a great opportunity to apply my lessons learned from my first courses.

## Tips

Writing together motivates to keep going. We all committed to deliver something and had some high level ideas when the next release would be published.

Improve the writing a lot by getting constant feedback.

Made a lot of fun, learned a ton about AWS, met and get to know great and knowledgeable people.

Iterative approach, collect emails from interested people.

Meeting schedules, continuous sprints, peer review

We were using a Trello board for our task planning. We grouped our tasked in columns like: marketing, backlog, in progress, in verify, done.

This helped us keep an overview of what is currently in progress and what still needs to be done.

AWS sponsored us some gift vouchers so that we could run the infrastructure (almost) for free. We could even sponsor a two-part article on the AWS Open Source blog to gain some traction for our project.

After the book was published, we even got a great donation from AWS for our project via GitHub.

Keep it simple, shared logins for the tools.

For our laning page we purchased a bootstrap HTML theme for some bucks and adjusted it to our needs. During the inception phase of the project and while the eBook was not at 100, we primarily used the landing page to attract potential readers. Our landing page had (and still has) a newsletter subscription form to keep potential readers around.

Used tools:

Writing the eBook in their editor of choice. I personally used IntelliJ IDEA most of the time.

I tweaked the editor setting to wrap the lines so that I can write more naturally without having to horizontally scroll endlessly or buy a curved monitor.

GitHub suggestion feature for the PR. Show example. The collaboration makes fun. Immediate feedback and now need to send Word files via email and use the comment functionality of Word.

Leanpub removed the barriers of formatting a nice-looking PDF and publishing it in various formats.

Getting to the end of the book, some publishers started to reach out to us. They wanted to publish Stratospheric from their publishing house and bring it to various marketplaces. We . The additional outreach may be great but the royalties are diminishing compared to Leanpub, especially if we have to split them into three equal parts. To stay independent we chose against a publisher and published the eBook ourselves on Amazon to have at least the big search traffic from this major ecommerce platform. We know that Leanpub is a niche site and not all developers are available of this great source of technical books. However, given our existing audience from our blog, newsletter, Twitter, etc. we make our potential readers aware via those channels.

Running Grammarly to spot low-hanging fruits when it comes to grammar and typos.

All changes were reviewed by all of us

`main` branch -> final output
`preview` branch -> generate a preview PDF

We were writing our content on feature branches and integrated them into the `preview` branch. Once we had enough reviewed sections in the `preview` branch, we released a new

Automation: We could even directly release from the main branch, but we prefer to still do it manually. PDF, Kindle, ePub format.

The final result was release on the first of August 2021: 450 pages long eBook

We even organized a small release party where we talked about the project, the sample application and hit the release button together.

Since the release, we're still meeting each other on a bi-weekly basis. We add reader feedback, keep the source code up-to-date and add new section where it makes sense.

With currently more than 700 readers

Adding links for further resources is both a curse and a blessing. It allows the interested reader to dive deeper into a topic. However, the links rotten over time and may no longer be accessible as the content might have moved or the site got shutdown. We automated the hyperlink verification with a small GitHub Action and a npm package that checks all links (also internal manuscript links) on each commit:

SHOW Link verify mechanism.

This helped us to identify and replace rotten links

## About the eBook authors

### Tom Hombergs

### Björn Wilsmann

### Philip Riecks


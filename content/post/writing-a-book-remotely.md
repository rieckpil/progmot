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

Short intro about this article. What worked, how we organized ourselves. The book is all about AWS and Spring Boot. Getting your Spring Boot application into production.

Our journey to write a technical book remotley together without having met each other in person before.

Three co-authors: Tom, Björn, Philip.

## How we got together

Small anecdote how it started with a simple Tweet by Tom.

We next met with the intent to share experience as tech bloggers. During the second or third meeting of this kind, Tom asked for fellow bloggers that would be interested in taking a closer look at AWS and Spring Boot and may want to write about it.

Björn and me who were participating in this meeting raised our hands. We've never met each other before.

We organized a seperate meeting to discuss more details and to get to know each other.


## How it started

In the first meetings that we organized bi-weekly we were first getting to know each other better. This included the current experience with AWS and what our plans with this project would be.

We then met constantly every two weeks and

We started with the project name `aws101`. However, was this was clearly violating trademarks of AWS, we had to find another name. As the book is all about getting ready for the cloud and effectively deploy applications to production in the cloud, the symbol of a starting rocket seemed natural.

We ordered two design examples for the logo on Fiverr and picked the best:

INSERT LOGO HERE


While the AWS CDK was getting more and more traction in the meantime, we decided to rework the infrastructure setup and use the CDK instead of CloudFormation templates.

Stratospheric

Not much in-depth content for this complex domain. We all had some experience with AWS but there were clearly parts that we're not understanding in detail

Project to learn and will learning produce something

Structure of the eBook:

1. Getting Started with AWS
2. Building the sample application
3. Operating and montoring and application in production on AWS

## Getting Started With Writing the Book

Once we had a working sample application running on AWS and were confident that the topic we're about to write adds value, we started writing the book. We first sketched out a table of contents and started working on the different chapters in parallel.

Everybody was working on a dedicated chapter so there wasn't any conflict or waiting. Writing the new chapter consisted both of doing some resarch, adjusting the sample application and writing the manuscript.

As were incrementally releasing new version of th eBook, we tried to work on the modules and chapters in sequence. It should be more or less and append-only of chapters and no inline adding of chapters so that the readers that get a copy early, can continue reading the book were they left if there's a new version available.

I've used this same iterative approach with an [early bird audience for my first online course](https://progmot.com/post/creating-and-selling-my-first-online-course/) and we saw the same benefits for this book.

As this project was or all three of us a side-project and nothing we do full time, we all agreed that working with a formal publisher is no option for us. Setting deadlines and having to deliver a final piece on a given date was something we clearly wanted to avoid.

As Tom already had self-published an eBook on Leanpub before, we went for Leanpub as their services are appealing for self-publishing tech authors:

- write the manuscript in Markdown
- formatting comes automatically
- direct integration with a GitHub repository
- fair pricing with 80% royalties
- payout via PayPal and support for multiple authors

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


## Tips

Made a lot of fun, learned a ton about AWS, met and get to know great and knowledgeable people.

Iterative approach, collect emails from interested people.

Meeting schedules, continuous sprints, peer review

We were using a Trello board for our task planning. We grouped our tasked in columns like: marketing, backlog, in progress, in verify, done.

This helped us keep an overview of what is currently in progress and what still needs to be done.

AWS sponsored us some gift vouchers so that we could run the infrastructure (almost) for free.

We could even sponsor a two-part article on the AWS Open Source blog to gain some traction for our project.

basic landing page

Used tools:

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

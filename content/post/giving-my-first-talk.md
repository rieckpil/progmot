---
title: "Giving My First Talk at a Public Conference"
date: 2022-06-20T11:00:00+02:00
slug: "/giving-my-first-talk-at-a-public-conference"
aliases: ["/post/giving-my-first-talk-at-a-public-conference"]
author: "Philip"
summary: "Journey & Lessons Learned - Stepping out of my comfort zone to give a technical talk at a public conference in front of more than 150 developers."
description: "Journey & Lessons Learned - Stepping out of my comfort zone to give a technical talk at a public conference in front of more than 150 developers."
cover:
  image: "/img/featured-images/conference-speaker-microphone-midjourney.png"
  alt: "Conference Speaker Microphone"
  caption: "Conference Speaker Microphone"
  relative: false
keywords: []
draft: false
tags: []
ShowToc: true
trackingPixel: "932be61c51924494abe93c4e06c178ee"
---

> Life happens outside of your comfort zone - everything else is just repetition ⭐️

For a long time, I've been thinking about giving a talk at a public conference. While I've already held technical knowledge-sharing sessions internally for colleagues or clients, I've never stood on stage _in public_.

Back on the 27th of May 2022, I could tick off this item from my bucket list as I gave my first talk: 'How fixing a broken window cut down our build time by 50%' at the [Spring I/O](https://springio.net) in Barcelona. The conference had 1200 attendees and around 60 speakers. In total, more than 150 attendees came to my talk.

This article describes my journey to giving my first talk, including the lessons learned and how I prepared for this event.

## Deciding to Give a Talk

There was this one item on my yearly goal list that I kept moving to my next year's goal list.

I was procrastinating a lot on giving my first public talk and always wanted to find the right moment. While I submitted some talk ideas to three different conferences, back in 2019, none of them got accepted.

Somehow, though, by none of these submissions was I feeling that I really wanted to give this talk. It was a more self-obligated duty just to submit something so that I could tell myself I tried it.

When the whole work-from-home period started, I first thought a remote conference might be an easy way to get started. However, I wanted to experience standing in front of a real audience and not staring into a screen.

Actually, I have seen many speakers complain that online conferences are sometimes even harder because you have no immediate feedback from the audience. Even worse, if every participant turns off their camera, you can't see how the talk is going.

That's why I decided to pause this goal and wait until in-person conferences were happening again.

Then, somewhere around the beginning of 2022, I saw on Twitter that the CFP (call for papers) for the Spring I/O 2022 started. The Spring I/O is a community organized (mainly by Sergi Almar) conference in Barcelona, Spain. Its focus is on the Spring framework, the de facto standard framework (next to Jakarta EE and Quarkus) for developing Java applications.

The [Spring I/O conference](https://springio.net) is a community organized conference and has no (direct) affiliation with VMWare. It was the 9th iteration of this conference and in the past, more than 1000 people participated.

During the pandemic, they switched to a remote conference, and the conference in 2022 would be the first in-person conference after this break.

I somehow felt that this was the right conference for me as it fits 100% to my blogging niche, and I knew various previous speakers that I could ask for help and insights.

For a long time, I've always had a talk idea in my head. It was regarding a project experience with a great learning analogy and background information. It was both full of actionable takeaways, lessons learned, and practical advice based on a real project on software development.

After spending 30 minutes finalizing the talk title, elevator pitch, and description, I submitted the talk.

I didn't think this was too big of an audience for an unknown speaker with zero experience on a public stage. I thought, "Let's submit the talk and see what happens".

## Getting Accepted for the Conference

On the 17h of March 2022, I got a positive COVID test result after feeling sick for almost two days 😣

To recover and relax, I enjoyed the entire day on my couch, surfing the web and watching YouTube videos.

Somewhere around 3 pm that day, I checked my emails and found an email from the Spring I/O conference organizer ...

I GOT ACCEPTED 🥳!

![Talk Selection](/img/first-talk/talk-selection.png#center "Talk Selection")

As there is some gap time between the deadline for the call for papers (CFP) and the day the organizers announce the lucky speakers, I almost already forgot about the talk submission.

What a feeling of joy at this point despite having COVID and being sick.

That day was an entire emotional roller coaster. In the morning, the COVID test really shaped my day in a negative sense and I thought the day was over...

... and then in the afternoon, I received a confirmation email that I was going to be a speaker at the conference. I couldn't be happier. The sickness became secondary.

Looking back, it seems that I was quite lucky being selected while having just one talk submitted. While many conferences allow you to submit multiple talks, I went all-in with this one. The main reason was that only for this particular talk I was feeling confident enough to present this idea as my first talk at a public conference.

With the talk being accepted, the countdown started, and it was time to prepare and train for the conference day. I only had the title, elevator pitch, and a description.

I didn't have a single slide yet ...

## The Talk Idea

The talk was about a journey and our lessons learned from optimizing our integration test setup and reducing the overall build time by 50% from 26 to 12 minutes.

The common thread throughout my talk was about the [Broken Windows Theory](https://en.wikipedia.org/wiki/Broken_windows_theory). While this theory comes from the criminological area, it can be applied to almost everything.

In short, this theory describes that in rural areas where there's much litter on the ground, damaged cars, and rundown houses, the likelihood that similar _crime_ happens is more likely than in a neighbourhood where everything is spotless.

![Broken Window](/img/first-talk/broken-window.jpg#center "Broken Window")

We can transfer this analogy to software projects. As soon as a team member introduces a not-so-optimal workaround to our code base, the more likely it is that other developers will follow. This can drain our overall project health as the first _broken window_ entails potentially more broken windows.

Back in 2019, I was working on a project where we had a broken window inside our codebase. It resulted in ever-increasing build times, and the overall team motivation started to decline. After some initial hurdles, we could fix this broken window and bring our project health back to a clean state.

{{< newsletter-advertisement >}}

## Preparing the Talk

The requirements for this talk were crystal clear: I got 50 minutes. This includes the presentation and time for a live Q&A. As the audience is from all around the world (mostly Europe), the language had to be English.

As a rough ballpark figure, I was expecting 150-250 attendees for my talk as the overall conference had 1200 attendees and four parallel tracks.

While I had some basic bullet points and ideas for the talk in mind, I did not start with the actual preparation until 60 days before the conference.

I didn't want to prepare my slides all at once and instead invested one to two hours daily in preparing the talk. I already had the main topic for the talk in my head and just needed to put my outline _on paper_.

Most of the time, I worked on the talk in the morning so I could tick off this important item on my daily task list quite early. This continuous talk creation helped me stay creative and not work under pressure one week before the talk.

I frequently switched places for this kind of creative work and primarily prepared the talk in cozy cafés or co-working places in Berlin:

![Talk Preparation in a Cafe](/img/first-talk/co-working-talk-prep.jpg#center "Talk Preparation in a Cafe")

While I hadn't done any major presentations in recent years, I picked Google Slides as this was the presentation software I was most familiar with. I picked a slide theme and adjusted it to my _brand colors_:

![Sample Slide](/img/first-talk/sample-slide.png#center "Sample Slide")

It was clear to me that I didn't want to perform any live coding on stage for my first talk. That's why I included all code examples as screenshots.

For the slide design, I tried to balance text-only and graphical slides (including memes) to keep the talk exciting, as I already knew I'd be the second last speaker on the Friday.

For training purposes, I gave the talk a week before the conference to myself and recorded the screen and my camera. This acted both as a trial run as well as a backup plan. Given the unclear COVID situation, I might have received a positive test and not be able to hold the talk. I thought that if I prepared the talk, I could send it to the organizers, and they could at least play the video for the attendees. Fortunately, this backup was not needed at all.

I made this trial run as close as possible to the conference day. I used my standing desk and the presenter to get, as we would say in software development, as close to production as possible. This first run went fantastic, and I was just under time.

The second and final trial was done two days before the conference in a WeWork conference room in Barcelona. As I'm a bit superstitious, I thought that the final talk run had to be my third attempt, aka: all good things are in threes.

## The First Conference Day: Relaxed Networking

As the conference was in Barcelona, I used this event for some pre- and post-vacation that fitted around the conference in Spain 🇪🇸. I spent four days in Valencia before the conference and then drove to Barcelona by bus.

In the evening before the first conference, we had an amazing speaker dinner. There was even a shuttle that brought us to the dinner place. This speaker dinner was a great opportunity to meet the other speakers and connect with people I already knew virtually from Twitter.

![Spring I/O 2022 Speaker Dinner](/img/first-talk/speaker-dinner-selfie.jpg#center "Spring I/O 2022 Speaker Dinner")

We even went for a post-dinner beer on the rooftop bar of our hotel but got to bed around 1 am as most of us had their talk on the first conference day.

As my talk was on the second day, I could enjoy the first day. I went to many great sessions and connected with other speakers and people in the Spring Boot community.

It was a crazy feeling getting to the conference as a speaker. I was _only_ an attendee at all past conferences.

![Spring I/O Conference Venue](/img/first-talk/spring-io-conference-venue.jpg#center "Spring I/O Conference Venue")

I felt really grateful, even feeling a little like a star, especially when I saw myself during the keynote as part of the speaker lineup.

![Spring I/O Conference Speaker Line Up](/img/first-talk/conference-line-up.jpg#center "Spring I/O Conference Speaker Line Up")

The first day ended with beer and networking at the conference venue.

Around 9 pm, there was even a huge fountain animation (Barcelona Magic Fountain of Montjuïc) next to the conference hall:

![Barcelona Magic Fountain of Montjuïc](/img/first-talk/barcelona-fountain.jpg#center "Barcelona Magic Fountain of Montjuïc")

After this show, I even got the chance to have dinner with the organizers and other speakers.

As my talk was happening on the second day, I was hesitant to stay up late and went straight to bed after dinner. This was at around 11 pm as the people in Spain eat quite late compared to my usual German dining hours.

## The Second Conference Day: Giving the Talk

Getting up in the morning on the day of my talk was both joyful and scary. I knew that by the end of the day, I would have stepped out of my comfort zone and held my talk. However, I had to make it through an entire conference day as my talk was the second-last.

Watching other talks this day felt almost like being in school when it was time to hold presentations, and you were the last. You were sitting in the classroom, getting more nervous while more and more of your friends finished their presentations, and yet yours was still to come.

Given this slight mental pressure, I could still enjoy the entire conference day and only got really nervous and tired about one hour before my talk was due to start.

Fortunately, there was a 30-minute coffee break before my talk. Hence, there was no rush between two talks, and I could prepare the setup and get used to the stage and atmosphere. I arrived 20 minutes before the talk started, set up my machine, and connected to the beamer.

![Speaker Setup](/img/first-talk/speaker-setup.jpg#center "Speaker Setup")

While there were already some attendees sitting in the audience, most of them were enjoying their coffee break.

I used this gap time to check some slides on the big projector and made sure to close all applications on my Mac that could disturb the talk.

Ten minutes before the talk started, I got the mobile microphone from the sound team. By then, almost fifty people were in the audience, some of whom I met either during the speaker dinner or the conference.

![Pre-Talk Selfie](/img/first-talk/pre-talk.jpg#center "Pre-Talk Selfie")

Right on time, at 5 pm, the organizers closed the doors, and I started my talk...

First, I greeted the audience and thanked them that they came to my talk on a Friday afternoon at 5 pm while the weather was perfect outside in Barcelona.

After the first 4 to 5 sentences, the initial peak of excitement and nerves faded away, and I started to really enjoy talking on stage.

Fortunately, there were no major technical problems during the talk as I didn't live code and had all code examples stripped down to their minimum and included them as screenshots.

After 48 minutes, I finished my last 'Conclusion & FAQ' slide, and the talk was over.

![Post Talk Selfie](/img/first-talk/post-talk.jpg#center "Post Talk Selfie")

What a feeling!

Unfortunately, the 2 minutes left weren't enough to answer questions as the next speaker was lining up to give his talk in just 12 minutes.

Nevertheless, more than ten attendees came to me right after the talk to ask their questions and to thank me for giving this talk. We went outside the room to avoid any disturbance for the next speaker and discussed their questions with no rush.

I guess it's a good sign if there's interest after your talk, and the attendees even miss the first minutes of the final talks as they want to talk with you.

## Afterthoughts & Tips

Overall, it was one of the best experiences I have had in my professional career so far. The feeling of joy that I had finally worked out of my comfort zone really motivated me to tackle similar milestones from now on.

Timing-wise I could have done a bit better. While my session was planned for 50 minutes, I finished my talk within 48 minutes and hence had no time to answer questions directly from the audience. Nevertheless, I tried to help everyone that came to me after the talk, and we took a standing desk outside to discuss details or specific problems.

After giving the talk, I was both super happy and relaxed. I immediately pondered what talks I could prepare next, particularly as I enjoyed the entire experience of being a speaker at a conference.

In summary, these are the tips and recommendations I can offer as a first timer:

- Do at least one trial run. If you've never presented in front of a bigger audience, use an internal event or a meetup to train your talk and presentation skills
- Get a mentor or buddy to help out with the slide deck and talk preparation (I didn't have one but advise you to do so if you've not done so many other public speaking sessions.
- Record yourself during your trial run(s). I know that it's super awkward if you're doing it for the first time.
- Cut your best trial recording to have a plan B if everything goes south. Imagine a positive COVID test right before the conference. This way, you can at least send the recording to the organizers, and they can play it inside the room.
- Check the hardware on stage during a coffee break a few hours before your talk starts.
- Have fun. You're there to talk about stuff that you care about.
- Don't do live coding during your first talk.
- Have a fallback option for everything: Batteries for your presenter, maybe a second laptop, a USB with the final talk on it, mobile data if the conference WLAN is flaky, etc.
- Use big font sizes - the attendees in the last rows will thank you!
- Don't overuse bullet points, as they can make your audience tired
- Freshen up things with graphics, images, and short summaries
- Upload your slide deck to Speaker Deck afterwards
- Don't use dark themes when screenshotting your code examples (I use the distraction-free mode of IntelliJ IDEA for my screenshots)
- Bring some water and maybe some throat candy to the stage in case your voice starts cracking
- Wear clothes that you feel comfortable in

The final slide deck is [available on Speaker Deck](https://speakerdeck.com/rieckpil/how-fixing-a-broken-window-cut-down-our-build-time-by-50-percent).

Kudos belong to [Sergi Almar](https://twitter.com/sergialmar/) and his entire team for the fantastic organization of this event!

... and finally, here's the recording of the talk:

{{< youtube c-GV2PxymoY >}}

&nbsp;

Let me know how your first public talk experience was in the comments. Also, feel free to provide any valuable feedback on the talk performance 🤓

To many more talks 🚀

Have a good one,
Phil


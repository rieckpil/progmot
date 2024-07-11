---
title: "Making First Place at my Second Hackathon"
description: "Read about how I made first place at my second Hackathon Digital Tech Summit. For Siemens Healthineers we developed a solution to track medical packages"
slug: "/making-first-place-at-my-second-hackathon"
aliases: ["/posts/making-first-place-at-my-second-hackathon"]
author: philip
date: 2018-10-28T11:00:00+02:00
---
From the 19th to 21st of October 2018 the **Hackathon [Digital Tech Summit](https://www.gotechsummit.com/)** took place in **Nuremberg** as part of the[**Digital Festival in Nuremberg**](https://nuernberg.digital/festival/).

With more than **500** **attendees** and **23** **Hackathon** **teams** , it was my second and yet **biggest** **Hackathon** and my team made the **first** **place** .

We developed a solution for **Siemens** **Healthineers** to track their shipments of medical equipment so they are able to recognize possible damage and inform e.g. the receiving hospital and resend the same lifesaving equipment to prevent an outage.

In addition, the technicians were able to locate the shipment within a huge hospital to keep the seek time for the package as low as possible. In this blog post, I'll write about the event and give you insights into our team and how we made the first place.
![](/img/blog-content/review-making-first-place-at-my-second-hackathon-1.png)
Arriving at the event location

The whole event was organized by [Zollhof](https://www.zollhof.de/) a tech incubator in Nuremberg.

The main sponsors of this Hackathon were enterprises from the surrounding area like **Adidas, Schaeffler, Siemens Healthineers, Nürnberger Versicherung** and **Gfk.**

The enterprises provided challenges for the Hackathon in the following six tracks: **Health, Sports, Retail, Security, Mobility \& Wildcard**.

Within every track, there were about up to four concrete challenges.

![](/img/blog-content/review-making-first-place-at-my-second-hackathon-2.png)
The event took place at the Lederer Kulturbrauerei in Nuremberg

The Hackathon started at 6 pm on Friday with a general welcome speech and presentation of the challenges. Every company got five minutes to pitch their challenge to the audience.

After these pitches, the attendees voted by the show of hands in which track they'll probably take part.

Every track then got a dedicated area within the event location to start a more detailed Q\&A with the participants.
![](/img/blog-content/review-making-first-place-at-my-second-hackathon-3.png)
Schaeffler pitching their challenge

My colleague and I were really convinced to take part in the challenge from **Siemens Healthineers** within the health track as they not only had an awesome pitch but they also had a lot of employees as mentors for the two days.

The main problem they addressed with their pitch was the fact that they ship a lot of critical and lifesaving technical equipment and don't know the condition of the package until it arrives at the destination.

Shipping **damaged** **medical** **equipment** to not densely populated areas can lead to an outage of a device in the hospital and in the worst case to the **death of people**. To reduce this risk they were looking for solutions for this problem.

The first idea which came to our minds was a **smart** **device** that is able to collect different **sensor** **data** and perform **actions** (e.g. informing the hospital/Siemens/patients) when a package got damaged or will likely be broken when it arrives. For this idea, we were able to find and convince **six** other **attendees** to join our team **PreTrack** .

Our mission was to **save patients' lives** with a**smart tracking** device for the shipment. Our team consisted of three rather business-related members and five techies.
![](/img/blog-content/review-making-first-place-at-my-second-hackathon-4.png)
After the brainstorming session


At 10 pm on Friday, we were able to start our project and we began with brainstorming to find our concrete use case and discuss everyone's ideas.

We agreed on developing a reusable device for the shipment which is able to send different **sensor** **data** to the **cloud** and **trigger** different **actions** and log every suspicious event during the shipping.
In addition, our device should be able to locate the package within a huge hospital to find it more easily as the packages often arrive at night and the shift and the technician in the next morning don't know where the required equipment is.


With this use case in mind, we split our tasks and our business started to figure out a possible business plan and gather more information about the logistics from Siemens employees. For the technical side, we had four major tasks:

- providing a **backend**
- writing a **user** **interface** for our prototype
- **retrieve** and **send** **sensor** data from the device to the backend
- **detecting** **damage** from the sensor data.

I took part in writing the backend service and managing our infrastructure.

![](/img/blog-content/review-making-first-place-at-my-second-hackathon-5.png)

For the hardware device, we picked a [Pycom](https://pycom.io/) as these were provided during the Hackathon. In addition, we got access to **AWS** from Siemens and I created an EC2 instance for our backend and the webserver.

Furthermore, I ordered a managed **PostgreSQL** within **AWS** to store our sensor data and the events. For managing our codebase we used a private repository on **GitLab** .

With the **Pycom** the programming language to access the sensor data was set to **Python** , for the backend I picked **Java** and **Spring Boot** , and for the frontend we chose **Angular**. After setting up the main infrastructure for our prototype and granting access to all our developers we all went home at 1 am.

The next day started at 8:30 AM with a **short** **meeting** with some Siemens employees to present our idea and get the first **feedback** . Until the afternoon we were able to send the first sensor data to our backend, store the data in our database.

After the lunch, on Saturday we created a simple **mockup** for our **prototype** and while brainstorming for a mobile-friendly dashboard we got the idea to display a live view of the **current** **alignment** of the package.
In the evening our prototype was able to **stream** the **current** **sensor** **data** to our frontend and with [three.js](https://threejs.org) we were able to visualize the alignment of the package with a small delay.

Our business also gathered enough information during the whole day to start creating our slides for the pitch for the next day. This day ended at 12 pm as we were all really tired.

![](/img/blog-content/review-making-first-place-at-my-second-hackathon-6.png)

Sunday morning we integrated the business logic for detecting possible damage and in case of a **drop** /**damage** or **shaking** we sent **events** to our frontend application. As the semi-finals were announced for 4 pm we agreed on a code freeze at 3 pm to have enough time to practice our pitch.

For our pitch, we attached our **Pycom** to a sample package to show the functionality live.
![](/img/blog-content/review-making-first-place-at-my-second-hackathon-7.png)
Team PreTrack after the semi-final

For the semi-finals, we pitched against three competitors in the health track which also took part in the challenge from Siemens. For our **three** **minute** **pitch** , we prepared a slide deck to explain our solution and used the **two** **minutes** for **Q\&A** after the pitch to demonstrate the prototype in front of the jury. After a short discussion, we got the information from our mentors that we passed the semi-finals and are now part of the finals at 6 pm.
![](/img/blog-content/review-making-first-place-at-my-second-hackathon-8.png)

We also got valuable feedback for our semi-final pitch as we focussed too much on the business side of our prototype and should have integrated our running solution within the three minute pitch time to prove the **technical** **impressiveness** of our **prototype**.

With this feedback, we restructured our slide deck and focussed more on the technical solution with a live demo right at the start of the pitch.

![](/img/blog-content/review-making-first-place-at-my-second-hackathon-9.png)
For our final pitch, we provided three smartphones and a laptop for the jury to prove that we are not simulating anything and they could see the alignment and the events live during the pitch.

Our final pitch consisted of a **short** **introduction** to the **problem** , a **live** **demo** for dropping/damaging and shaking the shipment, a **technical** **overview** of our used technologies and an **outlook** for **possible** **post-shipping use cases** with the data we collect.

![](/img/blog-content/review-making-first-place-at-my-second-hackathon-10.png) The final pitch
After dinner, the five winning teams were announced and we were overwhelmed when the **CEO** of **Zollhof** **Benjamin** declared **PreTrack** as the winning team.

![](/img/blog-content/review-making-first-place-at-my-second-hackathon-11.png)

Thanks a lot to Zollhof for organizing this awesome event and Siemens Healthineers for providing the challenge and the support.

See you at the next Hackathon,\
Phil


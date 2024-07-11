---
title: "My First Hackathon - HACK|BAY by ZOLLHOF"
description: "Read about my first Hackathon: HACK|BAY 2018 in Nuremberg hosted by ZOLLHOF with a InsurTech solution for vehicle registration documents"
slug: "/my-first-hackathon"
aliases: ["/posts/my-first-hackathon"]
author: philip
date: 2018-07-15T12:51:26+00:00
---
From July 10th to the 11th I took part in the Hackathon [HACK\|BAY](https://www.hackbay.de/) which was organized by the tech incubator [Zollhof](https://www.zollhof.de/) in Nuernberg. Even if I participated in several coding challenges and a company internal Hackathon, this was my first Hackathon with a jury and multiple competing teams.

The event was sponsored by several local companies and they presented challenges in the following topics: **Connected City** , **Machine Learning** , and **Industrial IoT.**


Every challenge got five minutes for presentation and afterward, we could form teams in free ideation. At first, I was really interested in the Industrial IoT challenge from **Siemens** where we could use their **Mindsphere** cloud environment to hack something for the production manager in the future.

While we were talking to the presenter of the challenge my colleague and I couldn't come up with a really innovative idea for this challenge.

Fortunately, a team from another challenge came to us and asked if there are some techies who don't have a team yet. We followed them and they presented their current team and their idea. The challenge was from the insurance company **HUK-Coburg** in the **Machine Learning** topic.

The challenge was about **"Scan and compare your insurance documents!"** and they had already two business guys who were looking for techies for their team. The main idea was to use the vehicle registration document and use Machine Learning to speed up the time for a new insurance contract.

We liked the idea but my colleague and I both had not that deep knowledge in image recognition and OCR with Java but we decided on this challenge as we could learn a lot of new things.

After the ideation phase, our final team consisted of six people (three business, three techies) and our team was called**Smart Insurance.**

Together with our business teammates, we brainstormed about the desired outcome for the next **24 hours** of hacking. Our business model was to provide an interface for insurance companies to upload the vehicle registration document for a potential new customer.

As a response, we would return all the required information for a new car insurance contract so that they can speed up the contract conclusion. We would be paid by every**API call** of the insurance company and provide a trained **AI algorithm** to collect the data from the uploaded images.

For the Hackathon, we wanted to hack a prototype for the **HUK-Coburg** with a small web application to show the benefits with a real prototype.

As the German vehicle registration document has a defined structure we thought it would be easy to scan an image of it and to retrieve the data. But after some hours of trial and error with **Tesseract** for OCR and some image optimations we weren't that happy with the result.

Fortunately, we found the **Google Vision API** and got quite better results with this OCR. Our "Machine Learning" algorithm just needed to retrieve the important data from the Google Vision API call.

For future development we would use a self-trained algorithm to do the OCR but in the short period of time, we just used Google.

![My first Hackathon hacking area](/img/blog-content/review-my-first-hackathon-1.png#center)

With some tricks, we were able to get the **address** of the customer, the **vehicle manufacturer** and the **vehicle type** out of the registration document.

We used this data to call an API of the insurance company to calculate the insurance costs for exactly this car. As there are up to fifty parameters for an insurance contract we used a persona at age of 25 with about six years of driving experience to prefill some parameters for the API.

Our technical architecture looked like the following (the Machine Learning algorithm was the Google Vision API plus some backend code for the showcase):

![My first Hackathon system architecture](/img/blog-content/review-my-first-hackathon-2.png#center)

After about 20 hours of hacking (including some sleep) our prototype was ready and we were able to get correct results in about **40%** of the time if the vehicle document was printed correctly with no handwritten changes on it.

For the frontend technology we used **Angular 6** and our backend was a **Spring Boot** application which I hosted on my server so that everybody could try the progressive web application on their smartphone:

![](/img/blog-content/review-my-first-hackathon-3.png#center)

![](/img/blog-content/review-my-first-hackathon-4.png#center)

While we were hacking our business started to prepare our three-minute pitch in front of the jury. To make it to the finals we had to be a least second place in the semi-finals.

Not all the twelve teams were pitching their ideas in a row. All three topics (**Connected City** , **Machine Learning** and **Industrial IoT**) had their semi-finals where the teams in this track competed against each other.

Fortunately, in our track we just had two competitors and made it through the semi-final.

![My first Hackathon semi final pitch](/img/blog-content/review-my-first-hackathon-5.png#center)

For the final pitch, we had four competitors and got a new jury with executives from the sponsoring companies. Our idea and the web application convinced the jury and we got**third place**.

The winning team came up with a smart power socket solution and the second place was a plug-and-play Raspberry Pi network security solution for mid-sized companies.


![My first Hackathon Winner picture](/img/blog-content/review-my-first-hackathon-6.png#center)

The time spent hacking and our team was really nice. At first, we were quite doubtful if we can provide a solid solution for our challenge as we didn't have any deeper knowledge of this topic, but we were amazed by our prototype and the result.

I can recommend everyone to visit such events not only to win some prizes but to network and get together with awesome people. I'll definitely participate again next year!

Happy hacking,

Phil


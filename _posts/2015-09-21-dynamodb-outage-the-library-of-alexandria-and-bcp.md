---
title: DynamoDB Outage, The Library of Alexandria and BCP
tags: [Enterprise Architecture]
category: [Featured]
origianl_link: https://www.fourhundredwords.com/post/129532247596/dynamodb-outage-the-library-of-alexandria-and-bcp
image: /assets/images/posts/Ancientlibraryalex.jpg
image_attribution: Photo by <a title="O. Von Corven / Public domain" href="https://commons.wikimedia.org/wiki/File:Ancientlibraryalex.jpg"><img width="512" alt="Ancientlibraryalex" src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/64/Ancientlibraryalex.jpg/512px-Ancientlibraryalex.jpg"></a>O. Von Corven</a>
---
[The Library of Alexandria](https://en.wikipedia.org/wiki/Library_of_Alexandria) was one of the largest and most significant libraries of the ancient world until its destruction in 48BC (or maybe AD 270 – 275, AD 391 or AD 642).
<!-- readmore -->
However what is often missed in the accounts of its destruction is that the daughter library in the [Serapeum temple](https://en.wikipedia.org/wiki/Serapeum#Alexandria)was used in its absence. Our historic enterprise architecture colleagues were thinking about Business Continuity Processes (BCP) even back then!

Over the weekend the [AWS DynamoDB](https://aws.amazon.com/dynamodb) (Database-as-a-Service) was down for around 6 hours. Much of our modern day ‘knowledge’ was unavailable, many millions of dollars where lost (it’s estimated AWS lost about $1,000/second), and organisations reputation’s where damaged as the internet &nbsp;took to Twitter and other such services to complain about the lack of on-demand video in that time.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">This is what I assume <a href="https://twitter.com/hashtag/AWS?src=hash&amp;ref_src=twsrc%5Etfw">#AWS</a> <a href="https://twitter.com/hashtag/AWSOutage?src=hash&amp;ref_src=twsrc%5Etfw">#AWSOutage</a> looks like right now.. <a href="http://t.co/jdZVP1p6Rc">pic.twitter.com/jdZVP1p6Rc</a></p>&mdash; Jess 🤓 (@putapixelonit) <a href="https://twitter.com/putapixelonit/status/645609003976933376?ref_src=twsrc%5Etfw">September 20, 2015</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

What is clear from this outage is that many of these high profile organisations had no visible BCP process for when a cornerstone of their service was unavailable (in fairness their BCP may have been to just ride out the issue).

As an Enterprise Architect considering People, Processes and Technology is one of the key considerations when evaluating solutions for our enterprises and continuity is always evaluated as part of this process. With our services becoming ever more tightly coupled (Databases on Clusters, supported by virtualisation and storage arrays) a minor uncontrolled change in one area can have knock on impacts across the organisation. Working in a 24/7 environment our BCP processes are therefore key for when technology fails.

In the case of the AWS DynamoDB outage AWS provide the service in multiple locations so organisations have the opportunity to take advantage of failover processes/etc. as part of their BCP however without the proper architecture built into their applications it is clear that organisations were unable to take advantage of this.

Working in an industrial environment BCP is a key part of the way of working considering the impacts that it can have to safety of employees. Hopefully the loss of Netflix/etc. is not so critical, however with the increase of home automation, IoT and connected living it’s not such a stretch to see where this could start to impact safety – somebody in danger needing to get into their house, but not being able to when their phone won’t connect to unlock their front door.

BCP is something we need to consider is all systems. What are your thoughts?
---
title: "ResearchKit Fork"
date: 2023-04-09T13:50:46-04:00
featured: true
description: "A custom version of Apple's ResearchKit framework I built for Peer2Power. It strips down ResearchKit to only use its surveys."
image: ""
link: "https://github.com/jacksodl23/ResearchKit-minus-HealthKit"
fact: "Interesting little tidbit shown below image on summary and detail page"
weight: 500
sitemap:
  priority : 0.8
---

I made this fork while developing Peer2Power because I wanted to use the native and well-designed surveys provided by Apple's [ResearchKit framework](https://github.com/ResearchKit/ResearchKit). I ran into issues because ResearchKit was originally created to support medical research. However, the study I was building Peer2Power for did not need any medical information. Even though I was not using any features that accessed medical information, the framework still referenced code that did. This became an issue when I submitted the app to Apple for distribution on the App Store. Apple's App Review rejected my app due to the presence of code that accessed medical information. Having any code that does so present requires that you ask permission to access medical information.

Thus, to get approved by Apple Review, I had to go in and remove references to any code that accessed medical information. Fortunately, I didn't have to start from scratch as [a fork that removed all references to HealthKit](https://github.com/matyasbohacek/ResearchKit-without-HealthKit) already existed. However, there were additional privacy features such as accessing the camera, microphone, and speech recognition that I did not use but were still referenced. I had to remove these references as well. The result was a version of the framework specifically tailored for the Peer2Power app and one that could pass through the App Review process.
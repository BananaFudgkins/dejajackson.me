---
title: "Peer2Power"
date: 2023-04-02T19:23:46-04:00
featured: true
description: "An iOS app I wrote in SwiftUI for an undergraduate research project."
image: "/Peer2Power logo.png"
link: "https://apps.apple.com/us/app/peer2power/id1596147066"
weight: 500
sitemap:
  priority : 0.8
---

The Peer2Power app arose out of a need to develop a digital solution that could meet the needs of the [undergraduate research group](https://sites.lafayette.edu/clarkeaj/gov-lab/) I was part of. The study I participated on was meant to assess the effectiveness of friend-to-friend recruitment of volunteers for political campaigns. Extant literature examined the effect of social pressure on voter turnout but not volunteer recruitment. We modelled our study on a group called Empower, which used an app to collect contact information and for participants to complete tasks relevant to the study. However, Empower's study focused on voter turnout. After surveying civic involvement apps already on the market, we were unable to find one that fit our exact needs. Thus, I developed a custom app that focused on volunteer recruitment, supported random assignment into control and treatment groups, and provided digital surveys we could use to collect relevant data.

## ResearchKit

![Who emailed an elected representative survey question](/survey_first_q.png) ![Future recruitment likelihood survey question](/survey_second_q.png) ![End of study survey completed](/survey_completion.png)

The app uses Apple's [ResearchKit framework](https://github.com/jacksodl23/ResearchKit-minus-HealthKit) to present its digital surveys. Digital surveys allow for the instantaneous collection of data.
---
title: "Peer2Power"
date: 2023-04-02T19:23:46-04:00
featured: true
description: "An iOS app I wrote in SwiftUI for an undergraduate research project."
tags: ["SwiftUI","Swift","Xcode","MongoDB","iOS"]
image: "/Peer2Power logo.png"
link: "https://apps.apple.com/us/app/peer2power/id1596147066"
weight: 500
sitemap:
  priority : 0.8
---

The Peer2Power app arose out of a need to develop a digital solution that could meet the needs of the [undergraduate research group](https://sites.lafayette.edu/clarkeaj/gov-lab/) I was part of. The study I participated on was meant to assess the effectiveness of friend-to-friend recruitment of volunteers for political campaigns. Extant literature examined the effect of social pressure on voter turnout but not volunteer recruitment. We modelled our study on a group called Empower, which used an app to collect contact information and for participants to complete tasks relevant to the study. However, Empower's study focused on voter turnout. After surveying civic involvement apps already on the market, we were unable to find one that fit our exact needs. Thus, I developed a custom app that focused on volunteer recruitment, supported random assignment into control and treatment groups, and provided digital surveys we could use to collect relevant data.

## ResearchKit

<img src="/peer2power_screenshots/survey/survey_first_q.png" alt="Who emailed an elected representative survey question" width="25%" height="75%"> <img src="/peer2power_screenshots/survey/survey_second_q.png" alt="Future recruitment likelihood survey question" width="25%" height="75%"> <img src="/peer2power_screenshots/survey/survey_completion.png" alt="End of study survey completed" width="25%" height="75%">

The app uses Apple's [ResearchKit framework](https://github.com/jacksodl23/ResearchKit-minus-HealthKit) to present its digital surveys. Digital surveys allow for the instantaneous collection of data.

## Custom Built for Our Study

I initially joined this research team as a research assistant. However, my role quickly changed when a need arose for an in-house solution for an app to carry out our field study after we were unable to find an existing app that aligned with our experimental design. I knew that I could use my iOS development skillset to contribute to the team in a unique way. I personally offered to build the app we needed. Our study measures the effectiveness of friend-to-friend recruitment using a randomized control trial.

### Contacts List

<img src="/peer2power_screenshots/contacts_list.png" alt="Contacts list" width="25%" height="75%">  Similar to the [Turnout Nation study,](https://empowerproject.us/turnout-nation-digs-into-local-elections-and-creates-lifetime-voters-using-friend-to-friend-voter-mobilization/) participants upload a list of contacts who they think are interested in civic engagement. 

In our first run of the study, these contacts would be recruited to volunteer for a political campaign. In its current rendition, these contacts should be interested in emailing an elected representative. Once a contact is uploaded, it is randomly assigned to the control or treatment group. Contacts in the treatment group should be contacted to get them to email an elected representative while those in the control group should not be contacted. The app uses a random number generator to determine which group a contact will belong to.

After generating a list of contacts, participants will log each attempt they made to get a contact to email an elected representative. Every time a participant wants to log an outreach attempt, they will have to answer a survey question asking whether the contact committed to emailing an elected representative. 

The units in our study are student organizations on an undergraduate campus. Participants pick a club to serve as their "team" in a campus-wide competition with other clubs. Uploading a contact or logging an outreach attempt will award a participant's team a number of points. The team with the highest number of points will win the competition.

Once the competition is over, participants will be asked to complete an end-of-study survey indicating which contacts emailed an elected representative.

## Backend

Peer2Power uses MongoDB as its backend. Atlas App Services is used for authentication and to sync data on a user's device with the cloud. The app's data is stored on MongoDB Atlas.
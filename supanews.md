---
layout: default
title: SupaNEWS - Zero-to-One Product Development
---

[← Back to Home](./)

# 📌 Case Study: SupaNEWS - Zero-to-One Product Development

**Role:** Founder, Designer, & Full-Stack Developer  
**Tech Stack:** Flutter, Supabase, PostgreSQL, OpenAI API, Cloud Functions

---

## 1. The Vision
News consumption in Australia is fragmented across dozens of publisher apps, and readers are often overwhelmed by clickbait and bias. I identified an opportunity to use **Generative AI** to improve the signal-to-noise ratio.

**The Goal:** Build a "Zero-to-One" mobile product that aggregates news and uses AI to deliver unbiased, concise summaries.

## 2. Technical Architecture
As the sole developer, I architected a scalable, serverless solution to handle heavy data lifting without managing infrastructure.

* **Frontend (Flutter):** Built a responsive, cross-platform mobile app (iOS/Android) ensuring a native 60fps experience.
* **Backend (Supabase):** Leveraged Supabase for:
    * **Database:** PostgreSQL for storing user preferences and news metadata.
    * **Auth:** Secure authentication flows (Email, Social Login).
    * **Edge Functions:** Serverless Typescript functions to fetch and parse RSS feeds from major Australian publishers.
* **AI Integration:** Implemented an automated pipeline where incoming news articles are processed by LLMs (Large Language Models) to generate 3-bullet summaries and sentiment analysis tags.

## 3. Product Features
* **Personalized Feed:** An algorithm that learns from user interactions to surface relevant stories.
* **AI Summaries:** "Click-saving" summaries that allow users to understand the core story without visiting ad-heavy publisher sites.
* **Push Notifications:** Real-time alerts for breaking news events, managed via Cloud Messaging.

## 4. Outcome & Learning
* **Market Launch:** Successfully published the app to the Google Play Store.
* **Engineering Mastery:** This project honed my ability to speak the language of engineering. By building the entire stack myself—from database schema design to state management in Flutter—I can now collaborate more effectively with engineering teams on complex enterprise products.

---
[← Back to Home](./)

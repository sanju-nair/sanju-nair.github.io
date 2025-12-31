---
layout: default
title: SupaNEWS - Zero-to-One Product Development
---

[← Back to Home](./)

# 📌 SupaNEWS - Zero-to-One Product Development

**Role:** Founder & Technical Product Manager
**Tech Stack:** Flutter, Supabase, PostgreSQL, Edge Functions
**Tools:** ChatGPT, Gemini, Claude (AI-Assisted Engineering)

---

## 1. The Vision: Solving the "Clutter" Problem
News consumption in Australia is fragmented. To get a complete picture of the day's events, a user typically has to visit multiple publisher websites or apps.
* **The Friction:** Most free news apps are essentially "Ad Delivery Vehicles." They are cluttered with pop-ups, autoplay videos, and intrusive tracking.
* **The Goal:** I wanted to build a **"Signal-only"** news aggregator. A fast, clean, mobile-first experience that centralized top Australian news sources into a single feed, respecting the user's time.

## 2. Technical Architecture
Leveraging my background as a former **Full-Stack Engineer**, I architected a low-maintenance, scalable solution. I chose a "Serverless" approach to minimize DevOps overhead while ensuring high availability.

* **Frontend (Flutter):** I chose Flutter to build a single codebase that deploys natively to both iOS and Android, ensuring a smooth, 60fps scrolling experience.
* **Backend (Supabase):** I leveraged Supabase (an open-source Firebase alternative) to handle the heavy lifting:
    * **Database:** PostgreSQL to store user preferences and bookmarked articles.
    * **Authentication:** Secure email and social login flows.
    * **Edge Functions:** TypeScript functions to poll and parse RSS feeds from major Australian providers (ABC, SMH, etc.), normalizing the data into a unified schema.

## 3. The Workflow: AI-Augmented Engineering
I built this app to demonstrate the future of rapid product development. I utilized LLMs (ChatGPT, Gemini, and Claude) not just for snippets, but as a full-time **"Pair Programmer."**

* **Architect vs. Builder:** This was not "vibe coding" (blindly prompting). I acted as the **System Architect**, defining the data schema, state management strategy (Riverpod), and API contracts. I then directed the AI agents to write the implementation code, write unit tests, and refactor for performance.
* **Velocity Multiplier:** Using AI for boilerplate generation and complex debugging (e.g., solving async race conditions in Flutter) allowed me to move from **Idea to Play Store release** at 3x the speed of a traditional solo developer.
* **Tech Stack Fluidity:** Although my core background is Java, I used AI assistance to effectively write production-grade **Dart (Flutter)** and **TypeScript (Edge Functions)**, proving that a strong Technical PM can now build across the full stack regardless of their native language.

## 4. Product Iteration: Solving Retention
The initial launch taught me a critical lesson in user retention.
* **The Problem (High Churn):** Early telemetry showed a high bounce rate. Users were clicking headlines but abandoning the app immediately when redirected to slow, ad-heavy publisher websites via the in-app browser.
* **The Fix:** I developed a native **"In-App Reader"** mode. This feature parses article content into a clean, text-only view, stripping away ads and tracking scripts to load content instantly.
* **The Result:** This dramatically improved session duration and addressed the churn, proving that the "Reading Experience" (speed and cleanliness) was the core value driver for my users.

## 5. Outcome & Learning
* **Market Launch:** The app is successfully live on the **Google Play Store**, serving real users.
* **Engineering Empathy:** Building `SupaNEWS` reinforced my ability to speak the language of engineering. By wrestling with State Management, API Rate Limiting, and Release Management personally, I can collaborate more effectively with engineering leads on complex enterprise products.

---
[← Back to Home](./)

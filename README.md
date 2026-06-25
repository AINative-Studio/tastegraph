# TasteGraph

## AI-Native Personal Experience Memory & Recommendation Agent

> **"Your personal AI concierge that remembers every great experience you've ever had."**

---

# Overview

TasteGraph is an AI-native application built on the **AINative Studio platform** that automatically captures, organizes, understands, and recommends the real-world experiences of its users.

Unlike Yelp, Google Maps, TripAdvisor, or public review platforms, TasteGraph builds a **private lifelong memory** of a user's own experiences.

Over time, the system develops a semantic understanding of the user's tastes, preferences, relationships, favorite cities, favorite restaurants, favorite events, and favorite experiences.

The result is an AI agent capable of acting like a trusted friend who has perfect memory.

---

# Product Vision

Imagine asking:

> "Where should my parents eat in Austin?"

Instead of searching Google, the AI searches years of your own memories and responds:

> Based on your experiences, your parents would probably love these five restaurants. They all have quiet atmospheres, excellent seafood, outdoor seating, and you've rated each at least 4 stars.

The recommendations come from **your own life**, not anonymous internet reviews.

---

# Core Philosophy

TasteGraph is built around one principle:

> **Your own experiences are more valuable than everyone else's reviews.**

Rather than collecting public ratings, TasteGraph builds a living knowledge graph of everything you've personally experienced.

Every restaurant...

Every concert...

Every vacation...

Every coffee shop...

Every park...

Every hotel...

becomes part of your personal intelligence.

---

# Primary Goals

The platform should:

* Automatically remember experiences
* Require almost zero manual effort
* Continuously learn preferences
* Build lifelong memory
* Generate personalized recommendations
* Recommend only experiences the user genuinely loved
* Become smarter over time

---

# Technology Stack

This project should leverage existing AINative services wherever possible to minimize custom application code.

## Agent Cloud

Primary orchestration layer.

Responsibilities:

* Long-running agents
* Background jobs
* Event processing
* Scheduled workflows
* Multi-agent coordination

---

## ZeroDB

Primary datastore.

Use ZeroDB for:

* Structured tables
* Vector storage
* Semantic search
* Metadata
* Event storage

---

## ZeroMemory

Persistent AI memory.

Stores:

* User preferences
* Long-term facts
* Conversation memory
* Learned taste
* Friend preferences

---

## Models API

Responsible for:

* Classification
* Summarization
* Embeddings
* Extraction
* Recommendation reasoning
* Semantic tagging

---

## Knowledge Graph

Stores relationships between:

User

↓

Experiences

↓

Cities

↓

Venues

↓

People

↓

Preferences

↓

Recommendations

↓

Ratings

---

## AIKit

Frontend components.

Reuse wherever possible.

Examples:

* AI Chat
* Timeline
* Cards
* Voice UI
* Maps
* Search
* Recommendation Lists

---

## Lakehouse

Used for analytics.

Examples:

* Favorite cities
* Favorite cuisine
* Recommendation quality
* Preference evolution
* Travel history
* Long-term insights

---

# Product Workflow

```
User visits location

↓

Agent Cloud detects visit

↓

Experience Agent creates experience

↓

Models API extracts metadata

↓

ZeroDB stores structured data

↓

ZeroMemory updates long-term memory

↓

Knowledge Graph updates relationships

↓

User rates experience

↓

Taste Agent updates embeddings

↓

Future recommendations improve
```

---

# Major AI Agents

## 1. Experience Agent

Responsibilities

* Detect experiences
* Merge duplicate signals
* Create Experience records

Inputs

* Calendar
* GPS
* Photos
* Gmail
* Reservations
* Travel confirmations

Outputs

Experience objects

---

## 2. Memory Agent

Responsibilities

Generate structured memories.

Outputs

* Summary
* Metadata
* Embeddings
* Highlights
* Complaints

---

## 3. Rating Agent

Responsibilities

Collect lightweight feedback.

Target completion:

Under 30 seconds.

Captures:

* Overall Rating
* Food
* Service
* Atmosphere
* Value
* Return Intent

---

## 4. Taste Agent

Responsibilities

Learn preferences.

Examples

User likes:

* Outdoor seating
* Craft cocktails
* Quiet restaurants
* Walkable neighborhoods

User dislikes:

* Loud music
* Tourist traps
* Poor service

These become weighted preferences.

---

## 5. Recommendation Agent

Answers questions like:

Where should I eat?

Best tacos I've ever had?

Weekend in Portland?

Best date night?

Kid friendly?

Business dinner?

Parents visiting?

Uses:

* Ratings
* Embeddings
* Preferences
* Context
* Knowledge Graph

---

## 6. Friend Agent

Stores recurring profiles.

Examples

Mom

Seafood

Gardens

Quiet

Dad

Steak

Museums

Sarah

Vegan

Coffee

Children

Parks

Ice cream

Interactive museums

Recommendations become personalized.

---

# Core Domain Objects

The application revolves around these primary entities:

```
User

Experience

Venue

City

Rating

Preference

Person

Recommendation

Recommendation Feedback

Knowledge Graph Edge

Embedding

Memory

Share Session
```

---

# Recommendation Philosophy

By default, recommendations should **never** include mediocre experiences.

Default filter:

```
Overall Rating >= 4
```

Only if explicitly requested should the AI recommend lower-rated places.

Recommendation ranking should prioritize:

1. Rating
2. Semantic similarity
3. User preferences
4. Companion preferences
5. Occasion
6. Recency
7. Confidence score

---

# Experience Lifecycle

```
Experience detected

↓

Metadata extracted

↓

Experience summarized

↓

Stored

↓

Embedded

↓

Knowledge Graph updated

↓

User rates experience

↓

Preferences updated

↓

Recommendation engine updated
```

---

# Search Examples

Natural language search should work everywhere.

Examples

```
Best tacos I've ever had.

Favorite coffee in Seattle.

Restaurants my wife loved.

Every five-star restaurant in New York.

Quiet dinner with outdoor seating.

Family-friendly places in Austin.

Concerts from 2025.

Best date nights.
```

---

# Friend Recommendation Examples

Example:

```
Parents visiting Chicago.
```

Agent asks:

Budget?

Walking?

Kids?

Cuisine?

Then returns:

* 5 restaurants
* Coffee
* Walk
* Dessert
* Museums

using only experiences the user rated highly.

---

# Rating Philosophy

Simple.

Fast.

Private.

Ratings

⭐ 1

Never again.

⭐⭐ 2

Below average.

⭐⭐⭐ 3

Good.

⭐⭐⭐⭐ 4

Recommend.

⭐⭐⭐⭐⭐ 5

Exceptional.

The rating system is not intended to compete with public reviews.

It exists to strengthen future recommendations.

---

# Knowledge Graph

Relationships include

```
User

VISITED

Venue

Experience

IN_CITY

City

User

LIKES

Attribute

User

DISLIKES

Attribute

Experience

WITH

Person

Recommendation

FOR

Person

Venue

TAGGED_AS

Cuisine

Venue

TAGGED_AS

Atmosphere
```

---

# MVP Scope

Version 1 should include:

✅ Authentication

✅ User onboarding

✅ Experience detection

✅ AI summaries

✅ Timeline

✅ Ratings

✅ Recommendation engine

✅ Taste learning

✅ Friend profiles

✅ City pages

✅ AI chat

✅ Share recommendations

Everything else should be deferred until after MVP.

---

# Future Roadmap

* Apple Watch integration
* Oura integration
* WHOOP integration
* Camera vision
* Receipt OCR
* Menu recognition
* Trip planner
* AI travel guide
* Collaborative recommendations
* Taste similarity
* Public recommendation publishing
* Voice-first interaction
* Offline mode

---

# Engineering Principles

* Build on existing AINative APIs before writing custom code.
* Treat every feature as an Agent Cloud workflow where possible.
* Use ZeroDB as the single source of truth for structured and vector data.
* Store durable user preferences in ZeroMemory and expose them through semantic retrieval.
* Model relationships in the Knowledge Graph instead of duplicating data.
* Favor event-driven workflows over synchronous processing.
* Design agents to be idempotent and composable.
* Keep AI prompts versioned and configurable.
* Every experience should improve future recommendations.

---

# Definition of Done

A feature is considered complete when:

* It is orchestrated through Agent Cloud where appropriate.
* Data is persisted in ZeroDB using the agreed schema.
* Relevant memories are written to ZeroMemory.
* Knowledge Graph relationships are updated.
* Embeddings are generated for semantic search.
* AI reasoning uses structured data before free-text prompts.
* The frontend uses AIKit components whenever available.
* Events are emitted for analytics and Lakehouse ingestion.
* Tests cover business logic and agent workflows.
* Documentation is updated.

---

# Mission Statement

TasteGraph transforms a lifetime of experiences into a living, continuously learning AI memory. Every meal, trip, concert, hike, hotel, and conversation enriches a personal knowledge graph that becomes more valuable with time. By combining explicit ratings, semantic memory, vector search, and autonomous agents, TasteGraph evolves into a trusted personal concierge capable of delivering recommendations that feel less like search results and more like advice from your future self.

# Product Requirements Document (PRD)

# TasteGraph

### AI-Native Personal Experience Memory & Recommendation Agent

**Version:** 1.0
**Platform:** AINative Studio
**Primary Services:** Agent Cloud, ZeroDB, ZeroMemory, Models API, AIKit, Knowledge Graph, Lakehouse

---

# Vision

TasteGraph is an AI-native personal intelligence agent that automatically remembers the places you've been, the experiences you've had, and why they were meaningful.

Rather than relying on public reviews, TasteGraph builds a private, lifelong memory of your own experiences. Over time it develops a deep understanding of your preferences, allowing it to recommend restaurants, attractions, events, concerts, hotels, parks, neighborhoods, and entire itineraries that match your personal taste.

When friends or family ask for recommendations in cities you've visited, the agent instantly generates curated suggestions tailored specifically to their interests, using only the experiences you've personally rated highly.

The goal is to become your personal Michelin Guide for every city you've ever explored.

---

# Problem Statement

People spend years discovering amazing places, yet almost all of that knowledge disappears.

Common problems include:

* Forgetting favorite restaurants
* Forgetting hidden gems while traveling
* Mixing together experiences from multiple trips
* Having no easy way to recommend places to others
* Re-searching places they've already visited
* Depending on Yelp or Google instead of their own experience

Current review platforms optimize for the crowd.

TasteGraph optimizes for **you.**

---

# Goals

* Automatically remember experiences with minimal user effort
* Build a lifelong understanding of user preferences
* Learn context rather than simply collecting ratings
* Generate highly personalized recommendations
* Recommend only the user's favorite experiences by default
* Build using existing AINative services with minimal custom code

---

# Core Experience

User visits a restaurant.

↓

Agent detects the visit.

↓

After leaving:

> "How was dinner?"

User responds:

> "Amazing tacos. Great cocktails. Music was a little loud."

↓

The agent extracts structured information, stores the experience, generates embeddings, updates the knowledge graph, and asks the user for one simple overall rating.

That experience becomes part of the user's permanent Taste Graph.

---

# Design Principles

* AI-first
* Zero friction
* Passive whenever possible
* Private by default
* Memory-centric
* Context-aware
* Minimal handwritten code
* Built entirely on AINative infrastructure

---

# Experience Categories

* Restaurants
* Coffee Shops
* Bars
* Breweries
* Food Trucks
* Wine Tastings
* Concerts
* Festivals
* Sporting Events
* Museums
* Parks
* Hiking Trails
* Hotels
* Airbnbs
* Shopping
* Neighborhoods
* Attractions
* Comedy Clubs
* Beaches
* Entire Trips

---

# Functional Requirements

---

## FR1 — Automatic Experience Detection

The agent automatically detects experiences through:

* Calendar
* Google Maps Timeline
* Apple Location History
* Photos
* Reservation emails
* OpenTable
* Airbnb
* Uber
* Lyft
* Flight confirmations
* Eventbrite
* Ticketmaster
* Manual check-ins
* Voice commands

Agent Cloud orchestrates these integrations using existing AINative connectors.

---

## FR2 — Smart Follow-up

After leaving a location, the agent asks only a single follow-up question.

Examples:

* Would you go back?
* Best thing you ordered?
* Would your parents enjoy this?
* Good for kids?
* Date night or business dinner?

Voice and chat are both supported.

---

## FR3 — AI Memory Extraction

The Models API automatically extracts:

* Venue
* Cuisine
* Occasion
* Atmosphere
* Food Quality
* Service
* Price
* Wait Time
* Noise Level
* Parking
* Accessibility
* Family Friendly
* Dog Friendly
* Reservation Needed
* Highlights
* Complaints
* Summary
* Overall Sentiment
* Recommendation Confidence

Everything is stored automatically.

---

# ⭐ FR4 — Personal Rating System (NEW)

Every experience includes a simple overall rating from **1–5 stars**.

The rating is intentionally lightweight so users can complete it in seconds.

### Rating Scale

⭐ **1 Star**
Never recommend again.

⭐⭐ **2 Stars**
Below average. Not worth returning.

⭐⭐⭐ **3 Stars**
Good, but nothing special.

⭐⭐⭐⭐ **4 Stars**
Highly recommended.

⭐⭐⭐⭐⭐ **5 Stars**
Exceptional. Must recommend.

---

## Why Ratings Matter

Unlike public review platforms, these ratings are entirely private and are optimized for future recall and recommendation quality.

Ratings become one of the strongest signals inside the Taste Graph.

They are used for:

* Personal search
* Recommendation ranking
* Friend recommendations
* Trip planning
* AI reasoning
* Confidence scoring

---

## Smart Defaults

When users ask:

> "Where should my parents eat in San Diego?"

TasteGraph automatically filters to:

**4 and 5 star experiences only**

unless the user explicitly requests otherwise.

This ensures recommendations reflect only places the user genuinely loved.

---

## Advanced Filtering

Examples:

> Show me my 5-star sushi restaurants.

> Show only 4+ star coffee shops.

> Recommend only my highest-rated date night restaurants.

> Show every 5-star place I've visited in New York.

---

## Recommendation Ranking

Recommendations are ranked using:

```
Overall Rating (highest weight)

+

Semantic Preference Match

+

Context Match

+

Companion Match

+

Recency

+

Recommendation Confidence
```

This creates recommendations that are both highly relevant and personally endorsed.

---

## Learning From Ratings

The system continuously learns from user ratings.

For example:

User gives five stars to:

* Outdoor seating
* Quiet restaurants
* Farm-to-table
* Waterfront dining

The Taste Graph increases confidence in those preferences.

Conversely, repeated one- and two-star ratings help the system learn what to avoid.

The explicit star rating complements the learned embedding-based taste model, creating a stronger feedback loop than embeddings alone.

---

## FR5 — Personal Taste Graph

Beyond ratings, TasteGraph continuously builds semantic preference vectors.

Example:

User consistently enjoys:

* Waterfront restaurants
* Craft cocktails
* Small intimate venues
* Outdoor seating
* Walkable neighborhoods
* Farm-to-table cuisine
* Conversation-friendly spaces

Each experience strengthens or weakens these embeddings.

Powered by:

* ZeroDB Vector Search
* ZeroMemory
* Knowledge Graph

---

## FR6 — Relationship Context

Each experience stores:

* Who attended
* Relationship
* Occasion

Examples:

* Wife
* Kids
* Parents
* Friends
* Investor
* Client
* Solo

Future recommendations become far more personalized.

---

## FR7 — City Memory

Each city becomes its own knowledge graph.

Example:

San Francisco

* Restaurants
* Coffee
* Cocktail Bars
* Parks
* Museums
* Hotels
* Views
* Walks
* Hidden Gems
* Remote Work Spots
* Family Activities

---

## FR8 — Personalized Recommendation Engine

The Recommendation Agent asks:

* Who is traveling?
* Budget?
* Food preferences?
* Kids?
* Walking?
* Business?
* Date night?

It then searches only the user's own memories.

By default, only 4–5 star experiences are returned.

---

## FR9 — Shareable Recommendation Agent

Instead of sending long text messages, users can share an AI-powered recommendation agent.

Examples:

* Share Link
* QR Code
* Temporary Chat Session

Friends interact naturally:

> "We're vegan."

> "Traveling with kids."

> "Need something under $40."

The agent filters recommendations automatically using the user's memory.

---

## FR10 — Friend Preference Profiles

TasteGraph remembers recurring preferences for friends and family.

Examples:

Mom

* Museums
* Gardens

Dad

* Seafood
* Scenic drives

Sarah

* Vegan

John

* Craft Beer

Kids

* Parks
* Ice Cream

Recommendations become increasingly personalized over time.

---

## FR11 — Continuous Learning

Every recommendation improves the system.

If a friend loves a recommendation:

Confidence increases.

If they dislike it:

Confidence decreases.

The Taste Graph becomes smarter with every interaction.

---

# AI Agents

### Experience Agent

Detects new experiences.

---

### Memory Agent

Creates structured memories.

---

### Taste Agent

Learns evolving preferences.

---

### Rating Agent

Tracks explicit ratings and updates recommendation confidence.

---

### City Agent

Organizes cities into knowledge graphs.

---

### Recommendation Agent

Answers recommendation requests.

---

### Friend Agent

Personalizes recommendations for specific people.

---

### Notification Agent

Collects lightweight feedback after visits.

---

# Data Model

## Experience

* id
* venue
* city
* category
* coordinates
* companions
* visit_date
* summary
* sentiment
* **overall_rating (1–5)**
* recommendation_confidence
* embeddings
* metadata

---

## Venue

* id
* name
* categories
* tags
* knowledge_graph

---

## Preference

* entity
* weight
* confidence
* last_updated

---

## Friend Profile

* id
* preferences
* dietary restrictions
* interests
* recommendation history

---

# AI-Native Architecture

## Agent Cloud

* Long-running autonomous agents
* Event orchestration
* Background processing
* Scheduled learning

---

## ZeroDB

* Structured storage
* Vector search
* Semantic retrieval

---

## ZeroMemory

Persistent user memory.

---

## Models API

* Classification
* Embeddings
* Summaries
* Extraction
* Recommendation reasoning

---

## Knowledge Graph

Relationships between:

User

↓

Cities

↓

Experiences

↓

Friends

↓

Occasions

↓

Preferences

↓

Ratings

↓

Recommendations

---

## AIKit

Reusable UI components:

* Chat
* Voice
* Experience Timeline
* Rating Cards
* Recommendation Lists
* Interactive Maps

---

## Lakehouse

Analytics:

* Favorite cities
* Favorite cuisines
* Average ratings by city
* Recommendation success
* Seasonal preferences
* Travel history

---

# Event Flow

```
Visit Detected

↓

Experience Agent

↓

Memory Extraction

↓

ZeroDB

↓

Knowledge Graph

↓

User Rates Experience (1–5)

↓

Taste Agent Updates Preferences

↓

Embeddings Updated

↓

Future Recommendations Improve
```

---

# Success Metrics

| Metric                           | Target                 |
| -------------------------------- | ---------------------- |
| Experience capture rate          | >90%                   |
| User feedback time               | <30 seconds            |
| Recommendation acceptance rate   | >70%                   |
| 4–5 star recommendation accuracy | >90% positive feedback |
| Recommendation generation time   | <5 seconds             |
| Manual tagging required          | <10%                   |
| Code written outside AINative    | <15%                   |

---

# Future Roadmap

### Wearables

Correlate enjoyment with:

* Apple Watch
* Oura
* WHOOP

---

### Camera Vision

One photo automatically extracts:

* Venue
* Menu
* Food
* Ambience

---

### Expense Matching

Automatically connect:

* Receipts
* Tips
* Company cards

---

### AI Trip Recaps

Examples:

> "Your Best Experiences in Tokyo"

---

### Taste Twins

Compare personal taste similarity with friends.

---

### Intent-Based Planning

Instead of searching for locations, users express an intent:

> "Plan a memorable anniversary weekend in Chicago with amazing food, quiet cocktail bars, and outdoor activities."

TasteGraph assembles a complete itinerary using only the user's highest-rated experiences, contextual knowledge, and learned preferences.

---

# Product Vision

TasteGraph transforms years of personal experiences into a continuously learning AI memory that becomes more valuable over time. By combining passive experience capture, semantic preference learning, explicit 1–5 star ratings, and AI-native orchestration on Agent Cloud, it evolves into a trusted personal concierge that delivers recommendations with the confidence of a close friend who knows exactly what you love. Every new experience strengthens the system, making its recommendations increasingly personalized, accurate, and shareable while requiring very little ongoing effort from the user.

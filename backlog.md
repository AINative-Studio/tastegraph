# TasteGraph

## Agile Product Backlog

### AI-Native Experience Memory Agent

This backlog is organized around vertical slices that leverage the AINative platform (Agent Cloud, ZeroDB, ZeroMemory, Models API, AIKit, Knowledge Graph, and Lakehouse) to minimize custom code. The MVP can be completed with the first six epics, while later epics progressively enhance intelligence and sharing.

---

# Epic 1 — User Identity & Onboarding

**Goal:** Enable users to create an account, connect data sources, and configure their personal experience agent.

## User Stories

### TG-1.1 User Registration

**As a** new user
**I want** to create an account
**So that** my experiences can be stored securely.

---

### TG-1.2 Connect Identity

As a user

I want to authenticate using Google or Apple

So my calendar and services can be connected.

---

### TG-1.3 Configure Home City

As a user

I want to define my home city

So recommendations understand my local area.

---

### TG-1.4 Connect External Services

As a user

I want to connect:

* Calendar
* Google Maps
* Apple Maps
* Gmail
* Photos

So the system can automatically detect experiences.

---

### TG-1.5 Configure Recommendation Defaults

As a user

I want to choose my default recommendation threshold (4 stars by default)

So recommendations automatically reflect my standards.

---

# Epic 2 — Experience Detection

**Goal:** Automatically detect experiences using Agent Cloud workflows.

## User Stories

### TG-2.1 Detect Restaurant Visits

Automatically create experiences from location history.

---

### TG-2.2 Detect Calendar Events

Create experiences from calendar events.

---

### TG-2.3 Detect Ticketed Events

Create experiences from:

* Eventbrite
* Ticketmaster

---

### TG-2.4 Detect Travel

Create hotel, airport, and destination experiences automatically.

---

### TG-2.5 Merge Duplicate Signals

Merge calendar, GPS, receipt, and reservation data into one experience.

---

### TG-2.6 Manual Experience Entry

Allow manual check-ins.

---

# Epic 3 — Experience Capture

**Goal:** Capture rich structured memories.

## User Stories

### TG-3.1 AI Summary

Generate experience summaries using Models API.

---

### TG-3.2 Extract Metadata

Automatically classify:

* cuisine
* category
* mood
* atmosphere
* price
* companions

---

### TG-3.3 Store Photos

Associate uploaded photos with experiences.

---

### TG-3.4 Voice Notes

Allow voice reflections after experiences.

---

### TG-3.5 Timeline View

Display all experiences chronologically.

---

# Epic 4 — Ratings & Reviews

**Goal:** Capture explicit user feedback.

## User Stories

### TG-4.1 Overall Rating

Rate experiences from 1–5 stars.

---

### TG-4.2 Category Ratings

Capture:

* Food
* Service
* Atmosphere
* Value

---

### TG-4.3 Would Return

Simple Yes / Maybe / No question.

---

### TG-4.4 Favorite Dishes

Store favorite menu items.

---

### TG-4.5 Private Notes

Allow freeform notes.

---

### TG-4.6 Quick Rating Card

Complete rating in under 30 seconds.

---

# Epic 5 — Venue Knowledge

**Goal:** Build reusable venue intelligence.

## User Stories

### TG-5.1 Canonical Venue

Normalize duplicate venues.

---

### TG-5.2 Venue Metadata

Store:

* website
* phone
* hours
* coordinates

---

### TG-5.3 Venue Tags

Automatically generate semantic tags.

---

### TG-5.4 Neighborhood Assignment

Map venues into neighborhoods.

---

### TG-5.5 Venue Statistics

Calculate:

* visits
* average rating
* last visit

---

# Epic 6 — Taste Learning Engine

**Goal:** Continuously learn user preferences.

## User Stories

### TG-6.1 Learn Positive Preferences

Increase confidence for repeatedly loved experiences.

---

### TG-6.2 Learn Negative Preferences

Reduce confidence for disliked attributes.

---

### TG-6.3 Generate Preference Embeddings

Store embeddings in ZeroDB.

---

### TG-6.4 Knowledge Graph Updates

Automatically update graph relationships.

---

### TG-6.5 Confidence Scoring

Maintain confidence score for every learned preference.

---

### TG-6.6 Preference Dashboard

Visualize learned preferences.

---

# Epic 7 — Companion Intelligence

**Goal:** Learn who the user spends time with.

## User Stories

### TG-7.1 Create People Profiles

Store family and friends.

---

### TG-7.2 Associate Experiences

Attach companions to experiences.

---

### TG-7.3 Companion Preferences

Learn likes and dislikes.

---

### TG-7.4 Relationship Memory

Track recurring activities.

---

### TG-7.5 Companion History

Show shared experiences.

---

# Epic 8 — Recommendation Engine

**Goal:** Deliver highly personalized recommendations.

## User Stories

### TG-8.1 Recommend Restaurants

Recommend restaurants in a city.

---

### TG-8.2 Recommend Events

Recommend concerts and attractions.

---

### TG-8.3 Recommend Hotels

Recommend accommodations.

---

### TG-8.4 Recommend Entire Weekend

Generate complete itineraries.

---

### TG-8.5 Respect Rating Filter

Return only 4–5 star experiences by default.

---

### TG-8.6 Semantic Search

Match recommendations using vector search.

---

### TG-8.7 Explain Recommendations

Display why each recommendation was selected.

---

# Epic 9 — Friend & Family Recommendation Agent

**Goal:** Personalize recommendations for others.

## User Stories

### TG-9.1 Friend Profiles

Store recurring friend preferences.

---

### TG-9.2 Dietary Preferences

Store:

* vegan
* gluten free
* seafood

---

### TG-9.3 Accessibility Preferences

Store mobility needs.

---

### TG-9.4 Family Recommendations

Recommend based on recipient profile.

---

### TG-9.5 Share AI Agent

Generate temporary recommendation agent.

---

### TG-9.6 Share Link

Create shareable recommendation URL.

---

# Epic 10 — City Memory

**Goal:** Build long-term knowledge about cities.

## User Stories

### TG-10.1 City Dashboard

Display all experiences within a city.

---

### TG-10.2 Favorite Places

Rank venues.

---

### TG-10.3 Hidden Gems

Identify lesser-known favorites.

---

### TG-10.4 Neighborhood Explorer

Browse by neighborhood.

---

### TG-10.5 Seasonal Memories

Recommend based on season.

---

# Epic 11 — Agent Cloud Workflows

**Goal:** Automate the platform.

## User Stories

### TG-11.1 Experience Agent

Monitor integrations.

---

### TG-11.2 Memory Agent

Generate memories.

---

### TG-11.3 Rating Agent

Request ratings after visits.

---

### TG-11.4 Taste Agent

Update preferences.

---

### TG-11.5 Recommendation Agent

Generate recommendations.

---

### TG-11.6 Notification Agent

Prompt users when information is missing.

---

# Epic 12 — Knowledge Graph

**Goal:** Build interconnected intelligence.

## User Stories

### TG-12.1 Create Graph Nodes

Users

Venues

Cities

Experiences

People

Preferences

---

### TG-12.2 Build Relationships

Visited

Likes

Dislikes

Recommended

Attended

---

### TG-12.3 Graph Search

Query relationships.

---

### TG-12.4 Similar Experiences

Find related experiences.

---

# Epic 13 — AI Search

**Goal:** Natural language retrieval.

## User Stories

### TG-13.1 Search Experiences

"Best tacos I've ever had."

---

### TG-13.2 Search Cities

"My favorite places in Tokyo."

---

### TG-13.3 Search Friends

"What restaurants did Sarah love?"

---

### TG-13.4 Search by Mood

"Quiet date night."

---

### TG-13.5 Search by Rating

"Show only my five-star restaurants."

---

# Epic 14 — Analytics

**Goal:** Personal insights.

## User Stories

### TG-14.1 Favorite Cuisine

---

### TG-14.2 Favorite City

---

### TG-14.3 Average Ratings

---

### TG-14.4 Most Visited Venues

---

### TG-14.5 Recommendation Success

---

### TG-14.6 Taste Evolution

Track preference changes over time.

---

# Epic 15 — AIKit Frontend

**Goal:** Deliver a polished AI-native UI.

## User Stories

### TG-15.1 Experience Timeline

---

### TG-15.2 City Explorer

---

### TG-15.3 Maps

---

### TG-15.4 Recommendation Cards

---

### TG-15.5 Voice Chat

---

### TG-15.6 AI Chat Assistant

---

# Epic 16 — Notifications

**Goal:** Keep memories fresh.

## User Stories

### TG-16.1 Post Visit Reminder

---

### TG-16.2 Missing Rating Reminder

---

### TG-16.3 Weekly Digest

---

### TG-16.4 Monthly Recap

---

### TG-16.5 Recommendation Follow-up

Ask whether shared recommendations were successful.

---

# Epic 17 — Lakehouse & Intelligence

**Goal:** Learn from years of experiences.

## User Stories

### TG-17.1 Experience Analytics

---

### TG-17.2 Recommendation Effectiveness

---

### TG-17.3 Preference Drift

---

### TG-17.4 Travel Heatmaps

---

### TG-17.5 Trend Detection

---

# Epic 18 — Administration

## User Stories

### TG-18.1 User Settings

---

### TG-18.2 Export Data

---

### TG-18.3 Delete Experiences

---

### TG-18.4 Privacy Controls

---

### TG-18.5 GDPR/CCPA Compliance

---

# MVP Release (Sprint 1–6)

* User authentication and onboarding
* Automatic experience detection
* Experience timeline
* AI memory extraction
* 1–5 star rating workflow
* ZeroDB storage
* ZeroMemory integration
* Knowledge Graph updates
* Taste learning engine
* Recommendation engine with 4+ star filtering
* AI chat interface
* City dashboards
* Friend profiles
* Shareable recommendation agent

---

# Phase 2

* Companion intelligence
* Trip itinerary generation
* Voice capture
* AI-generated city guides
* Photo analysis
* Restaurant menu recognition
* Weekly and monthly insights
* Recommendation feedback loops
* Analytics dashboards

---

# Phase 3

* Apple Watch, Oura, and WHOOP integrations
* Collaborative travel planning
* Taste similarity ("Taste Twins")
* Multi-user shared memories
* Public recommendation publishing
* AI travel concierge
* Predictive recommendations based on weather, seasonality, and upcoming travel

---

# Estimated Backlog Size

| Level                         | Count |
| ----------------------------- | ----: |
| Epics                         |    18 |
| User Stories                  |   95+ |
| AI Agents                     |     6 |
| Core Database Tables          |    15 |
| Agent Cloud Workflows         |   20+ |
| ZeroDB Collections            |    15 |
| Knowledge Graph Relationships |   40+ |
| AIKit Screens                 |   20+ |

This backlog is intentionally structured around **vertical AI-native capabilities** rather than traditional frontend/backend layers. Each epic delivers an end-to-end slice of functionality by composing existing AINative platform services (Agent Cloud, ZeroDB, ZeroMemory, Models API, AIKit, and the Knowledge Graph), allowing the majority of the product to be assembled through configuration and orchestration instead of custom application code.

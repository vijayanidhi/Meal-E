# Meal-E 🍽️
**Meals made Eeeazy.**

A smart fridge-integrated app that bridges the gap between what's in your fridge and what's on your plate — helping people (especially budget-conscious students) cut food waste, save money, and hit their nutritional goals.

## Inspiration

As college students, we constantly struggle with food waste and meal planning. Ingredients sit in the fridge until they expire, we forget what we have, and we end up spending money eating out instead of cooking what's already available. We wanted to build something that bridges the gap between what's in your fridge and what's on your plate — especially for students on a budget trying to eat healthy and hit their nutritional goals.

## What it does

Meal-E is a smart meal planning system that:

- Uses a fridge-mounted camera to automatically detect ingredients via computer vision
- Stores detected items in a pantry database with nutritional info and expiration dates
- Generates personalized weekly meal plans using AI
- Prioritizes ingredients that are expiring soon
- Respects dietary preferences and allergies
- Optimizes for user-defined macro targets (calories, protein, etc.)

## Tech Stack

- **Backend:** FastAPI
- **Database:** PostgreSQL (via pg8000)
- **AI / Meal Planning:** Gemini API
- **Frontend:** Swift (iOS)
- **Computer Vision:** Custom fridge camera detection script

## How We Built It

We used computer vision (via a fridge camera script) to identify ingredients entering and leaving the fridge. The backend is built with FastAPI and PostgreSQL (via pg8000) to sync pantry state, track nutritional data, and manage expiration dates. Meal plan generation is powered by Gemini's API, prompted with the user's pantry inventory, dietary preferences, and macro targets. The iOS frontend is built in Swift, giving users a clean interface to view their pantry and weekly meal plans.

## Challenges We Ran Into

- Getting pantry sync right was tricky — we hit column naming mismatches in our database schema, date parsing errors from passing numeric values into date fields, and issues with parameter ordering in SQL inserts.
- Integrating AI meal plan generation required careful prompt engineering to ensure the model only used ingredients actually in the pantry and accurately calculated macros.
- Coordinating the Git workflow across the team had its bumps too, with divergent branches and repo restructuring mid-hackathon.

## Accomplishments That We're Proud Of

We built a fully functional end-to-end pipeline in 24 hours — from a camera detecting ingredients, to a database tracking them, to an AI generating meal plans from them. The system respects dietary constraints, prioritizes expiring food, and produces meal plans with real recipes and accurate macro breakdowns.

## What We Learned

We learned a lot about prompt engineering for structured JSON output from LLMs, working with PostgreSQL in Python, handling edge cases in computer vision pipelines, and coordinating a full-stack project across a 5-person team under time pressure. We also deepened our understanding of nutritional data modeling and how to build reliable data flows between hardware, backend, and frontend.

## What's Next for Meal-E

- High-quality barcode scanners and internal cameras for improved accuracy
- Production-grade vision models for reliable detection
- Edge + cloud integration for fast processing and scalability
- Automated tracking with minimal user effort
- Adaptive freshness modeling based on real-time temperature data

## Team

Built by a 5-person team in 24 hours, with Vijayanidhi Pillai contributing to the project.

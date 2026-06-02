# AI Daily Life Assistant – Architecture Overview

## Overview
AI Daily Life Assistant is a closed‑source Windows `.exe` application designed for fast, local personal analytics with optional AI enhancements. The system stores all user data locally in SQL Server Express, ensuring privacy, reliability, and full data ownership. Unlike cloud‑dependent productivity apps, AI Daily Life Assistant performs all analysis on‑device, requiring internet only for subscription verification and optional token‑based AI actions.

The application supports SQL Server Express for simple, single‑user setups and uses a secure subscription + token model for monetization.

---

# Architecture

## Subscription Access Control
AI Daily Life Assistant uses a lightweight licensing system to control access to the application.

### Subscription Requirement
A valid Stripe subscription is required to unlock the app. The subscription governs **access**, not AI usage.

### Subscription Flow
- On startup, the app checks subscription status through the backend.
- If active → full access is granted.
- If inactive → the user is redirected to the **License Gate**.
- The user can subscribe through Stripe’s secure checkout.
- Internet is required only during subscription checks and billing actions.

### License Gate
The License Gate provides:
- “Subscribe Now” → opens Stripe Checkout
- “I Completed Payment” → rechecks subscription status
- “Exit” → closes the application

This ensures clean, predictable access control without interfering with local data or token usage.

---

## Token‑Based AI Usage
AI Daily Life Assistant uses a **dual‑layer monetization model**:

### Subscription → Access to the app  
### Tokens → Pay‑per‑use AI actions

Tokens are purchased through Stripe one‑time payments and are only required when the user chooses to run AI‑powered features.

### Token Workflow
- User initiates an AI action.
- App checks token balance via backend.
- If insufficient tokens → Token Gate appears.
- User can purchase token packs through Stripe Checkout.
- Stripe webhook credits tokens to the user’s balance.
- User retries the AI action once tokens are available.

This model keeps the app affordable while allowing scalable AI usage.

---

## Local Session Context
- All personal data is stored locally in SQL Server Express.
- No cloud sync, no external LLM, no remote data storage.
- The app uses a persistent `client_key` to identify the installation.
- After subscription verification, the app operates fully offline except for optional AI token purchases.

---

## SQL Connection Page
The application includes a built‑in SQL Express connection setup:

- `sql_connection_page.py`  
  - Tests SQL Express connection  
  - Validates credentials  
  - Creates database if missing  
  - Ensures stable local storage  

This page is shown on first launch or when the database connection is missing.

---

## Data Storage & Local Analytics
AI Daily Life Assistant uses SQL Express to store:

- Tasks  
- Meals  
- Workouts  
- Daily logs  
- User preferences  
- Terms agreement  

Local analytics are performed through `ai_client.py`, which generates:

- Daily plans  
- Meal suggestions  
- Workout recommendations  
- General insights  

All analysis is rule‑based and runs entirely on the user’s machine.

---

## Application Flow
**Startup Sequence:**

1. Terms & Conditions Gate  
2. Subscription License Gate  
3. Token Gate (only for AI actions)  
4. Start Page Dashboard  

**AI Usage Sequence:**

User Action → Token Check → AI Processing → Response

**Subscription Sequence:**

License Inactive → License Gate → Stripe Checkout → Webhook → License Active

---

## File Storage & Export
All user‑generated data and analytics remain local:

- SQL Express database files  
- User logs  
- Task, meal, and workout history  
- Local configuration files  

No data is uploaded to external servers except:

- Subscription verification (Stripe)
- Token purchases (Stripe)

---

## Summary
AI Daily Life Assistant is built on a privacy‑first, local‑analytics architecture with a clean dual‑layer monetization model:

- **Subscription** unlocks the app  
- **Tokens** unlock AI actions  

The system is lightweight, secure, and designed for long‑term maintainability with minimal external dependencies.

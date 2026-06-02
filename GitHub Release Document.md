# AI Daily Life Assistant — Unified Local Analytics Edition
## Initial GitHub Release — Version 1.0.0

This release introduces the unified version of the AI Daily Life Assistant, a Windows `.exe` application designed for fast, private, and fully local personal analytics. The app stores all user data in SQL Server Express and performs all insights, planning, and recommendations on‑device — no cloud LLMs, no external data sync, and no third‑party data processing.

The application includes a subscription access layer and an optional token‑based AI enhancement system, both powered through secure Stripe Checkout.

---

## Subscription Access Control
AI Daily Life Assistant uses a lightweight licensing system to control access to the application.

Subscription Required  
A valid Stripe subscription is required to unlock and use the app.

Subscription Flow  
• On startup, the app checks your subscription status securely through the backend.  
• If your subscription is active, full access is granted.  
• If your subscription is inactive, canceled, or unpaid, access is restricted.  
• Internet is required only during subscription verification and billing actions.  
• All billing, upgrades, and renewals are handled through Stripe’s secure checkout.

License Gate  
If the subscription is inactive, the user is shown a License Gate with options to subscribe, retry verification, or exit the application.

---

## Included in This Release
- Unified local analytics engine  
- SQL Express database storage  
- Subscription access control  
- Token‑based AI usage system  
- Daily planning engine  
- Meal suggestion engine  
- Workout recommendation engine  
- General insight engine  
- Local session context  
- One installer, one app, one onboarding flow  

---

## Feature Descriptions

### Daily Planning
Generates a personalized daily plan based on tasks stored in the local SQL database.  
Ideal for users who want structured guidance without cloud‑based AI.

---

### Meal Suggestions
Analyzes recent meal entries and provides balanced nutritional recommendations.  
Designed for users tracking food habits or improving dietary routines.

---

### Workout Recommendations
Reads workout history and generates daily exercise suggestions.  
Useful for maintaining consistent fitness habits.

---

### General Insights
A rule‑based engine that interprets user prompts and routes them to the appropriate analytics module.  
Provides simple, fast, and private responses without external APIs.

---

## Token‑Based AI Usage
AI Daily Life Assistant includes an optional pay‑per‑use AI enhancement system.

• Tokens are purchased through Stripe one‑time payments.  
• Tokens are required only when running AI‑powered features.  
• Users can continue using all non‑AI features without tokens.  
• Token balance is stored securely on the backend and checked before each AI action.  

This model keeps the app affordable while allowing scalable AI usage.

---

## License Activation
A valid Stripe subscription is required to use the application.

• On first launch, the app checks your subscription status.  
• If active, the app unlocks full access.  
• If inactive, the user is redirected to the License Gate.  
• Internet is required only during subscription checks and billing events.  
• All payments are handled through Stripe’s secure checkout.  

---

## Database
AI Daily Life Assistant uses SQL Server Express for all local data storage:

### SQL Express (Local Database — Recommended for All Users)
- Automatically configured during setup  
- Ideal for single‑machine operation  
- Fully offline and self‑contained  
- Stores tasks, meals, workouts, logs, and user preferences  

All analytics are performed locally using this database.

---

## Stability
This version is the current stable build and serves as the foundation for all future updates.  
The architecture is designed for long‑term maintainability, privacy, and offline reliability.


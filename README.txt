AI Daily Life Assistant App – README.txt
====================================

Welcome to the Automating Innovating AI Daily Life Assistant App — a personal productivity,
health, wellness, and habit‑tracking system powered entirely by local analytics, secure data
storage, and a token‑based AI Assistant.

This app helps users manage tasks, meals, workouts, habits, daily planning, and personal insights
through a unified dashboard and analytics center.


====================================
Core Philosophy
====================================
The AI Daily Life Assistant App is designed to:

• Improve daily organization
• Track personal health and wellness
• Provide actionable insights
• Keep all data local and private
• Offer an AI Assistant without external APIs
• Deliver professional‑grade analytics without subscriptions

All intelligence is performed locally using your stored data.


====================================
Key Features
====================================

Tasks Manager
-------------
• Add, update, delete, and track daily tasks
• Priority levels (Low, Medium, High)
• Due dates and completion tracking
• Productivity analytics and charts

Meals Tracker
-------------
• Log meals with ingredients and calories
• Track nutritional patterns
• View calorie trends over time
• Meal‑type distribution charts

Workouts Tracker
----------------
• Log workout type, duration, intensity, and date
• Track fitness progress
• View duration trends and intensity breakdowns

Habits & Habit Logs
-------------------
• Create habits with weekly targets
• Log daily completions
• Habit completion analytics
• Weekly heatmap visualization

AI Assistant (Token‑Based)
--------------------------
• Local analytics engine — no external AI
• Generates:
  - Daily plans
  - Meal suggestions
  - Workout recommendations
  - General insights
• Uses tokens only when the Assistant is used
• CRUD and analytics features require zero tokens

Analytics Center
----------------
A unified dashboard with:

• Fullscreen Canvas‑based charts
• Tasks, meals, workouts, and habits analytics
• Weekly summary panel
• AI Insights tab
• Export/Import tab (CSV, JSON, PDF)

Export & Import
---------------
• Export all data to CSV or JSON
• Import CSV/JSON backups
• Generate PDF summary reports
• Uses built‑in file_manager.py and pdf_generator.py

Terms & Conditions Enforcement
------------------------------
• User must accept Terms on first launch
• Acceptance stored in SQL database
• Optional versioning system forces re‑acceptance when updated


====================================
System Requirements
====================================
• Windows 10 or later
• SQL Server Express LocalDB
• ~900 MB available disk space
• No internet required except for token purchases
• No external AI APIs required


====================================
Token System
====================================
The AI Assistant uses a token‑based model:

• Tokens are consumed only when generating AI insights
• CRUD, charts, analytics, and dashboards require no tokens
• Users may purchase token packs through Stripe
• If tokens reach zero, the Token Gate screen appears
• All other app features remain fully accessible


====================================
Getting Started
====================================
1. Launch the AI Daily Life Assistant App
2. Accept the Terms & Conditions (first launch only)
3. Navigate to the Start Page
4. Use the dashboard to access:
   • Tasks
   • Meals
   • Workouts
   • Habits
   • Analytics Center
   • AI Assistant
5. Purchase tokens only if you want AI insights


====================================
Navigation & Exiting
====================================
• Use the Start Page to access all modules
• Press ESC to exit fullscreen
• Click “Exit” on any screen to close the app


====================================
Tips
====================================
• Log tasks daily for better planning
• Track meals consistently for accurate calorie trends
• Use the heatmap to maintain habit streaks
• Export data regularly
• Use tokens only when needed — analytics are free


====================================
Troubleshooting
====================================
App won’t launch:
• Ensure Windows 10+ is installed
• Confirm SQL Server Express LocalDB is available

Token Gate appears unexpectedly:
• Check your token balance
• Complete your Stripe purchase

Charts not displaying:
• Ensure your screen resolution is 1080p or higher

Import failed:
• Ensure CSV/JSON format matches exported structure


====================================
Support
====================================
Questions or feedback?
automatinginnovatingai@outlook.com

Thank you for using the AI Daily Life Assistant App!

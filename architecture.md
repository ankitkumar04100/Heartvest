# 🏗️ Heartvest Architecture (Conceptual)

Heartvest follows a *modular architecture* designed for scalability and flexibility.

## 🔑 Components
1. *Frontend (React Native)*
   - Cross-platform UI for Android/iOS
   - Couples dashboard, milestone tracker, and rewards page

2. *Backend (Python / Flask or Django)*
   - Handles user authentication
   - Relationship "investment" logic
   - AI suggestion engine (conceptual GPT-OSS integration)

3. *Database*
   - Firebase Firestore (NoSQL) or PostgreSQL (SQL)
   - Stores user profiles, activities, and milestones

4. *AI Layer (Conceptual)*
   - GPT-OSS-20B used for:
     - Personalized activity suggestions
     - Reward multipliers
     - Notification messages

5. *Notifications & Payments*
   - Twilio/SendGrid for SMS/email reminders
   - Razorpay/Stripe (future integration) for investment tracking

## 🖼️ Example Flow
```mermaid
graph TD
    A[User Action] --> B[Frontend: React Native]
    B --> C[Backend: Flask/Django API]
    C --> D[Database: Firestore/PostgreSQL]
    C --> E[AI Suggestion Engine - GPT-OSS]
    D --> F[Milestone Dashboard]
    E --> F
    F --> G[Rewards & Notifications]

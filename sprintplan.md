# 🏁 Sprint Plan: VoiceCal – Speech-to-Text Food Tracking App (Windsurf Build)

## Overview
- **Platform:** Windsurf (AI-agent-based IDE)
- **Team Composition:**  
  - 🧠 NLP Agent (Speech-to-text + LLM Parsing)  
  - 📱 Frontend Agent (UI/UX & React Native Interface)  
  - 🔧 Backend Agent (API & Data Layer)  
  - 🔒 Auth & Sync Agent (OAuth + HealthKit/Google Fit sync)
- **Sprint Duration:** 2 weeks
- **Total Duration:** 4 sprints (8 weeks)

---

## 🚀 Sprint 1: Voice Logging MVP + Transcription Pipeline

**Goal:** Capture voice input, convert to transcription, store raw logs.

### Tasks:
- `Frontend Agent`:
  - Build minimal mobile UI with:
    - Tap-to-speak mic button
    - Log list view (static)
- `NLP Agent`:
  - Integrate Whisper/OpenAI STT API
  - Create basic transcription processor with confidence scoring
- `Backend Agent`:
  - Create VoiceLog model + API endpoint to store transcriptions
  - Set up Postgres + backend project scaffold
- `Infra Agent`:
  - Deploy minimal backend API + DB
  - Set up staging environment in Windsurf

### Deliverables:
- Voice input → transcript → stored backend entry
- Functional dev environment for frontend/backend agents

---

## 🔍 Sprint 2: AI Food Parsing + Nutrient Estimation Engine

**Goal:** Parse transcriptions into food entries and estimate nutritional values.

### Tasks:
- `NLP Agent`:
  - Build LLM prompt pipeline for natural language food parsing
  - Integrate USDA FDC API / Nutritionix for lookup
  - Generate structured food entries with portion estimation
- `Backend Agent`:
  - Create FoodEntry model and link to VoiceLogs
  - Add nutrient estimation fields (kcal, macros)
  - Store model version used for predictions
- `Frontend Agent`:
  - Display parsed food items & nutritional breakdown
  - Allow manual edits to entries

### Deliverables:
- Voice → transcript → food entry → calorie/macros
- Editable food logs displayed in the app

---

## 📊 Sprint 3: Sync, Dashboard & Daily Logging Flow

**Goal:** Enable health app sync, summary dashboards, and daily diary.

### Tasks:
- `Auth & Sync Agent`:
  - Integrate OAuth for Apple Health & Google Fit
  - Implement sync scheduler & conflict handling
- `Backend Agent`:
  - Create `NutritionSummary` model
  - Add scheduled aggregation for daily totals
- `Frontend Agent`:
  - Build daily diary view with calorie/macronutrient totals
  - Add trend graph UI (weekly/monthly)
- `NLP Agent`:
  - Add time context detection from logs (e.g., "for lunch")

### Deliverables:
- Connected health apps
- Food diary + summary dashboard with trend visualization

---

## 🔐 Sprint 4: Personalization, Settings & Export

**Goal:** Add personalization, reminder UX, privacy settings, and CSV/PDF export.

### Tasks:
- `Frontend Agent`:
  - Add user profile and preferences screen
  - Build notification reminder UI and controls
  - Add export buttons (CSV, PDF via backend)
- `Backend Agent`:
  - Implement unit conversion (metric/imperial)
  - Build log export endpoints
  - Enable data deletion requests
- `NLP Agent`:
  - Add multilingual support for STT/NLP agents
- `Auth Agent`:
  - Finalize user authentication & secure session management

### Deliverables:
- Full user preference control
- Reminders and export tools
- Privacy + account controls

---

## ✅ Post-Sprint Wrap & Next Steps

### Windsurf Integration Notes:
- Agents should use the **shared task memory** and **typed data contracts**.
- User testing flows should be scripted as agent test-cases.
- Debug traces for NLP and API calls should be reviewed with autonomous test agents.
- Set up CI/CD pipeline using Windsurf's deployment triggers.

### Optional Sprint 5 (Future Enhancements):
- Image-based food recognition
- Smart meal recommendations
- Social logging and coach view

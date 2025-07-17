# 🗂️ Product Backlog: VoiceCal – AI Food Logging App

## 🧠 EPIC 1: Voice Input & Transcription

### US 1.1 – Start Voice Logging
**As a user**, I want to press a button to start recording my voice so I can log my food quickly.

- **Acceptance Criteria:**
  - A visible mic button starts and stops recording.
  - Audio is saved and sent to backend for transcription.

- **Priority:** High

---

### US 1.2 – Auto Transcribe Voice Input
**As a user**, I want my voice input to be transcribed into text automatically.

- **Acceptance Criteria:**
  - Audio is transcribed in <2 seconds.
  - Transcript is displayed for confirmation or editing.

- **Priority:** High

---

### US 1.3 – Playback Voice Logs
**As a user**, I want to replay my recording to confirm what I said was captured correctly.

- **Acceptance Criteria:**
  - Audio playback is available after logging.
  - User can re-record if needed.

- **Priority:** Medium

---

## 🤖 EPIC 2: AI Food Parsing & Nutrition Estimation

### US 2.1 – Parse Food from Natural Language
**As a user**, I want the app to understand what foods I ate from my spoken input.

- **Acceptance Criteria:**
  - System identifies individual food items and quantities.
  - Handles variations like “a slice of pizza” vs “two medium pepperoni pizzas”.

- **Priority:** High

---

### US 2.2 – Estimate Nutritional Data
**As a user**, I want the app to tell me how many calories, protein, carbs, and fats I consumed.

- **Acceptance Criteria:**
  - AI matches food to nutrition database.
  - Estimates calories/macros with a confidence score.

- **Priority:** High

---

### US 2.3 – Edit Nutrient Estimates
**As a user**, I want to edit the AI's estimation if I know it’s inaccurate.

- **Acceptance Criteria:**
  - Editable fields for quantity, calories, macros.
  - Changes are saved to log.

- **Priority:** Medium

---

## 📅 EPIC 3: Food Diary & Trend Dashboard

### US 3.1 – View Daily Food Diary
**As a user**, I want to see what I’ve eaten today with nutrient totals.

- **Acceptance Criteria:**
  - Displays list of food entries.
  - Shows total calories, protein, carbs, fats.

- **Priority:** High

---

### US 3.2 – Review Weekly & Monthly Trends
**As a user**, I want to view graphs of how my food intake changes over time.

- **Acceptance Criteria:**
  - Line/bar graphs for nutrients over time.
  - Filters for day/week/month.

- **Priority:** Medium

---

### US 3.3 – Set and Track Nutrition Goals
**As a user**, I want to set calorie or macro goals and track progress.

- **Acceptance Criteria:**
  - Set daily target values.
  - Progress bar or indicator on dashboard.

- **Priority:** Medium

---

## 🔄 EPIC 4: Sync with Health Platforms

### US 4.1 – Connect to Apple Health / Google Fit
**As a user**, I want to sync my food logs to Apple Health or Google Fit.

- **Acceptance Criteria:**
  - OAuth integration and permissions.
  - Data pushes to and pulls from connected apps.

- **Priority:** High

---

### US 4.2 – Sync with Fitbit / MyFitnessPal
**As a user**, I want to sync with other platforms like Fitbit or MyFitnessPal.

- **Acceptance Criteria:**
  - OAuth connection flow.
  - Nutrition logs shared both ways.

- **Priority:** Medium

---

### US 4.3 – Export Logs
**As a user**, I want to export my logs as a CSV or PDF to share with my coach or doctor.

- **Acceptance Criteria:**
  - Export button available on dashboard.
  - Formats include CSV and PDF.

- **Priority:** Low

---

## 🔐 EPIC 5: Privacy, Security & Preferences

### US 5.1 – Set Unit Preferences
**As a user**, I want to switch between metric and imperial units.

- **Acceptance Criteria:**
  - Global setting for grams vs ounces, cm vs inches, etc.
  - Logs update to reflect preference.

- **Priority:** Medium

---

### US 5.2 – Configure Reminder Notifications
**As a user**, I want reminders to log meals if I forget.

- **Acceptance Criteria:**
  - Users can set reminder times (e.g., 8AM, 1PM).
  - Push notifications are sent accordingly.

- **Priority:** Medium

---

### US 5.3 – Manage My Data & Privacy
**As a user**, I want to see what data is stored and delete it if I choose.

- **Acceptance Criteria:**
  - Data export and deletion options available in settings.
  - Clear privacy policy and terms of service.

- **Priority:** High

---

## 🌐 EPIC 6: Onboarding & Account Management

### US 6.1 – Sign Up and Log In
**As a user**, I want to create an account and securely log in to access my data.

- **Acceptance Criteria:**
  - Email/password registration or OAuth (Google/Apple).
  - Email validation and error handling.

- **Priority:** High

---

### US 6.2 – Onboarding Tutorial
**As a new user**, I want a brief guide to show me how to use voice logging.

- **Acceptance Criteria:**
  - 3–5 step walkthrough on first launch.
  - Skip or revisit option.

- **Priority:** Medium

---

### US 6.3 – Edit Profile & Health Data
**As a user**, I want to update my name, DOB, height, weight, and goals.

- **Acceptance Criteria:**
  - Editable profile section.
  - Fields saved securely.

- **Priority:** Medium

---

## 📸 EPIC 7: Future – Multimodal (Image + Voice)

### US 7.1 – Upload or Snap Food Image
**As a user**, I want to take a picture of my food to help improve accuracy.

- **Acceptance Criteria:**
  - Image upload or camera integration.
  - Image sent to AI for visual food recognition.

- **Priority:** Future

---

### US 7.2 – Combine Voice & Image Inputs
**As a user**, I want the app to use both my voice and an image for better food recognition.

- **Acceptance Criteria:**
  - Backend combines image + transcription.
  - Results merged for higher accuracy.

- **Priority:** Future


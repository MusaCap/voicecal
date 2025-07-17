# 📊 Data Model: VoiceCal – Speech-to-Text Food Tracking App

## 1. Users

Represents a registered user of the app.

| Field Name       | Type       | Description                            |
|------------------|------------|----------------------------------------|
| user_id          | UUID       | Primary key                            |
| name             | String     | Full name                              |
| email            | String     | Unique login ID                        |
| password_hash    | String     | Secure hashed password                 |
| date_of_birth    | Date       | Used to personalize caloric needs      |
| gender           | String     | 'male', 'female', 'other'              |
| height_cm        | Integer    | Height in centimeters                  |
| weight_kg        | Float      | Weight in kilograms                    |
| activity_level   | String     | e.g. 'sedentary', 'active'             |
| created_at       | Timestamp  | Account creation time                  |
| updated_at       | Timestamp  | Last update timestamp                  |

---

## 2. VoiceLogs

Stores raw and transcribed user voice input.

| Field Name       | Type       | Description                            |
|------------------|------------|----------------------------------------|
| log_id           | UUID       | Primary key                            |
| user_id          | UUID       | Foreign key to Users                   |
| audio_url        | String     | Path to uploaded voice file            |
| transcription    | Text       | Transcribed natural language           |
| timestamp        | Timestamp  | Time voice log was created             |
| confidence_score | Float      | NLP model confidence (0.0 to 1.0)      |
| parsed           | Boolean    | Was it successfully parsed?            |

---

## 3. FoodEntries

Represents AI-processed entries from voice logs.

| Field Name       | Type       | Description                            |
|------------------|------------|----------------------------------------|
| entry_id         | UUID       | Primary key                            |
| log_id           | UUID       | Foreign key to VoiceLogs               |
| user_id          | UUID       | Redundant for query speed              |
| food_item        | String     | Canonical food name (e.g. 'Grilled Chicken Breast') |
| quantity         | Float      | Amount consumed (in grams or units)    |
| unit             | String     | e.g. 'g', 'cup', 'slice'               |
| meal_type        | String     | e.g. 'breakfast', 'lunch', 'snack'     |
| estimated_calories | Float    | Estimated total kcal                   |
| protein_g        | Float      | Estimated protein in grams             |
| carbs_g          | Float      | Estimated carbohydrates in grams       |
| fat_g            | Float      | Estimated fat in grams                 |
| log_date         | Date       | Date consumed                          |
| ai_model_version | String     | Model version used for estimation      |

---

## 4. HealthSync

Tracks synced external platform data.

| Field Name       | Type       | Description                            |
|------------------|------------|----------------------------------------|
| sync_id          | UUID       | Primary key                            |
| user_id          | UUID       | Foreign key to Users                   |
| platform         | String     | e.g. 'Apple Health', 'Fitbit'          |
| access_token     | String     | OAuth token (encrypted)                |
| last_sync_time   | Timestamp  | Last successful sync                   |
| sync_status      | String     | 'success', 'error', 'pending'          |

---

## 5. NutritionSummaries

Aggregated daily summaries per user.

| Field Name       | Type       | Description                            |
|------------------|------------|----------------------------------------|
| summary_id       | UUID       | Primary key                            |
| user_id          | UUID       | Foreign key to Users                   |
| summary_date     | Date       | Day of summary                         |
| total_calories   | Float      | Sum of calories                       |
| total_protein_g  | Float      | Sum of protein in grams                |
| total_carbs_g    | Float      | Sum of carbs in grams                  |
| total_fat_g      | Float      | Sum of fats in grams                   |
| entries_count    | Integer    | Number of entries on that day          |

---

## 6. Settings

Stores user preferences and configuration.

| Field Name       | Type       | Description                            |
|------------------|------------|----------------------------------------|
| user_id          | UUID       | Primary key (1:1 mapping to Users)     |
| units_pref       | String     | 'imperial' or 'metric'                 |
| reminder_times   | Array      | Times of day for reminder notifications|
| sync_enabled     | Boolean    | Enable sync with health platforms      |
| voice_input_lang | String     | e.g. 'en-US', 'es-ES'                  |


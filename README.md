# 🧠 CalorieAI — Intelligent Nutrition Tracker

> **Your AI-powered nutrition companion.** Scan meals, analyze ingredients, plan your diet, and track macros — all in a single, beautifully designed web app.

---

## ✨ Overview

CalorieAI is a fully client-side, single-file HTML web application that brings AI-driven nutrition tracking to your browser. It leverages the **OpenAI API** to analyze food photos, answer nutrition questions, and generate personalized meal plans — no backend or installation required.

---

## 🚀 Features

### 📸 Image Scan
Upload a photo or use your device's camera to scan any meal. CalorieAI uses OpenAI's vision model to identify food items and return a detailed breakdown of calories and macronutrients — including protein, carbs, fats, sugar, and energy (kJ).

### 🥗 Ingredient Analyzer
Manually enter a list of ingredients with quantities and get an instant AI-powered nutritional breakdown. Results are displayed as macro cards and a detailed per-ingredient table.

### 💬 AI Nutrition Chat
An interactive chat interface for asking any nutrition-related question — from "Is avocado good for weight loss?" to "How much protein should I eat post-workout?" — powered by the OpenAI Chat API.

### 📋 Personalized Meal Planner
Generate a full weekly meal plan tailored to your dietary preferences, health goals, and caloric targets. Supports dietary filters (e.g., vegetarian, vegan, keto) and activity levels.

### 📊 Daily Tracker
Log your meals throughout the day and track your running totals for calories and macros. Visualized with a hero stats strip and a history log, persisted via `localStorage`.

### 👤 User Profile & Health Snapshot
Set your personal details — age, gender, height, weight, activity level, and health goal — and CalorieAI computes your **BMI**, **BMR**, **TDEE**, and ideal macro targets automatically.

---

## 🔐 Authentication

CalorieAI includes a built-in auth system (stored in `localStorage`):

- **Sign Up / Sign In** with email and password
- Password visibility toggle and "Remember Me" support
- Secure password change flow
- Session persistence for 7 days
- Account deletion with full data wipe

> ⚠️ Note: Auth data is stored in the browser's `localStorage`. This is suitable for personal/demo use — not production-grade security.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | Pure CSS (CSS custom properties, responsive grid) |
| Logic | Vanilla JavaScript (ES6+) |
| AI | OpenAI API (`gpt-4o` vision + chat) |
| Storage | Browser `localStorage` |
| Fonts | [Syne](https://fonts.google.com/specimen/Syne) + [DM Sans](https://fonts.google.com/specimen/DM+Sans) (Google Fonts) |

---

## 📁 Project Structure

This project is intentionally a **single self-contained HTML file**:

```
CalorieAI.html
├── <head>          — Fonts, CSS variables, and all styles
├── <body>
│   ├── Auth Overlay     — Sign in / Sign up modal
│   ├── Header           — Logo + API key input
│   ├── Tab Navigation   — Image Scan, Ingredients, Chat, Meal Plan, Tracker, Profile
│   ├── Main Panels      — Tab content for each feature
│   └── <script>         — All JavaScript logic (auth, API calls, state, rendering)
```

---

## 🎨 Design Highlights

- Dark theme with animated ambient orbs and glassmorphism surfaces
- Sticky header and tab bar with smooth transitions
- Responsive layout down to mobile (≥ 320px)
- Animated scan line effect on the live camera view
- Color-coded macro cards (calories in green, protein in blue, carbs in amber, fats in orange)

---

## 🔒 Privacy

All data — meals logged, profile info, and auth credentials — stays **entirely in your browser**. Nothing is sent to any server except your food queries to the OpenAI API.

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 🙌 Contributing

Pull requests are welcome! If you find a bug or have a feature idea, feel free to open an issue.

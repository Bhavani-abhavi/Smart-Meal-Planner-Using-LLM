# Smart Meal Planner using LLM

A Streamlit app that calculates a user's daily caloric needs from basic biometrics and
generates a personalized, descriptive meal plan via a generative language model.

## How it works

- Collects name, age, weight, height, gender, and dietary restrictions (vegan,
  gluten-free, diabetic, low-carb, etc.) through a Streamlit form.
- Computes daily caloric requirement using the Mifflin-St Jeor BMR formula scaled by an
  activity factor.
- Sends a structured prompt (target calories + restrictions) to the Google Gemini API,
  requesting a 5-meal plan (breakfast, lunch, dinner, two snacks) with ingredients and a
  description for each meal.
- Displays the generated plan directly in the app.

## Stack

Python · Streamlit · Google Gemini API · Requests

## Setup

```
pip install streamlit requests
export GEMINI_API_KEY=<your-key>
streamlit run code.py
```

The API key is read from the `GEMINI_API_KEY` environment variable — set it locally
before running; never commit it to the repo.

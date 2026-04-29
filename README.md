Live Website DEMO :- https://niranjandoijode23.github.io/RESTAURANT/

# 🍽️ NiRaNjAn's ReSto — Recipe Finder

A dynamic recipe search app built with **HTML, CSS & Vanilla JavaScript**, using a **public REST API** to fetch real recipe data. Built while learning how APIs and async JavaScript work.

---

## 🌐 Live API Used

**[TheMealDB API](https://www.themealdb.com/api.php)** — A free, open REST API for recipes.

| Endpoint | Purpose |
|----------|---------|
| `/search.php?s={query}` | Search meals by name |
| `/lookup.php?i={id}` | Get full recipe details by ID |

---

## 🧠 What I Learned

- **`fetch()`** — Making HTTP GET requests to a REST API
- **`async / await`** — Handling asynchronous JavaScript cleanly
- **JSON parsing** — Reading and using API response data (`data.meals[0]`)
- **Dynamic DOM manipulation** — Building HTML cards from API data using JS
- **Event listeners** — Wiring up search, click, and keyboard interactions
- **CSS positioning & layout** — Fixed navbar, popup overlay, responsive grid

---

## ✨ Features

- 🔍 Search any recipe by name (e.g. "pasta", "sushi", "curry")
- 📋 View full ingredients + step-by-step instructions in a popup
- ▶️ YouTube video link when available
- 🌍 Shows cuisine area and category per recipe
- 📱 Responsive layout for mobile and desktop

---

## 🛠️ Built With

- HTML5
- CSS3 (Flexbox, Grid, Backdrop Filter, Animations)
- Vanilla JavaScript (Fetch API, async/await, DOM API)
- [TheMealDB REST API](https://www.themealdb.com/api.php) (free, no key required)
- Font Awesome (icons)

---

## 📁 Project Structure

```
project/
├── index.html       ← Main page structure
├── style.css        ← All styles (layout, cards, popup, responsive)
├── index.js         ← API calls, DOM rendering, event handling
└── bgimg.jpg        ← Background image
```

---

## 🚀 How to Run

1. Download or clone the project folder
2. Open `index.html` in any browser

No server or build tools needed — it runs entirely in the browser.

---

## 📖 How the API Works (Quick Reference)

```js
// Search for recipes
const res = await fetch('https://www.themealdb.com/api/json/v1/1/search.php?s=chicken');
const data = await res.json();
const meals = data.meals; // array of meal objects

// Get a specific recipe by ID
const res = await fetch('https://www.themealdb.com/api/json/v1/1/lookup.php?i=52772');
const data = await res.json();
const meal = data.meals[0]; // single meal object
```

Each meal object contains: `strMeal`, `strMealThumb`, `strInstructions`, `strIngredient1`–`strIngredient20`, `strMeasure1`–`strMeasure20`, `strYoutube`, and more.

---

## 📝 Notes

- The API is free and requires no API key for basic use
- `data.meals` returns `null` (not an empty array) when no results are found — always check before rendering
- Ingredients go up to index 20 — loop through and skip empty ones

---

*Made while learning APIs & async JS — NiRaNjAn's ReSto 🍕*
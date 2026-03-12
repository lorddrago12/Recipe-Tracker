# 🍽️ Recipe Tracker

A simple JavaScript application for managing and organizing recipes — including automatic ingredient counting and difficulty rating based on cooking time.

---

## 📋 Features

- Store recipes with ingredients and cooking times
- Automatically calculate **total ingredient count** per recipe
- Automatically assign **difficulty levels** based on cooking time:
  - 🟢 **Easy** — 30 minutes or under
  - 🟡 **Medium** — 31 to 60 minutes
  - 🔴 **Hard** — over 60 minutes
- Easily extendable recipe list

---

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine

### Installation

Clone the repository:

```bash
git clone https://github.com/lorddrago12/Recipe-Tracker.git
```

Navigate into the project directory:

```bash
cd Recipe-Tracker
```

Run the application:

```bash
node index.js
```

---

## 🗂️ Project Structure

```
Recipe-Tracker/
├── index.js       # Main application logic
└── README.md      # Project documentation
```

---

## 📦 Example Recipes

| Recipe | Ingredients | Cooking Time | Difficulty |
|---|---|---|---|
| Spaghetti Carbonara | 4 | 22 mins | Easy |
| Chicken Curry | 5 | 42 mins | Medium |
| Vegetable Stir Fry | 3 | 15 mins | Easy |

---

## 🧠 How It Works

Two core utility functions drive the logic:

```js
// Returns the number of ingredients in a recipe
function getTotalIngredients(ingredients) {
  return ingredients.length;
}

// Returns a difficulty rating based on cooking time
function getDifficultyLevel(cookingTime) {
  if (cookingTime <= 30) return "easy";
  else if (cookingTime <= 60) return "medium";
  else return "hard";
}
```

Each recipe object is updated with `totalIngredients` and `difficultyLevel` before being stored in the `recipes` array.

---

## 🛠️ Built With

- **JavaScript** (vanilla, no dependencies)
- **Node.js**

---

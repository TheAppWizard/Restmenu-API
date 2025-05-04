# 🍽️ Restores Recipe API

Welcome to the **Restores Recipe API**! This API allows you to manage a collection of recipes, including creating, retrieving, updating, and deleting them.

## 🌐 Base URL

```
{Base URL}
```

Ensure your API server is running before making requests.

---

## 📚 Endpoints & Usage

### 🔍 Get All Recipes

Fetch all available recipes.

```bash
curl -X GET {Base URL}/recipes
```

---

### 📘 Get a Specific Recipe

Retrieve a recipe by its `dish_id`.

```bash
curl -X GET {Base URL}/recipe/1
```

> Replace `1` with the appropriate `dish_id`.

---

### 📝 Create a New Recipe

Add a new recipe with a POST request.

```bash
curl -X POST {Base URL}/recipe \
  -H "Content-Type: application/json" \
  -d '{
    "dish_name": "Spaghetti Carbonara",
    "description": "Classic Italian pasta dish",
    "spice": "Mild",
    "prep_time": "15 minutes",
    "serves": 4,
    "dietry_info": "Contains dairy, eggs",
    "cook_time": "20 minutes",
    "ingredients": "400g spaghetti, 200g pancetta, 4 eggs, 100g Pecorino cheese, Black pepper",
    "instructions": "1. Cook pasta. 2. Fry pancetta. 3. Mix eggs and cheese. 4. Combine all ingredients.",
    "image_url": "https://example.com/carbonara.jpg"
  }'
```

> Be sure to replace fields with your own recipe details.

---

### ✏️ Update an Existing Recipe

Modify specific fields of an existing recipe.

```bash
curl -X PUT {Base URL}/recipe/1 \
  -H "Content-Type: application/json" \
  -d '{
    "dish_name": "Spaghetti Carbonara Deluxe",
    "description": "Upgraded classic Italian pasta dish",
    "spice": "Medium",
    "prep_time": "20 minutes"
  }'
```

> Replace `1` with the ID of the recipe you want to update. You only need to include fields you want to change.

---

### 🗑️ Delete a Recipe

Remove a recipe by ID.

```bash
curl -X DELETE {Base URL}/recipe/1
```

> Replace `1` with the ID of the recipe you want to delete.

---

### 📄 View API Documentation

Returns a simple documentation page (HTML).

```bash
curl -X GET {Base URL}
```

---

## 🔖 Data Format (JSON)

All POST and PUT requests should be sent as JSON. Here's a sample structure:

```json
{
  "dish_name": "Example Dish",
  "description": "Tasty and simple",
  "spice": "Mild",
  "prep_time": "10 minutes",
  "serves": 2,
  "dietry_info": "Vegan, Gluten-free",
  "cook_time": "15 minutes",
  "ingredients": "Example ingredients list",
  "instructions": "Step-by-step instructions",
  "image_url": "https://example.com/image.jpg"
}
```

---

## ⚠️ Notes

- Make sure your server is running on `localhost:5000`.
- All endpoints return JSON responses.
- Use proper `Content-Type: application/json` headers for POST and PUT requests.

---

## 🧾 License

This project is open for educational and demo purposes only. Feel free to customize and expand it!

---

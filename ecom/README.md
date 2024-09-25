# 🛒 E-Commerce Platform

A fully responsive e-commerce web application that allows users to browse products, add them to a shopping cart, manage cart quantities, and remove items. The app uses the **Fake Store API** for fetching product data, and the cart functionality is handled using JavaScript, providing a dynamic user experience.

This project demonstrates various front-end development techniques such as DOM manipulation, API integration, and CSS for responsive layouts.

---

## 🌟 Features
- **Product Listing**: Fetches products dynamically from the Fake Store API and displays them in a card layout.
- **Search Functionality**: Allows users to search for products by name in real-time.
- **Add to Cart**: Enables users to add products to their shopping cart and see a notification when an item is added.
- **Cart Management**: Users can increase or decrease the quantity of products in their cart or remove them entirely.
- **Responsive Design**: Layout adjusts beautifully across devices (mobile, tablet, and desktop) using CSS Grid and Flexbox.

---

## 🚀 Demo
[Demo](https://drive.google.com/file/d/1HJ-KYi98Nm9-1Vlta7WQ79JTyG9N7vt9/view?usp=sharing) 
---

## 🛠️ Tech Stack

### Frontend
- **HTML5**: Structure of the webpage.
- **CSS3**: Styling and layout (Flexbox, CSS Grid) for responsiveness.
- **JavaScript**: Core functionality for product fetching, cart management, and real-time updates.

### API
- **Fake Store API**: Provides mock data for the products.

---

## 📸 Screenshots

### Home Page (Product Listing)
[Product Listing](https://drive.google.com/file/d/1nYDXgeDHkBNODdrj4Wa0x6Ag7snjd16i/view)

### Cart Page
[Cart Page](https://drive.google.com/file/d/1ISNGEdyV7TUp5K1AEd306E0f1Q7hccMW/view?usp=sharing)

---


## 🖥️ Usage
Product Listing:

Products will be displayed when the page is loaded.
Each product card contains the product image, name, rating, price, and an "Add to Cart" button.
Search:

Use the search bar at the top to filter products by name in real-time.
Add to Cart:

Click on the "Add to Cart" button to add products to your cart.
A notification appears indicating the item has been added.
Manage Cart:

In the cart, you can increase or decrease the quantity of items using the + and - buttons.
You can also remove an item entirely by clicking the X icon next to it.
Price Details:

The total price in the cart updates automatically based on the quantity and any additional charges like shipping or platform fees

## 🔍 Search Feature
The search function allows users to filter products based on their title. It's case-insensitive and updates the product list in real-time as the user types.
```javascript
document.getElementById('search-button').addEventListener('click', () => {
    const searchTerm = document.getElementById('search-input').value.toLowerCase();
    const filteredProducts = products.filter(product => product.title.toLowerCase().includes(searchTerm));
    displayProducts(filteredProducts);
});
```
## 📡 API Reference
This project uses the Fake Store API to fetch product data. The API provides various endpoints for getting products, categories, and more.

Example Endpoint:
Products: https://fakestoreapi.com/products
For more detailed information on the API, visit the official Fake Store API Documentation.

## 🛠️ Key Functions

1)fetchProducts():
* Fetches product data from the API and displays them on the page.
* Example:
```javascript
async function fetchProducts() {
    const response = await fetch('https://fakestoreapi.com/products');
    const products = await response.json();
    displayProducts(products);
}
```
2)addToCart(product):

* Adds a product to the cart.
* Displays a notification that the item was added.
* Example:
```javascript
function addToCart(product) {
    cart.push(product);
    updateCartUI();
    alert('Item added to cart!');
}
```
3)updateCartUI():

* Updates the UI when items are added or removed from the cart.
* Example:
```javascript
function updateCartUI() {
    // Update cart items and total amount display
}
```
4)Search Functionality:
* Filters the products based on user input.
* Example:
```javascript
function searchProducts() {
    const searchTerm = document.getElementById('search-input').value.toLowerCase();
    const filteredProducts = products.filter(product => product.title.toLowerCase().includes(searchTerm));
    displayProducts(filteredProducts);
}
```
## ✨ Optimizations
Responsive Design: Ensured that the layout adapts seamlessly to mobile, tablet, and desktop screen sizes.
Performance: Added client-side caching to reduce redundant API calls (can be improved by leveraging service workers in future).
UX/UI: Improved user experience by adding notifications when items are added to the cart and aligning the cart layout for a clean interface.

## 🌱 Future Improvements
Authentication: Implement user authentication for personalized carts.
Backend Integration: Replace the Fake Store API with a real backend.
Payment Gateway: Integrate with a payment gateway like Stripe or PayPal for actual transactions.
Wishlist Feature: Allow users to add items to a wishlist.


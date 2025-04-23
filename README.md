clothing-store/
├── index.html          # Главная страница
├── catalog.html        # Страница каталога
├── product.html        # Страница товара
├── cart.html           # Страница корзины
├── checkout.html       # Страница оформления заказа
├── account.html          # Страница профиля пользователя
├── styles/
│   ├── main.scss       # Главный файл SCSS
│   ├── components/     # Папка для компонентов CSS
│   │   ├── _header.scss
│   │   ├── _footer.scss
│   │   ├── _product-card.scss
│   │   └── ...
│   └── utils/          # Папка для утилит CSS (миксины, переменные)
│       ├── _variables.scss
│       ├── _mixins.scss
│       └── ...
├── scripts/
│   ├── app.js          # Главный файл JavaScript
│   ├── modules/        # Папка для модулей JS
│   │   ├── cart.js
│   │   ├── product.js
│   │   ├── api.js       # Для работы с API (например, для получения товаров)
│   │   └── ...
├── images/             # Изображения товаров, логотипы и т.д.
└── fonts/              # Пользовательские шрифты (если используются)
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Магазин одежды</title>
    <link rel="stylesheet" href="styles/main.css">
    <link rel="icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>
    <header class="header">
        <div class="container">
            <a href="index.html" class="logo">
                <img src="">Контакты</a></li>
                </ul>
            </nav>
            <div class="header-actions">
                <a href="account.html" class="header-actions__item">
                    <img src="" alt="Account">
                </a>
                <a href="cart.html" class="header-actions__item cart-link">
                    <img src="" alt="Cart">
                    <span class="cart-count">0</span>
                </a>
            </div>
        </div>
    </header>
    <main class="main">
        <section class="hero">
            <div class="container">
                <div class="hero__content">
                    <h1 class="hero__title">Новая коллекция Осень/Зима 2024</h1>
                    <p class="hero__description">Найдите свой идеальный образ в нашей новой коллекции.</p>
                    <a href="catalog.html" class="button button--primary">Смотреть коллекцию</a>
                </div>
                <div class="hero__image">
                    <img src="" alt="Hero Image">
                </div>
            </div>
        </section>
        <section class="featured-products">
            <div class="container">
                <h2 class="section-title">Популярные товары</h2>
                <div class="product-grid">
                    <!-- Product cards will be dynamically added here -->
                </div>
                <div class="featured-products__cta">
                    <a href="catalog.html" class="button">Все товары</a>
                </div>
            </div>
        </section>
    </main>
    <footer class="footer">
        <div class="container">
            <div class="footer__top">
                <div class="footer__section">
                    <h3 class="footer__title">Информация</h3>
                    <ul class="footer__list">
                        <li><a href="about.html" class="footer__link">О нас</a></li>
                        <li><a href="delivery.html" class="footer__link">Доставка и оплата</a></li>
                        <li><a href="return.html" class="footer__link">Возврат</a></li>
                    </ul>
                </div>
                <div class="footer__section">
                    <h3 class="footer__title">Поддержка</h3>
                    <ul class="footer__list">
                        <li><a href="faq.html" class="footer__link">FAQ</a></li>
                        <li><a href="contact.html" class="footer__link">Контакты</a></li>
                    </ul>
                </div>
                <div class="footer__section">
                    <h3 class="footer__title">Подпишитесь на нас</h3>
                    <ul class="footer__social">
                        <li><a href="#" class="footer__social-link"><img src="" alt="Facebook"></a></li>
                        <li><a href="#" class="footer__social-link"><img src="" alt="Instagram"></a></li>
                        <li><a href="#" class="footer__social-link"><img src="" alt="Twitter"></a></li>
                    </ul>
                </div>
            </div>
            <div class="footer__bottom">
                <p class="footer__copyright">&copy; 2024 Магазин одежды. Все права защищены.</p>
            </div>
        </div>
    </footer>
    <script src="scripts/app.js"></script>
</body>
</html>
// 1. Import variables and functions
@import "utils/variables";
@import "utils/mixins";

// 2. Base styles
body {
    font-family: 'Roboto', sans-serif; /* Подключите шрифт через @font-face */
    margin: 0;
    padding: 0;
    background-color: $light-gray;
    color: $dark-text;
}

.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 15px;
}

a {
    text-decoration: none;
    color: inherit;
}

// 3. Import components
@import "components/header";
@import "components/footer";
@import "components/buttons";
@import "components/product-card";

// 4. Global styles (e.g., section titles, utility classes)
.section-title {
    font-size: 2.5rem;
    text-align: center;
    margin-bottom: 2rem;
}

/* =========================================================== */
/*  Hero Section                                             */
/* =========================================================== */

.hero {
    background-color: white;
    padding: 4rem 0;
    &__content {
      flex: 1;
      padding-right: 2rem;
    }
    &__title {
      font-size: 3rem;
      margin-bottom: 1rem;
    }
    &__description {
      font-size: 1.2rem;
      line-height: 1.6;
      margin-bottom: 2rem;
    }
    &__image {
      flex: 1;
      text-align: center;
    }
    &__image img {
      max-width: 100%;
      height: auto;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }
    @media (min-width: 768px) {
      display: flex;
      align-items: center;
    }
  }
  /* =========================================================== */
  /*  Featured Product Section                                            */
  /* =========================================================== */
  .featured-products{
    background-color:#f1f1f1;
    padding:50px 0;
    &__cta{
       text-align:center;
       padding:30px 0;
    }
  }
.header {
  background-color: $white;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  position: sticky;
  top: 0;
  z-index: 100;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
  }

  .logo {
    img {
      max-height: 40px;
    }
  }

  .nav {
    &__list {
      list-style: none;
      padding: 0;
      margin: 0;
      display: flex;
    }

    &__item {
      margin-left: 1.5rem;
    }

    &__link {
      font-size: 1.1rem;
      font-weight: 500;
      color: $dark-text;
      transition: color 0.2s ease;

      &:hover {
        color: $primary-color;
      }
    }
  }

  .header-actions {
    display: flex;
    align-items: center;
    &__item {
      margin-left: 1rem;
      display: flex;
      align-items: center;
      justify-content: center;
      width: 30px;
      height: 30px;
      border-radius: 50%;
      background-color: $light-gray;
      img {
        max-width: 100%;
        height: auto;
      }
      &:hover {
        background-color: darken($light-gray, 10%);
      }
    }
    .cart-link {
      position: relative;
      .cart-count {
        position: absolute;
        top: -5px;
        right: -5px;
        background-color: $primary-color;
        color: $white;
        font-size: 0.8rem;
        padding: 2px 5px;
        border-radius: 50%;
      }
    }
  }
}
// Colors
$primary-color: #007bff;
$secondary-color: #6c757d;
$success-color: #28a745;
$danger-color: #dc3545;

$dark-text: #333;
$light-text: #fff;

$light-gray: #f8f9fa;
$medium-gray: #ddd;

// Fonts
$base-font-size: 16px;
$base-line-height: 1.5;

// Breakpoints (example)
$breakpoint-small: 576px;
$breakpoint-medium: 768px;
$breakpoint-large: 992px;
$breakpoint-xlarge: 1200px;
// Example mixin for responsive media queries
@mixin media($breakpoint) {
  @if $breakpoint == small {
    @media (min-width: $breakpoint-small) { @content; }
  }
  @if $breakpoint == medium {
    @media (min-width: $breakpoint-medium) { @content; }
  }
  @if $breakpoint == large {
    @media (min-width: $breakpoint-large) { @content; }
  }
  @if $breakpoint == xlarge {
    @media (min-width: $breakpoint-xlarge) { @content; }
  }
}
import { getFeaturedProducts } from './modules/api.js'; // Example of an API module
import { updateCartCount } from './modules/cart.js'; // Example of a Cart module

document.addEventListener('DOMContentLoaded', () => {
    loadFeaturedProducts();
    updateCartCount(); // Initialize cart count on page load
});

async function loadFeaturedProducts() {
    const productGrid = document.querySelector('.product-grid');
    if (!productGrid) return; // If the element doesn't exist, exit function

    try {
        const products = await getFeaturedProducts();
        products.forEach(product => {
            const card = createProductCard(product);
            productGrid.appendChild(card);
        });
    } catch (error) {
        console.error('Error loading featured products:', error);
        productGrid.innerHTML = '<p class="error-message">Не удалось загрузить товары.</p>';
    }
}

function createProductCard(product) {
    // Create a product card element dynamically
    const card = document.createElement('div');
    card.className = 'product-card'; // Add the class name here
    card.innerHTML =  <a href="product.html?id=${product.id}" class="product-card__link">
          <img src="" alt="${product.name}" class="product-card__image">
              <h3 class="product-card__title">${product.name}</h3>
          <p class="product-card__price">Цена: ${product.price} ₽</p>
          </a>
          <button class="button button--secondary add-to-cart" data-product-id="${product.id}">В корзину</button>  return card;
  }
// Add event listeners to the add to cart buttons
document.addEventListener('click', function(event) {
    if (event.target.classList.contains('add-to-cart')) {
        const productId = event.target.dataset.productId;
        // Here, call your `addToCart` function from the `cart.js` module
        // and pass the `productId`.
        // The `addToCart` function will handle updating the cart
        // and saving the information (in `localStorage` or elsewhere).
        addToCart(productId); // Call your `addToCart` function
        updateCartCount();    // Update the cart count after adding an item
        console.log(`Товар с ID ${productId} добавлен в корзину.`);
        // Provide feedback to the user
        //alert(`Товар с ID ${productId} добавлен в корзину!`);
      }
  });
  // scripts/modules/cart.js

const CART_KEY = 'shoppingCart';

// Функция для получения содержимого корзины из localStorage
export function getCart() {
    const cartData = localStorage.getItem(CART_KEY);
    return cartData ? JSON.parse(cartData) : [];
}

// Функция для сохранения корзины в localStorage
export function saveCart(cart) {
    localStorage.setItem(CART_KEY, JSON.stringify(cart));
}

// Функция для добавления товара в корзину
export function addToCart(productId) {
    let cart = getCart();
    cart.push(productId);
    saveCart(cart);
}

// Функция для удаления товара из корзины (по индексу)
export function removeFromCart(index) {
    let cart = getCart();
    if (index >= 0 && index < cart.length) {
        cart.splice(index, 1); // Удаляем элемент по индексу
        saveCart(cart);          // Сохраняем обновлённую корзину
    }
}

// Function to calculate the total number of items in the cart
export function getCartItemCount() {
    const cart = getCart();
    return cart.length;
}

// Update the cart count in the header
export function updateCartCount() {
  const cartCountElement = document.querySelector('.cart-count');
  if (cartCountElement) {
      const itemCount = getCartItemCount();
      cartCountElement.textContent = itemCount.toString();
  }
}
// api.js
// This is a mock implementation.  In a real application, you would fetch data from a server.

const MOCK_PRODUCTS = [
    {
        id: 1,
        name: "Stylish T-Shirt",
        image: "images/product1.jpg",  // Replace with real image URL
        price: 2500,
        description: "A comfortable and stylish t-shirt for everyday wear."
    },
    {
        id: 2,
        name: "Classic Jeans",
        image: "images/product2.jpg",  // Replace with real image URL
        price: 5000,
        description: "Timeless denim jeans that never go out of style."
    },
    {
        id: 3,
        name: "Leather Jacket",
        image: "images/product3.jpg",  // Replace with real image URL
        price: 12000,
        description: "A premium leather jacket to elevate your look."
    },
];

export async function getFeaturedProducts() {
    // In a real app, you'd fetch this data from an API endpoint
    // For example:
    // const response = await fetch('/api/featured-products');
    // const data = await response.json();
    // return data;
    // Simulating a delay to mimic a real API call
    return new Promise(resolve => {
        setTimeout(() => {
            resolve(MOCK_PRODUCTS);
        }, 500);
    });
}

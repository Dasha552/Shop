магазин-одежды/
├── index.html       <!-- Главная страница -->
├── catalog.html     <!-- Страница каталога товаров -->
├── product.html     <!-- Страница товара -->
├── cart.html        <!-- Страница корзины -->
├── styles.css       <!-- Файл со стилями CSS -->
├── script.js        <!-- Файл с JavaScript кодом -->
├── images/          <!-- Папка с изображениями товаров, логотипами и т.д. -->
│   ├── product1.jpg
│   ├── logo.png
│   └── ...
└── fonts/           <!-- Папка со шрифтами (если используются) -->
    └── ...
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Магазин Одежды</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="container">
            <a href="index.html" class="logo">
                <img src="" alt="Логотип магазина">
            </a>
            <nav>
                <ul>
                    <li><a href="index.html">Главная</a></li>
                    <li><a href="catalog.html">Каталог</a></li>
                    <li><a href="cart.html">Корзина</a></li>
                </ul>
            </nav>
            <div class="cart-icon">
                <a href="cart.html">🛒 Корзина (0)</a> <!-- Пример, корзина будет обновляться через JS -->
            </div>
        </div>
    </header>
    <main>
        <section class="hero">
            <div class="container">
                <h1>Добро пожаловать в наш магазин</h1>
                <p>Большой выбор стильной одежды для вас!</p>
                <a href="catalog.html" class="button">Перейти в каталог</a>
            </div>
        </section>
        <section class="featured-products">
            <div class="container">
                <h2>Рекомендуемые товары</h2>
                <div class="product-grid">
                    <!-- Здесь будут карточки товаров, создаваемые динамически с помощью JavaScript -->
                </div>
            </div>
        </section>
    </main>
    <footer>
        <div class="container">
            <p>&copy; 2024 Магазин одежды. Все права защищены.</p>
        </div>
    </footer>
    <script src="script.js"></script>
</body>
</html>
/* Общие стили */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

.container {
    width: 80%;
    margin: 0 auto;
    padding: 20px;
}

a {
    text-decoration: none;
    color: #333;
}

.button {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border-radius: 5px;
    display: inline-block;
    margin-top: 10px;
}

/* Header */
header {
    background-color: white;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header nav ul {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
}

header nav ul li {
    margin-left: 20px;
}

/* Hero Section */
.hero {
    background-color: #eee;
    padding: 50px 0;
    text-align: center;
}

/* Featured Products (product-grid) */
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Адаптивная сетка */
    gap: 20px;
}

.product-card {
    background-color: white;
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 15px;
    text-align: center;
}

.product-card img {
    max-width: 100%;
    height: auto;
    margin-bottom: 10px;
}

/* Footer */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px 0;
}
// Пример данных о товарах (в реальном проекте данные будут браться с сервера)
const products = [
    {
        id: 1,
        name: "Футболка с принтом",
        image: "images/product1.jpg",
        price: 1200,
        description: "Классная футболка из хлопка.",
    },
    {
        id: 2,
        name: "Джинсы",
        image: "images/product2.jpg",
        price: 3500,
        description: "Удобные джинсы на каждый день.",
    },
    // Добавьте больше товаров
];

// Функция для генерации карточек товаров
function createProductCard(product) {
    const card = document.createElement("div");
    card.classList.add("product-card");

    card.innerHTML = `
        <img src="" alt="${product.name}">
        <h3>${product.name}</h3>
        <p>${product.description}</p>
        <p>${product.price} ₽</p>
        <button data-id="${product.id}" class="add-to-cart-button">В корзину</button>
    `;
    return card;
}

// Загрузка карточек товаров в секцию "Рекомендуемые товары"
const productGrid = document.querySelector(".product-grid");

if (productGrid) {
    products.forEach(product => {
        const card = createProductCard(product);
        productGrid.appendChild(card);
    });
}


// Обработчики событий (например, добавление товара в корзину)
//  Этот код будет усложняться для работы с корзиной
//  (например, сохранение в localStorage и т.д.)
const addToCartButtons = document.querySelectorAll(".add-to-cart-button");

addToCartButtons.forEach(button => {
    button.addEventListener("click", (event) => {
        const productId = event.target.dataset.id;
        // В этой функции будет логика добавления товара в корзину
        alert(`Товар с ID ${productId} добавлен в корзину!`);
    });
});
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Название товара - Магазин Одежды</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <!-- ... (код header из index.html) ... -->
    </header>
    <main>
        <section class="product-details">
            <div class="container">
                <h1>Название товара</h1>
                <div class="product-image">
                    <img src="" alt="Название товара"> <!-- Замените на правильную картинку -->
                </div>
                <div class="product-info">
                    <p>Цена: 1200 ₽</p> <!-- Замените на реальную цену -->
                    <p>Описание товара...</p>
                    <button class="add-to-cart-button">В корзину</button>
                </div>
            </div>
        </section>
    </main>
    <!-- Footer -->
    <footer>
        <!-- ... (код footer из index.html) ... -->
    </footer>
    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Каталог - Магазин Одежды</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <!-- ... (код header из index.html) ... -->
    </header>
    <main>
        <section class="catalog">
            <div class="container">
                <h2>Каталог товаров</h2>
                <div class="product-grid">
                    <!-- Здесь будут карточки товаров, создаваемые динамически с помощью JavaScript,
                         аналогично Featured Products на главной странице -->
                </div>
            </div>
        </section>
    </main>
    <!-- Footer -->
    <footer>
        <!-- ... (код footer из index.html) ... -->
    </footer>
    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Корзина - Магазин Одежды</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header -->
    <header>
        <!-- ... (код header из index.html) ... -->
    </header>
    <main>
        <section class="cart">
            <div class="container">
                <h2>Корзина</h2>
                <!-- Здесь будет отображаться содержимое корзины,
                     динамически создаваемое с помощью JavaScript -->
            </div>
        </section>
    </main>
    <!-- Footer -->
    <footer>
        <!-- ... (код footer из index.html) ... -->
    </footer>
    <script src="script.js"></script>
</body>
</html>

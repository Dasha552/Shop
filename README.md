<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Салон Маникюра и Педикюра "Nail Art"</title>
    <link rel="stylesheet" href="styles/main.css">
    <link rel="icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>
    <header class="header">
        <div class="container">
            <a href="index.html" class="logo">
                <img src="" alt="Nail Art Logo">
            </a>
            <nav class="nav">
                <ul class="nav__list">
                    <li class="nav__item"><a href="index.html" class="nav__link">Главная</a></li>
                    <li class="nav__item"><a href="services.html" class="nav__link">Услуги</a></li>
                    <li class="nav__item"><a href="portfolio.html" class="nav__link">Портфоли>
            <div class="header__cta">
                <a href="booking.html" class="button button--primary">Записаться</a>
            </div>
        </div>
    </header>
    <main class="main">
        <section class="hero">
            <div class="container">
                <div class="hero__content">
                    <h1 class="hero__title">Идеальный маникюр и педикюр для вас</h1>
                    <p class="hero__description">Мы предлагаем широкий спектр услуг по уходу за руками и ногами. Доверьте свои руки профессионалам!</p>
                    <a href="services.html" class="button button--primary">Наши услуги</a>
                </div>
                <div class="hero__image">
                    <img src="" alt="Beautiful Nails">
                </div>
            </div>
        </section>
        <section class="services">
            <div class="container">
                <h2 class="section-title">Наши услуги</h2>
                <div class="services-grid">
                    <!-- Services cards will be dynamically added here -->
                </div>
                <div class="services__cta">
                    <a href="services.html" class="button">Все услуги</a>
                </div>
            </div>
        </section>
        <section class="portfolio">
            <div class="container">
                <h2 class="section-title">Наше портфолио</h2>
                <div class="portfolio-gallery">
                    <!-- Portfolio images will be dynamically added here -->
                </div>
                <div class="portfolio__cta">
                    <a href="portfolio.html" class="button">Больше работ</a>
                </div>
            </div>
        </section>
        <section class="testimonials">
            <div class="container">
                <h2 class="section-title">Отзывы клиентов</h2>
                <div class="testimonials-slider">
                    <!-- Testimonials will be dynamically added here (using a slider library) -->
                </div>
            </div>
        </section>
    </main>
    <footer class="footer">
        <div class="container">
            <div class="footer__top">
                <div class="footer__info">
                    <img src="" alt="Nail Art Logo" class="footer__logo">
                    <p class="footer__description">Мы создаем красоту и заботимся о ваших руках и ногах с любовью и профессионализмом.</p>
                </div>
                <div class="footer__contact">
                    <h3 class="footer__title">Контактная информация</h3>
                    <p>Адрес: г. Москва, ул. Тверская, д. 10</p>
                    <p>Телефон: +7 (495) 123-45-67</p>
                    <p>Email: info@nailart.ru</p>
                </div>
                <div class="footer__social">
                    <h3 class="footer__title">Мы в социальных сетях</h3>
                    <ul class="footer__social-list">
                        <li><a href="#" class="footer__social-link"><img src="" alt="Facebook"></a></li>
                        <li><a href="#" class="footer__social-link"><img src="" alt="Instagram"></a></li>
                    </ul>
                </div>
            </div>
            <div class="footer__bottom">
                <p class="footer__copyright">&copy; 2024 Салон маникюра и педикюра "Nail Art". Все права защищены.</p>
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
    font-family: 'Arial', sans-serif; /* Замените на ваш шрифт */
    margin: 0;
    padding: 0;
    background-color: $light-gray;
    color: $dark-text;
    line-height: 1.6;
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

img {
    max-width: 100%;
    height: auto;
}

// 3. Import components
@import "components/header";
@import "components/footer";
@import "components/buttons";
@import "components/service-card";
@import "components/gallery";

// 4. Global styles (e.g., section titles, utility classes)
.section-title {
    font-size: 2.5rem;
    text-align: center;
    margin-bottom: 2rem;
    color: $primary-color;
}

/* =========================================================== */
/*  Hero Section                                             */
/* =========================================================== */
.hero {
    background-color: #f8f8f8;
    padding: 5rem 0;
    .container {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    &__content {
        flex: 1;
        padding-right: 2rem;
    }
    &__title {
        font-size: 3rem;
        margin-bottom: 1rem;
        color: $primary-color;
    }
    &__description {
        font-size: 1.2rem;
        margin-bottom: 2rem;
    }
    &__image {
        flex: 1;
        text-align: center;
    }
}

/* =========================================================== */
/*  Services Section                                          */
/* =========================================================== */

.services {
    padding: 4rem 0;
    background-color: $white;
    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); /* Адаптивная сетка */
        gap: 2rem;
        margin-bottom: 2rem;
    }
}
/* =========================================================== */
/*  Portfolio Section                                          */
/* =========================================================== */
.portfolio {
    padding: 4rem 0;
    background-color: #f9f9f9;
    .portfolio-gallery {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Адаптивная сетка */
        gap: 1rem;
        margin-bottom: 2rem;
    }
    .portfolio-image {
        overflow: hidden;
        border-radius: 5px;
        transition: transform 0.3s ease;
        &:hover {
            transform: scale(1.1);
        }
        img {
            display: block;
            width: 100%;
            height: auto;
            object-fit: cover;
        }
    }
}
// Colors
$primary-color: #e91e63;  // Яркий розовый цвет для акцентов
$secondary-color: #9c27b0; // Фиолетовый цвет для дополнительных элементов

$dark-text: #333;
$light-text: #fff;

$light-gray: #f9f9f9;
$medium-gray: #ddd;

$white: #fff;

// Fonts
$base-font-size: 16px;
$base-line-height: 1.5;

// Breakpoints (example)
$breakpoint-small: 576px;
$breakpoint-medium: 768px;
$breakpoint-large: 992px;
$breakpoint-xlarge: 1200px;
import { loadServices } from './modules/services.js';
import { loadPortfolio } from './modules/portfolio.js';
import { initBooking } from './modules/booking.js';  // Предполагается, что здесь будет код для инициализации формы бронирования

document.addEventListener('DOMContentLoaded', () => {
    loadServices();
    loadPortfolio();
    initBooking(); // Инициализация модуля для бронирования
});

// Функция для динамической загрузки карточек услуг
async function loadServices() {
    const servicesGrid = document.querySelector('.services-grid');
    if (!servicesGrid) return;  // Если элемента не существует, выходим
    try {
        const services = await getServicesData();  // Получаем данные об услугах (замените на реальный API-запрос)
        services.forEach(service => {
            const serviceCard = createServiceCard(service);
            servicesGrid.appendChild(serviceCard);
        });
    } catch (error) {
        console.error("Ошибка при загрузке списка услуг:", error);
        servicesGrid.innerHTML = "<p>Не удалось загрузить услуги.</p>"; // Обработка ошибки
    }
}

// Функция для динамической загрузки изображений портфолио
async function loadPortfolio() {
    const portfolioGallery = document.querySelector('.portfolio-gallery');
    if (!portfolioGallery) return;  // Если элемента не существует, выходим
    try {
        const portfolioItems = await getPortfolioData();  // Получаем данные о портфолио (замените на реальный API-запрос)
        portfolioItems.forEach(item => {
            const portfolioImage = createPortfolioImage(item);
            portfolioGallery.appendChild(portfolioImage);
        });
    } catch (error) {
        console.error("Ошибка при загрузке портфолио:", error);
        portfolioGallery.innerHTML = "<p>Не удалось загрузить портфолио.</p>"; // Обработка ошибки
    }
}

// Функция для создания карточки услуги
function createServiceCard(service) {
    const card = document.createElement('div');
    card.className = 'service-card';  // Задаем класс элемента
    card.innerHTML = `
        <img src="" alt="${service.name}" class="service-card__image">
        <h3 class="service-card__title">${service.name}</h3>
        <p class="service-card__description">${service.description}</p>
        <p class="service-card__price">Цена: ${service.price} ₽</p> 
    return card;
}

// Функция для создания элемента изображения в портфолио
function createPortfolioImage(item) {
    const imageContainer = document.createElement('div');
    imageContainer.className = 'portfolio-image';  // Задаем класс элемента
    imageContainer.innerHTML = `
        <img src="" alt="${item.description}">
    return imageContainer;
}

// ======================================================================
// MOCK DATA (ЗАМЕНИТЕ НА РЕАЛЬНЫЕ ЗАПРОСЫ К API)
// ======================================================================

// Пример данных об услугах (ЗАМЕНИТЕ НА РЕАЛЬНЫЙ API-ЗАПРОС)
async function getServicesData() {
    return new Promise(resolve => {
        setTimeout(() => {
            resolve([
                {
                    id: 1,
                    name: "Классический маникюр",
                    image: "images/service1.jpg",
                    description: "Уход за ногтями и придание им формы.",
                    price: 800
                },
                {
                    id: 2,
                    name: "Педикюр",
                    image: "images/service2.jpg",
                    description: "Комплексный уход за кожей стоп и ногтями.",
                    price: 1200
                },
                {
                    id: 3,
                    name: "Гель-лак",
                    image: "images/service3.jpg",
                    description: "Покрытие ногтей гель-лаком на длительный срок.",
                    price: 1500
                }
            ]);
        }, 500); // Имитация задержки при запросе к API
    });
}

// Пример данных для портфолио (ЗАМЕНИТЕ НА РЕАЛЬНЫЙ API-ЗАПРОС)
async function getPortfolioData() {
    return new Promise(resolve => {
        setTimeout(() => {
            resolve([
                {
                    id: 1,
                    image: "images/portfolio1.jpg",
                    description: "Маникюр в стиле минимализм"
                },
                {
                    id: 2,
                    image: "images/portfolio2.jpg",
                    description: "Яркий летний педикюр"
                },
                {
                    id: 3,
                    image: "images/portfolio3.jpg",
                    description: "Элегантный дизайн ногтей"
                }
            ]);
        }, 500); // Имитация задержки при запросе к API
    });
}
// modules/booking.js

export function initBooking() {
    const bookingForm = document.getElementById('booking-form');
    if (bookingForm) {
        bookingForm.addEventListener('submit', handleBookingSubmit);
    }
}

async function handleBookingSubmit(event) {
    event.preventDefault();
    const name = document.getElementById('name').value;
    const phone = document.getElementById('phone').value;
    const email = document.getElementById('email').value;
    const service = document.getElementById('service').value;
    const date = document.getElementById('date').value;
    // Здесь можно добавить валидацию данных
    const bookingData = {
        name,
        phone,
        email,
        service,
        date
    };
    try {
        const response = await sendBookingRequest(bookingData); // Отправляем запрос на сервер (имитация)
        if (response.success) {
            alert('Ваша заявка успешно отправлена! Мы свяжемся с вами в ближайшее время.');
            bookingForm.reset();  // Очищаем форму
        } else {
            alert('Ошибка при отправке заявки. Пожалуйста, попробуйте позже.');
        }
    } catch (error) {
        console.error('Ошибка при отправке запроса:', error);
        alert('Произошла ошибка. Пожалуйста, попробуйте снова.');
    }
}

// Функция имитации отправки запроса (замените на реальный API-запрос)
async function sendBookingRequest(data) {
    return new Promise(resolve => {
        setTimeout(() => {
            // Имитация успешной отправки (можно добавить логику для имитации ошибки)
            const success = Math.random() > 0.2;  // 80% вероятность успеха
            resolve({ success: success });
        }, 1000);
    });
}
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Записаться на прием - Салон маникюра</title>
    <link rel="stylesheet" href="styles/main.css">
</head>
<body>
    <header class="header">
        <!--  Header  -->
    </header>
    <main class="main">
        <section class="booking">
            <div class="container">
                <h2 class="section-title">Записаться на прием</h2>
                <form id="booking-form" class="booking-form">
                    <div class="form-group">
                        <label for="name">Ваше имя:</label>
                        <input type="text="service" required>
                            <option value="">--Выберите услугу--</option>
                            <option value="manicure">Маникюр</option>
                            <option value="pedicure">Педикюр</option>
                            <option value="gel-polish">Гель-лак</option>
                            <!-- Добавьте другие услуги -->
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="date">Выберите дату и время:</label>
                        <input type="datetime-local" id="date" name="date" required>
                    </div>
                    <button type="submit" class="button button--primary">Отправить заявку</button>
                </form>
            </div>
        </section>
    </main>
    <footer class="footer">
        <!-- Footer -->
    </footer>
    <script src="scripts/app.js"></script>
</body>
</html>

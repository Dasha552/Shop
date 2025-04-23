<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Салон Маникюра и Педикюра</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
</head>
<body>
    <header>
        <h1>Салон Маникюра и Педикюра</h1>
        <nav>
            <ul>
                <li><a href="#services">Услуги</a></li>
                <li><a href="#gallery">Галерея</a></li>
                <li><a href="#testimonials">Отзывы</a></li>
                <li><a href="#contact">Контакты</a></li>
            </ul>
        </nav>
    </header>
    <main>
        <section id="services">
            <h2>Наши Услуги</h2>
            <div class="service">
                <h3>Маникюр</h3>
                <p>Классический, аппаратный, гелевый и другие виды маникюра.</p>
                <p>Цена: от 800 ₽</p>
            </div>
            <div class="service">
                <h3>Педикюр</h3>
                <p>Классический, аппаратный, спа-педикюр и другие виды.</p>
                <p>Цена: от 1200 ₽</p>
            </div>
            <div class="service">
                <h3>Наращивание ногтей</h3>
                <p>Гелевое и акриловое наращивание ногтей.</p>
                <p>Цена: от 2000 ₽</p>
            </div>
        </section>
        <section id="gallery">
            <h2>Галерея</h2>
            <div class="gallery-images">
                <img src="nails1.jpg" alt="Маникюр">
                <img src="nails2.jpg" alt="Педикюр">
                <img src="nails3.jpg" alt="Дизайн ногтей">
                <!-- Добавьте больше изображений здесь -->
            </div>
        </section>
        <section id="testimonials">
            <h2>Отзывы</h2>
            <div class="testimonial">
                <p>"Отличный сервис и профессиональные мастера!" - Анна</p>
            </div>
            <div class="testimonial">
                <p>"Я довольна результатом, обязательно приду снова!" - Мария</p>
            </div>
            <!-- Добавьте больше отзывов здесь -->
        </section>
        <section id="contact">
            <h2>Контакты</h2>
            <p>Телефон: <a href="tel:+79000000000">+7 (900) 000-00-00</a></p>
            <p>Email: <a href="mailto:info@manicure-salon.ru">info@manicure-salon.ru</a></p>
            <p>Адрес: г. Москва, ул. Примерная, д. 1</p>
        </section>
    </main>
    <footer>
        <p>© 2023 Салон Маникюра и Педикюра. Все права защищены.</p>
        <div class="socials">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-vk"></i></a>
        </div>
    </footer>
    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

header {
    background-color: #f8c8c8;
    color: #333;
    padding: 20px;
    text-align: center;
}

nav ul {
    list-style-type: none;
    padding: 

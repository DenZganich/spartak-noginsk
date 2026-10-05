<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ЖБК «Спартак» Ногинск — Официальный сайт</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background-color: #0a0a0a;
            color: #ffffff;
            line-height: 1.6;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* NAV */
        nav {
            background: #111;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
            border-bottom: 2px solid #c8102e;
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.3rem;
            font-weight: bold;
            color: #c8102e;
            letter-spacing: 1px;
        }

        .logo span {
            color: #fff;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 25px;
        }

        nav a {
            color: #ccc;
            text-decoration: none;
            font-size: 0.95rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #c8102e;
        }

        /* HERO */
        .hero {
            background: linear-gradient(135deg, #1a0000 0%, #0a0a0a 100%);
            padding: 100px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(200, 16, 46, 0.08) 0%, transparent 60%);
        }

        .hero .container {
            position: relative;
        }

        .hero-badge {
            display: inline-block;
            background: #c8102e;
            color: #fff;
            padding: 5px 18px;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: bold;
            margin-bottom: 25px;
            letter-spacing: 1px;
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 900;
            margin-bottom: 20px;
            line-height: 1.1;
            text-transform: uppercase;
        }

        .hero h1 span {
            color: #c8102e;
        }

        .hero p {
            font-size: 1.2rem;
            color: #aaa;
            max-width: 650px;
            margin: 0 auto 35px;
        }

        .btn {
            display: inline-block;
            background: #c8102e;
            color: #fff;
            padding: 15px 40px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1rem;
            border-radius: 5px;
            transition: all 0.3s;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .btn:hover {
            background: #e01535;
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(200, 16, 46, 0.4);
        }

        .btn-outline {
            background: transparent;
            border: 2px solid #c8102e;
            color: #c8102e;
            margin-left: 15px;
        }

        .btn-outline:hover {
            background: #c8102e;
            color: #fff;
        }

        /* SECTIONS */
        section {
            padding: 80px 0;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 900;
            margin-bottom: 50px;
            text-transform: uppercase;
            position: relative;
            display: inline-block;
        }

        .section-title::after {content: '';
            position: absolute;
            bottom: -12px;
            left: 0;
            width: 60px;
            height: 4px;
            background: #c8102e;
        }

        .section-title.center {
            display: block;
            text-align: center;
        }

        .section-title.center::after {
            left: 50%;
            transform: translateX(-50%);
        }

        /* STATS */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }

        .stat-card {
            background: #111;
            border: 1px solid #222;
            border-radius: 10px;
            padding: 35px 25px;
            text-align: center;
            transition: border-color 0.3s, transform 0.3s;
        }

        .stat-card:hover {
            border-color: #c8102e;
            transform: translateY(-5px);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 900;
            color: #c8102e;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 0.95rem;
            color: #888;
        }

        /* ABOUT */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text p {
            color: #aaa;
            margin-bottom: 20px;
            font-size: 1.05rem;
        }

        .about-text .highlight {
            color: #c8102e;
            font-weight: bold;
        }

        .about-img {
            background: linear-gradient(135deg, #c8102e 0%, #7a0a1c 100%);
            border-radius: 15px;
            height: 350px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 5rem;
            font-weight: 900;
            color: rgba(255, 255, 255, 0.15);
            text-transform: uppercase;
        }

        /* ACHIEVEMENTS */
        .achievements-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .achievement-card {
            background: #111;
            border-left: 4px solid #c8102e;
            padding: 25px;
            border-radius: 0 10px 10px 0;
            transition: background 0.3s;
        }

        .achievement-card:hover {
            background: #151515;
        }

        .achievement-card h3 {
            color: #c8102e;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .achievement-card p {
            color: #999;
            font-size: 0.95rem;
        }

        /* SCHEDULE */
        .schedule-table {
            width: 100%;
            border-collapse: collapse;
            background: #111;
            border-radius: 10px;
            overflow: hidden;
        }

        .schedule-table th {
            background: #c8102e;
            padding: 15px;
            text-align: left;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .schedule-table td {
            padding: 15px;
            border-bottom: 1px solid #1a1a1a;
            font-size: 0.95rem;
            color: #bbb;
        }

        .schedule-table tr:last-child td {
            border-bottom: none;
        }

        .schedule-table tr:hover td {
            background: #151515;
            color: #fff;
        }

        .result-win {
            color: #4caf50;
            font-weight: bold;
        }

        .result-loss {
            color: #c8102e;
            font-weight: bold;
        }

        /* CONTACT */
        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info h3 {
            margin-bottom: 20px;
            font-size: 1.3rem;
        }.contact-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 20px;
        }

        .contact-icon {
            font-size: 1.5rem;
            width: 40px;
            text-align: center;
            color: #c8102e;
        }

        .contact-item p {
            color: #aaa;
            font-size: 0.95rem;
        }

        .contact-item strong {
            color: #fff;
            display: block;
            margin-bottom: 3px;
        }

        /* FORM */
        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: #ccc;
            font-size: 0.9rem;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            background: #111;
            border: 1px solid #333;
            border-radius: 5px;
            color: #fff;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: #c8102e;
        }

        .form-group textarea {
            height: 120px;
            resize: vertical;
        }

        /* FOOTER */
        footer {
            background: #050505;
            padding: 40px 0;
            text-align: center;
            border-top: 1px solid #1a1a1a;
            color: #555;
            font-size: 0.9rem;
        }

        footer .logo {
            margin-bottom: 15px;
            font-size: 1.1rem;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.2rem;
            }

            .hero p {
                font-size: 1rem;
            }

            nav ul {
                display: none;
            }

            .about-content,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .btn-outline {
                display: block;
                margin: 15px auto 0;
                text-align: center;
            }

            .section-title {
                font-size: 1.7rem;
            }

            .schedule-table {
                font-size: 0.85rem;
            }

            .schedule-table th,
            .schedule-table td {
                padding: 10px;
            }
        }
    </style>
</head>
<body>

<nav>
    <div class="container">
        <div class="logo">ЖБК <span>«СПАРТАК»</span></div>
        <ul>
            <li><a href="#about">О клубе</a></li>
            <li><a href="#achievements">Достижения</a></li>
            <li><a href="#schedule">Матчи</a></li>
            <li><a href="#contact">Контакты</a></li>
        </ul>
    </div>
</nav>

<section class="hero">
    <div class="container">
        <div class="hero-badge">Ногинск • Московская область</div>
        <h1>Женский баскетбольный клуб <span>«Спартак»</span></h1>
        <p>Легендарный клуб, основанный в 1949 году. Чемпионы СССР, обладатели Кубка Ронкетти, гордость российского баскетбола.</p>
        <a href="#about" class="btn">Узнать больше</a>
        <a href="#schedule" class="btn btn-outline">Расписание</a>
    </div>
</section>

<section id="about">
    <div class="container">
        <h2 class="section-title">О клубе</h2>
        <div class="about-content">
            <div class="about-text">
                <p>Женский баскетбольный клуб <span class="highlight">«Спартак» (Ногинск)</span> был основан в 1949 году выдающимся тренером <span class="highlight">Давидом Яковлевичем Берлиным</span>. Он оставался бессменным руководителем команды на протяжении более 70 лет.</p><p>Клуб дебютировал в высшей лиге чемпионата СССР в 1964 году и быстро стал одним из сильнейших коллективов страны. В 1978 году «Спартак» завоевал <span class="highlight">золото чемпионата СССР</span>, а в 1973 году — Кубок СССР.</p>
                <p>На международной арене команда четырежды становилась обладателем <span class="highlight">Кубка Лилиан Ронкетти</span> (Кубок Европы ФИБА) — в 1977, 1981, 1982 и 1983 годах.</p>
                <p>Сегодня «Спартак» продолжает выступать в Высшей лиге России и остаётся кузницей талантов: клуб традиционно делает ставку на собственных воспитанниц, многие из которых выступают за сборные страны.</p>
            </div>
            <div class="about-img">
                СПАРТАК<br>1949
            </div>
        </div>
    </div>
</section>

<section id="achievements" style="background: #050505;">
    <div class="container">
        <h2 class="section-title center">Достижения</h2>
        <div class="achievements-grid">
            <div class="achievement-card">
                <h3>🥇 Чемпион СССР</h3>
                <p>1978 год — золото чемпионата СССР</p>
            </div>
            <div class="achievement-card">
                <h3>🏆 Кубок СССР</h3>
                <p>1973 год — обладатель Кубка СССР</p>
            </div>
            <div class="achievement-card">
                <h3>🇪🇺 Кубок Ронкетти</h3>
                <p>4-кратный обладатель (1977, 1981, 1982, 1983)</p>
            </div>
            <div class="achievement-card">
                <h3>🥈 Чемпионат России</h3>
                <p>Неоднократный призёр Высшей лиги</p>
            </div>
            <div class="achievement-card">
                <h3>🏅 Зимние соревнования</h3>
                <p>1967 год — победитель Всесоюзных зимних соревнований</p>
            </div>
            <div class="achievement-card">
                <h3>🎓 Воспитанницы</h3>
                <p>7 золотых олимпийских медалей у воспитанниц школы</p>
            </div>
        </div>
    </div>
</section>

<section id="schedule">
    <div class="container">
        <h2 class="section-title">Матчи и результаты</h2>
        <table class="schedule-table">
            <thead>
                <tr>
                    <th>Дата</th>
                    <th>Соперник</th>
                    <th>Турнир</th>
                    <th>Результат</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>15.10.2024</td>
                    <td>«Енисей» (Красноярск)</td>
                    <td>Премьер-лига</td>
                    <td class="result-win">Победа — 72:65</td>
                </tr>
                <tr>
                    <td>22.10.2024</td>
                    <td>«Динамо» (Москва)</td>
                    <td>Премьер-лига</td>
                    <td class="result-loss">Поражение — 52:66</td>
                </tr>
                <tr>
                    <td>29.10.2024</td>
                    <td>«Надежда» (Оренбург)</td>
                    <td>Премьер-лига</td>
                    <td class="result-win">Победа — 68:60</td>
                </tr>
                <tr>
                    <td>05.11.2024</td>
                    <td>«Спартак» (Санкт-Петербург)</td>
                    <td>Кубок России</td>
                    <td class="result-win">Победа — 81:74</td>
                </tr>
            </tbody>
        </table>
    </div>
</section>

<section id="contact" style="background: #050505;">
    <div class="container">
        <h2 class="section-title">Контакты</h2>
        <div class="contact-grid">
            <div class="contact-info">
                <h3>Свяжитесь с нами</h3>
                <div class="contact-item">
                    <div class="contact-icon">📍</div>
                    <div>
                        <strong>Адрес</strong>
                        <p>Московская область, г. Ногинск, спортивно-оздоровительный комплекс «Знамя»</p></div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">📞</div>
                    <div>
                        <strong>Телефон</strong>
                        <p>+7 (XXX) XXX-XX-XX</p>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">✉️</div>
                    <div>
                        <strong>Email</strong>
                        <p>info@spartak-noginsk.ru</p>
                    </div>
                </div>
                <div class="contact-item">
                    <div class="contact-icon">🌐</div>
                    <div>
                        <strong>Официальный сайт</strong>
                        <p>spartaknoginsk.ucoz.com</p>
                    </div>
                </div>
            </div>
            <div>
                <form onsubmit="event.preventDefault(); alert('Спасибо! Мы свяжемся с вами.');">
                    <div class="form-group">
                        <label>Ваше имя</label>
                        <input type="text" placeholder="Иван Иванов" required>
                    </div>
                    <div class="form-group">
                        <label>Email</label>
                        <input type="email" placeholder="ivan@example.com" required>
                    </div>
                    <div class="form-group">
                        <label>Сообщение</label>
                        <textarea placeholder="Ваш вопрос или предложение..."></textarea>
                    </div>
                    <button type="submit" class="btn" style="border: none; cursor: pointer; width: 100%;">Отправить</button>
                </form>
            </div>
        </div>
    </div>
</section>

<footer>
    <div class="container">
        <div class="logo">ЖБК <span>«СПАРТАК»</span> Ногинск</div>
        <p>© 1949–2026 Женский баскетбольный клуб «Спартак» (Ногинск). Все права защищены.</p>
        <p style="margin-top: 10px; font-size: 0.8rem; color: #333;">Создано с уважением к истории клуба</p>
    </div>
</footer>

</body>
</html>
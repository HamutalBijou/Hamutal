# Hamutal
hamutal/
│
├── index.html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hamutal</title>
    <link rel="stylesheet" href="style.css">
    <!-- Íconos minimalistas -->
    <script src="https://unpkg.com/feather-icons"></script>
</head>
<body>

    <!-- Barra superior -->
    <header>
        <div class="logo">Hamutal</div>
        <div class="menu-icon" onclick="toggleMenu()">&#9776;</div>
        <nav id="menu">
            <a href="#">Anillos</a>
            <a href="#">Pulseras</a>
            <a href="#">Collares</a>
            <a href="#">Pañuelos</a>
            <a href="#">Broches</a>
            <a href="#">Bolsitos</a>
            <a href="#">Colitas</a>
        </nav>
    </header>

    <!-- Barra de iconos -->
    <div class="icon-bar">
        <a href="index.html"><i data-feather="home"></i></a>
        <a href="pages/historia.html"><i data-feather="clock"></i></a>
        <a href="pages/promociones.html"><i data-feather="percent"></i></a>
        <a href="pages/usos.html"><i data-feather="star"></i></a>
    </div>

    <!-- Carrusel -->
    <section class="carousel">
        <div class="slides">
            <img src="img/banner1.jpg" alt="Promoción 1">
            <img src="img/banner2.jpg" alt="Promoción 2">
            <img src="img/banner3.jpg" alt="Promoción 3">
        </div>
    </section>

    <!-- Productos destacados -->
    <section class="productos">
        <h2>Destacados de la semana</h2>
        <div class="grid">
            <!-- Cambiar imagen, título y precio -->
            <div class="producto">
                <img src="img/producto1.jpg" alt="">
                <h3>Anillo Aurora</h3>
                <p>$2500</p>
            </div>
            <div class="producto">
                <img src="img/producto2.jpg" alt="">
                <h3>Pulsera Raíz</h3>
                <p>$1800</p>
            </div>
            <div class="producto">
                <img src="img/producto3.jpg" alt="">
                <h3>Collar Bruma</h3>
                <p>$3000</p>
            </div>
            <div class="producto">
                <img src="img/producto4.jpg" alt="">
                <h3>Pañuelo Seda</h3>
                <p>$4500</p>
            </div>
            <div class="producto">
                <img src="img/producto5.jpg" alt="">
                <h3>Broche Floral</h3>
                <p>$1200</p>
            </div>
            <div class="producto">
                <img src="img/producto6.jpg" alt="">
                <h3>Bolsito Mimbre</h3>
                <p>$5000</p>
            </div>
        </div>
    </section>

    <script src="script.js"></script>
    <script>
        feather.replace()
    </script>
</body>
</html>

├── style.css
/* Paleta de colores */
:root {
    --orchid: #CB438B;
    --crimson: #BF3556;
    --mossy: #6C6A43;
    --mulberry: #4D3449;
    --pearl: #FFF0D2;
}

/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', sans-serif;
}

body {
    background-color: var(--pearl);
    color: var(--mulberry);
}

/* Barra superior */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: var(--orchid);
    color: white;
    padding: 10px 20px;
    position: sticky;
    top: 0;
    z-index: 10;
}

.logo {
    font-size: 1.5em;
    font-weight: bold;
}

.menu-icon {
    font-size: 1.5em;
    cursor: pointer;
}

nav {
    display: none;
    flex-direction: column;
    background-color: var(--orchid);
    position: absolute;
    top: 50px;
    right: 20px;
}

nav a {
    color: white;
    padding: 10px;
    text-decoration: none;
}

nav a:hover {
    background-color: var(--crimson);
}

/* Barra de iconos */
.icon-bar {
    display: flex;
    justify-content: space-around;
    background: var(--mossy);
    padding: 10px;
}

.icon-bar a {
    color: white;
}

/* Carrusel */
.carousel {
    width: 100%;
    overflow: hidden;
}

.slides {
    display: flex;
    animation: slide 12s infinite;
}

.slides img {
    width: 100%;
}

@keyframes slide {
    0% { transform: translateX(0%); }
    33% { transform: translateX(-100%); }
    66% { transform: translateX(-200%); }
    100% { transform: translateX(0%); }
}

/* Productos */
.productos {
    padding: 20px;
}

.grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 15px;
}

.producto {
    background: white;
    padding: 10px;
    border-radius: 5px;
    text-align: center;
}

.producto img {
    max-width: 100%;
    border-radius: 5px;
}

├── script.js
│function toggleMenu() {
    const menu = document.getElementById("menu");
    menu.style.display = menu.style.display === "flex" ? "none" : "flex";
}

├── img/
│   ├── banner1.jpg
│   ├── banner2.jpg
│   ├── producto1.jpg
│   └── ...
│
└── pages/
    ├── historia.html
    ├── promociones.html
    ├── usos.html
    └── producto.html

© 2025 Agostina Humhofe - Hamutal 
Todos los derechos reservados. 
No se permite la copia ni distribución del contenido sin autorización expresa.

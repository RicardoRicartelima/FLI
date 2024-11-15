<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FLI - Locação de Motos</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* Resetando margens e paddings */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        /* Corpo */
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f9f9f9;
            color: #333;
            line-height: 1.6;
        }

        /* Cabeçalho */
        header {
            background-color: #FE8500; /* Laranja */
            padding: 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        }

        header .logo img {
            height: 80px;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 30px;
        }

        nav ul li {
            display: inline;
        }

        nav ul li a {
            text-decoration: none;
            color: #fff;
            font-weight: 600;
            font-size: 16px;
            transition: color 0.3s ease;
        }

        nav ul li a:hover {
            color: #000;
        }

        /* Seção Hero */
        .hero {
            text-align: center;
            padding: 80px 20px;
            background-color: #333; /* Preto */
            color: #fff;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 30px;
        }

        .hero button {
            background-color: #FF6600; /* Laranja */
            border: none;
            padding: 15px 40px;
            color: #fff;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background-color 0.3s;
            text-transform: uppercase;
        }

        .hero button:hover {
            background-color: #e65c00;
        }

        /* Seção Explicativa */
        .exp {
            padding: 50px 20px;
            text-align: center;
            background-color: #fff;
        }

        .exp h1 {
            font-size: 2.5rem;
            color: #FE8500;
            margin-bottom: 20px;
        }

        .exp1 {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #555;
        }

        .highlight {
            background-color: #FE8500;
            color: #fff;
            padding: 15px;
            font-weight: bold;
            margin: 20px 0;
            border-radius: 5px;
        }

        ul {
            text-align: left;
            max-width: 600px;
            margin: 0 auto;
            padding-left: 20px;
        }

        li {
            font-size: 1.1rem;
            margin-bottom: 10px;
        }

        .value {
            font-weight: bold;
            color: #FF6600;
        }

        /* Seção de Motos */
        .motos {
            padding: 50px 20px;
            background-color: #f4f4f4;
            text-align: center;
        }

        .motos h2 {
            font-size: 2.5rem;
            margin-bottom: 40px;
            color: #333;
        }

        .moto-cards {
            display: flex;
            justify-content: center;
            gap: 20px;
            flex-wrap: wrap;
            margin-top: 40px;
        }

        .card {
            background-color: #fff;
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            width: 280px;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .card img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            transition: transform 0.3s ease;
        }

        .card h3 {
            margin-top: 15px;
            font-size: 1.8rem;
        }

        .card p {
            font-size: 1.2rem;
            margin: 10px 0;
        }

        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0, 0, 0, 0.15);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            overflow: auto;
            padding-top: 60px;
        }

        .modal-content {
            background-color: #fff;
            margin: 5% auto;
            padding: 30px;
            border: 1px solid #888;
            width: 80%;
            max-width: 600px;
            text-align: center;
            border-radius: 10px;
        }

        .close {
            color: #aaa;
            font-size: 28px;
            font-weight: bold;
            position: absolute;
            top: 10px;
            right: 20px;
            transition: color 0.3s;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }

        button {
            background-color: #FF6600; /* Laranja */
            border: none;
            padding: 10px 20px;
            color: #fff;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s;
            text-transform: uppercase;
            margin-top: 20px;
        }

        button:hover {
            background-color: #e65c00;
        }

        /* Rodapé */
        footer {
            background-color: #333;
            color: #fff;
            text-align: center;
            padding: 20px;
        }

        footer p {
            font-size: 1rem;
        }

        /* Media Queries para Responsividade */
        @media (max-width: 768px) {
            nav ul {
                display: flex;
                flex-direction: column;
                gap: 10px;
                text-align: center;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.2rem;
            }

            .moto-cards {
                flex-direction: column;
            }

            .card {
                width: 100%;
                margin-bottom: 20px;
            }
        }
    </style>
</head>

<body>

    <header>
        <div class="logo">
            <img src="ft/LGG.png" alt="FLI">
        </div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="https://www.instagram.com/p/C9D41iIu_qv/">Locação</a></li>
                <li><a href="https://www.instagram.com/p/C9D4zzpOkm4/">Sobre</a></li>
                <li><a href="https://w.app/U1MsBN">Contato</a></li>
            </ul>
        </nav>
    </header>

    <!-- Seção principal -->
    <section class="hero">
        <h1>Alugue sua moto com a FLI</h1>
        <p>Venha viver a liberdade sobre duas rodas! Faça sua reserva online e escolha a moto ideal para sua jornada.</p>
        <button onclick="openModal()"><a href="https://w.app/U1MsBN" style="color: #fff; text-decoration: none;">Reserve agora</a></button>
    </section>

    <!-- Seção Explicativa -->
    <div class="exp">
        <h1>Locação de Motos FLI</h1>
        <p class="exp1">Seja bem-vindo à FLI! Oferecemos motos novas e seminovas para locação, ideais para quem busca praticidade, liberdade e economia. Confira os detalhes abaixo:</p>
        <h2>Valores de Locação</h2>
        <ul>
            <li><strong>Valor Caução:</strong> <span class="value">R$ 700,00</span> (reembolsável ao final do período de locação)</li>
            <li><strong>Valor Semanal:</strong> <span class="value">R$ 350,00</span> por semana</li>
        </ul>
        <p class="exp1">As motos disponíveis para locação são novas e seminovas, garantindo alta qualidade e segurança.</p>
    </div>

    <!-- Seção de Motos -->
    <section class="motos">
        <h2>Motos Disponíveis</h2>
        <div class="moto-cards">
            <div class="card" onclick="showMotoDetails('Moto 1', 'R$ 100/dia', 'Moto 1 é ideal para quem busca conforto e praticidade.')">
                <img src="assets/images/moto1.jpg" alt="Moto 1">
                <h3>Moto 1</h3>
                <p>R$ 350,00/semana</p>
            </div>
            <div class="card" onclick="showMotoDetails('Moto 2', 'R$ 120/dia', 'Moto 2 é perfeita para aventuras urbanas.')">
                <img src="assets/images/moto2.jpg" alt="Moto 2">
                <h3>Moto 2</h3>
                <p>R$ 350,00/semana</p>
            </div>
            <div class="card" onclick="showMotoDetails('Moto 3', 'R$ 150/dia', 'Moto 3 oferece uma experiência de pilotagem única.')">
                <img src="assets/images/moto3.jpg" alt="Moto 3">
                <h3>Moto 3</h3>
                <p>R$ 350,00/semana</p>
            </div>
        </div>
    </section>

    <!-- Modal -->
    <div id="motoModal" class="modal">
        <div class="modal-content">
            <span class="close" onclick="closeModal()">&times;</span>
            <h3 id="modalTitle"></h3>
            <p id="modalDescription"></p>
            <p id="modalPrice"></p>
            <button onclick="openModal()">Reservar</button>
        </div>
    </div>

    <!-- Rodapé -->
    <footer>
        <p>&copy; 2024 FLI Locação de Motos. Todos os direitos reservados.</p>
    </footer>

</body>

</html>


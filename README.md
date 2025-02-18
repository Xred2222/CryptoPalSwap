<!DOCTYPE html>
<html lang="pl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Crypto Exchange - Wymiana na PayPal</title>
    <link rel="stylesheet" href="styles.css">
    <script defer src="script.js"></script>
</head>
<body>
    <header>
        <h1>Crypto Exchange</h1>
        <p>Wymień kryptowaluty na środki PayPal szybko i bezpiecznie</p>
    </header>
    
    <section class="exchange-form">
        <h2>Formularz wymiany</h2>
        <form id="exchangeForm">
            <label for="crypto">Wybierz kryptowalutę:</label>
            <select id="crypto" required>
                <option value="BTC">Bitcoin (BTC)</option>
                <option value="ETH">Ethereum (ETH)</option>
                <option value="USDT">Tether (USDT)</option>
            </select>

            <label for="amount">Ilość:</label>
            <input type="number" id="amount" placeholder="Podaj ilość" required>

            <label for="paypal">Twój email PayPal:</label>
            <input type="email" id="paypal" placeholder="example@email.com" required>

            <button type="submit">Wymień</button>
        </form>
        <p id="responseMessage"></p>
    </section>

    <footer>
        <p>&copy; 2025 Crypto Exchange - Wszystkie prawa zastrzeżone.</p>
    </footer>
</body>
</html>

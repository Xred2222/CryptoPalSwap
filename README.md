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
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    text-align: center;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
}

.exchange-form {
    background: white;
    padding: 20px;
    max-width: 400px;
    margin: 20px auto;
    border-radius: 5px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

form {
    display: flex;
    flex-direction: column;
}

label, input, select, button {
    margin: 10px 0;
    padding: 10px;
    width: 100%;
}

button {
    background-color: #28a745;
    color: white;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #218838;
}

footer {
    margin-top: 20px;
    padding: 10px;
    background: #333;
    color: white;
}document.getElementById("exchangeForm").addEventListener("submit", function(event) {
    event.preventDefault();

    let crypto = document.getElementById("crypto").value;
    let amount = document.getElementById("amount").value;
    let paypalEmail = document.getElementById("paypal").value;

    if (amount <= 0) {
        alert("Podaj poprawną ilość kryptowaluty.");
        return;
    }

    document.getElementById("responseMessage").innerText = 
        `Zlecenie wymiany ${amount} ${crypto} na PayPal: ${paypalEmail} zostało przesłane. Oczekuj potwierdzenia.`;
});

<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Jogo Adivinhe o Número</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f8ff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        h1 {
            color: #333;
        }
        input[type="number"] {
            padding: 10px;
            font-size: 16px;
            width: 100px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            margin-left: 10px;
            cursor: pointer;
        }
        p {
            font-size: 18px;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Jogo Adivinhe o Número</h1>
    <p>Tente adivinhar um número entre 1 e 100.</p>
    <input type="number" id="palpite" min="1" max="100" />
    <button onclick="verificar()">Enviar</button>
    <p id="resultado"></p>

    <script>
        const numeroSecreto = Math.floor(Math.random() * 100) + 1;
        let tentativas = 0;

        function verificar() {
            const palpiteInput = document.getElementById('palpite');
            const resultado = document.getElementById('resultado');
            const palpite = Number(palpiteInput.value);

            if (isNaN(palpite) || palpite < 1 || palpite > 100) {
                resultado.textContent = 'Por favor, insira um número válido entre 1 e 100.';
                return;
            }

            tentativas++;

            if (palpite === numeroSecreto) {
                resultado.textContent = `Parabéns! Você acertou em ${tentativas} tentativa(s)!`;
                // Opcionalmente, reiniciar o jogo
                // location.reload();
            } else if (palpite < numeroSecreto) {
                resultado.textContent = 'Tente um número maior.';
            } else {
                resultado.textContent = 'Tente um número menor.';
            }

            palpiteInput.value = '';
            palpiteInput.focus();
        }
    </script>
</body>
</html>

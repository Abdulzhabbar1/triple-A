<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Доступ к Arduino</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #1e1e1e;
            color: #ddd;
            text-align: center;
            padding: 50px;
        }

        .container {
            background: #2c2c2c;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.5);
            width: 350px;
            margin: auto;
        }

        h2 {
            font-size: 20px;
            font-weight: bold;
            color: #f0f0f0;
        }

        input {
            padding: 12px;
            border: 2px solid #444;
            border-radius: 5px;
            width: 80%;
            background: #333;
            color: white;
            font-size: 16px;
            text-align: center;
            margin-bottom: 15px;
        }

        button {
            background: #ff4500;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.3s;
        }

        button:hover {
            background: #cc3700;
        }

        #connect {
            background: #007acc;
        }

        #connect:hover {
            background: #005f99;
        }

        .message {
            font-size: 18px;
            font-weight: bold;
            margin-top: 15px;
            color: #ffcc00;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>🔒 Введите пароль:</h2>
        <input type="password" id="password">
        <button id="submit">🔑 Отправить</button>
        <br><br>
        <button id="connect">🔗 Подключиться к Arduino</button>
        <div class="message" id="message"></div>
    </div>

    <script>
        let bluetoothDevice;
        let characteristic;

        document.getElementById("connect").addEventListener("click", async () => {
            try {
                bluetoothDevice = await navigator.bluetooth.requestDevice({
                    acceptAllDevices: true,
                    optionalServices: ['0000ffe0-0000-1000-8000-00805f9b34fb']
                });

                const server = await bluetoothDevice.gatt.connect();
                const service = await server.getPrimaryService('0000ffe0-0000-1000-8000-00805f9b34fb');
                characteristic = await service.getCharacteristic('0000ffe1-0000-1000-8000-00805f9b34fb');

                document.getElementById("message").innerText = "✅ Подключено!";
            } catch (error) {
                document.getElementById("message").innerText = "❌ Ошибка подключения!";
            }
        });

        document.getElementById("submit").addEventListener("click", async () => {
            let password = document.getElementById("password").value;
            let messageDiv = document.getElementById("message");

            if (password === "triple a") {
                messageDiv.innerText = "🔓 Пароль верный! Отключаем датчик...";
                if (characteristic) {
                    const encoder = new TextEncoder();
                    await characteristic.writeValue(encoder.encode("OFF"));
                }
            } else {
                messageDiv.innerText = "🚫 Неправильный пароль!";
            }
        });
    </script>
</body>
</html>

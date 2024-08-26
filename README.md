<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gerçekçi Slot Oyunu</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #222;
            color: #fff;
            margin-top: 50px;
        }
        #slot-makinesi {
            display: flex;
            justify-content: center;
            margin-top: 50px;
        }
        .slot {
            width: 100px;
            height: 100px;
            border: 2px solid #555;
            margin: 0 10px;
            font-size: 2em;
            display: flex;
            justify-content: center;
            align-items: center;
            background-color: #333;
        }
        button {
            padding: 10px 20px;
            font-size: 1.5em;
            cursor: pointer;
            background-color: #ff5722;
            color: #fff;
            border: none;
            margin-top: 20px;
        }
        #sonuc {
            font-size: 2em;
            margin-top: 20px;
            color: #00e676;
        }
    </style>
</head>
<body>
    <h1>Gerçekçi Slot Oyunu</h1>
    <div id="slot-makinesi">
        <div class="slot" id="slot1">?</div>
        <div class="slot" id="slot2">?</div>
        <div class="slot" id="slot3">?</div>
    </div>
    <button onclick="slotOyna()">Spin!</button>
    <div id="sonuc"></div>

    <script>
        function slotOyna() {
            const semboller = ['🍒', '🍋', '🔔', '💎', '7️⃣'];
            const slot1 = semboller[Math.floor(Math.random() * semboller.length)];
            const slot2 = semboller[Math.floor(Math.random() * semboller.length)];
            const slot3 = semboller[Math.floor(Math.random() * semboller.length)];

            document.getElementById("slot1").textContent = slot1;
            document.getElementById("slot2").textContent = slot2;
            document.getElementById("slot3").textContent = slot3;

            if (slot1 === slot2 && slot2 === slot3) {
                document.getElementById("sonuc").textContent = "Büyük İkramiye!";
                document.getElementById("sonuc").style.color = "#ffeb3b";
            } else {
                document.getElementById("sonuc").textContent = "Şansınızı tekrar deneyin!";
                document.getElementById("sonuc").style.color = "#e91e63";
            }
        }
    </script>
</body>
</html>

# surprise
Сайт-сюрприз
<!DOCTYPE html>
<html>
<head>
    <title>Для тебя 💖</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #667eea, #764ba2);
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0;
        }
        .container {
            background: white;
            padding: 40px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            max-width: 500px;
            width: 90%;
        }
        button {
            background: #ff6b6b;
            color: white;
            border: none;
            padding: 15px 30px;
            margin: 10px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 16px;
            transition: transform 0.3s ease;
        }
        button:hover {
            transform: scale(1.05);
        }
        .message {
            display: none;
            margin-top: 20px;
            padding: 20px;
            background: #f8f9fa;
            border-radius: 10px;
            animation: fadeIn 0.5s ease;
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .emoji {
            font-size: 2em;
            margin: 10px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Для моей замечательной подруги! 💕</h1>
        <p>Ты самая лучшая! Помни это! ✨</p>
        
        <div class="emoji">🌷🌸💐</div>
        
        <button onclick="showRandomMessage()">
            Нажми для приятных слов! 💫
        </button>
        
        <button onclick="showCompliment()">
            Случайный комплимент 🌟
        </button>
        
        <div id="message" class="message">
            <h2 id="messageTitle"></h2>
            <p id="messageText"></p>
            <div class="emoji" id="messageEmoji"></div>
        </div>
    </div>

    <script>
        const messages = [
            {
                title: "Ты заслуживаешь счастья!",
                text: "Спасибо, что ты есть в моей жизни! Ты делаешь её ярче и интереснее.",
                emoji: "🌈💖"
            },
            {
                title: "Ты сильнее, чем думаешь!",
                text: "Помни: даже в трудные дни ты справляешься лучше, чем можешь представить.",
                emoji: "💪✨"
            },
            {
                title: "Твоя улыбка — это солнце!",
                text: "Когда ты улыбаешься, мир становится светлее и добрее.",
                emoji: "😊☀️"
            },
            {
                title: "Ты уникальна и особенная!",
                text: "Нет никого похожего на тебя, и в этом твоя суперсила!",
                emoji: "🦄⭐"
            },
            {
                title: "Ты делаешь всё идеально!",
                text: "Не сомневайся в себе — ты поступаешь правильно в любой ситуации.",
                emoji: "🎯💫"
            },
            {
                title: "Ты — источник вдохновения!",
                text: "Твоя энергия и доброта вдохновляют окружающих на хорошие поступки.",
                emoji: "🔥❤️"
            },
            {
                title: "Сегодня твой день!",
                text: "Пусть сегодня случится что-то волшебное и прекрасное именно для тебя!",
                emoji: "🎉🎁"
            }
        ];

        const compliments = [
            "Ты излучаешь доброту и тепло! 🌟",
            "С тобой так приятно проводить время! 💕",
            "У тебя прекрасное чувство юмора! 😄",
            "Ты очень мудрый человек! 🦉",
            "Твоя улыбка заразительна! 😊",
	    "Ты делаешь мир лучше просто своим присутствием! 🌍",
            "С тобой можно быть собой — это бесценно! 💫",
            "Ты вдохновляешь меня каждый день! 🎨",
            "У тебя золотое сердце! 💛",
            "Ты прекрасно справляешься с любыми трудностями! 🌈",
            "Ты невероятно креативна! 🎭",
            "Твоя поддержка значит так много! 🤗",
            "Ты прекрасный друг! 👭",
            "Твоя энергия заряжает позитивом! ⚡",
            "Ты выглядишь потрясающе сегодня! 💃"
        ];

        function showRandomMessage() {
            const randomIndex = Math.floor(Math.random() * messages.length);
            const message = messages[randomIndex];
            
            document.getElementById('messageTitle').textContent = message.title;
            document.getElementById('messageText').textContent = message.text;
            document.getElementById('messageEmoji').textContent = message.emoji;
            document.getElementById('message').style.display = 'block';
        }

        function showCompliment() {
            const randomCompliment = compliments[Math.floor(Math.random() * compliments.length)];
            
            document.getElementById('messageTitle').textContent = "Просто хочу сказать...";
            document.getElementById('messageText').textContent = randomCompliment;
            document.getElementById('messageEmoji').textContent = "💝";
            document.getElementById('message').style.display = 'block';
        }
    </script>
</body>
</html>

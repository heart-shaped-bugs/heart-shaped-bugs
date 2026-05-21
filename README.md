<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Приветствие с Go</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #e9edf2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Segoe UI', 'Inter', system-ui, -apple-system, 'Roboto', sans-serif;
            padding: 1rem;
        }

        .greeting-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(2px);
            border-radius: 2.5rem;
            padding: 2rem 3rem;
            display: inline-flex;
            align-items: center;
            gap: 1.5rem;
            box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.2),
                        0 1px 2px rgba(0, 0, 0, 0.05);
            transition: transform 0.25s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.5);
        }

        .greeting-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 28px 40px -16px rgba(0, 0, 0, 0.25);
        }

        .go-icon {
            width: 50px;
            height: 50px;
            filter: drop-shadow(0 4px 6px rgba(0, 100, 200, 0.2));
            transition: transform 0.2s ease;
        }

        .greeting-card:hover .go-icon {
            transform: scale(1.05) rotate(2deg);
        }

        .greeting-text {
            font-size: 2rem;
            font-weight: 600;
            background: linear-gradient(135deg, #1e2b3c, #00acd7);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            letter-spacing: -0.01em;
            border-left: 3px solid #00acd7;
            padding-left: 1.2rem;
            line-height: 1.2;
        }

        /* Адаптация для маленьких экранов */
        @media (max-width: 550px) {
            .greeting-card {
                padding: 1.2rem 1.8rem;
                gap: 1rem;
                border-radius: 2rem;
            }
            .greeting-text {
                font-size: 1.4rem;
                padding-left: 0.8rem;
            }
            .go-icon {
                width: 40px;
                height: 40px;
            }
        }

        /* Опционально: легкая пульсация при загрузке */
        @keyframes softAppear {
            from {
                opacity: 0;
                transform: scale(0.96);
            }
            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        .greeting-card {
            animation: softAppear 0.4s cubic-bezier(0.2, 0.9, 0.4, 1.1);
        }
    </style>
</head>
<body>
    <div class="greeting-card">
        <img class="go-icon" 
             src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/go/go-original.svg" 
             alt="Go language logo"
             width="50" 
             height="50">
        <div class="greeting-text">
            Hallo zusammen
        </div>
    </div>
</body>
</html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Teacher's Day - Sir Randy Bello</title>

    <style>
        /* =========================
           GENERAL
        ========================== */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            min-height: 100vh;
            font-family: "Segoe UI", Arial, sans-serif;
            background: linear-gradient(135deg, #dff6ff, #b9eaff, #eafaff);
            color: #16445c;
            overflow-x: hidden;
            transition: background 0.6s ease, color 0.6s ease;
        }

        /* =========================
           DARK MODE
        ========================== */
        body.dark {
            background: linear-gradient(135deg, #071c2b, #0d3044, #102f42);
            color: #e8f8ff;
        }

        /* =========================
           TOP BAR
        ========================== */
        .top-bar {
            position: fixed;
            top: 20px;
            right: 25px;
            z-index: 1000;
        }

        .theme-btn {
            border: none;
            padding: 12px 18px;
            border-radius: 30px;
            background: rgba(255,255,255,0.8);
            color: #16749d;
            font-size: 14px;
            font-weight: bold;
            cursor: pointer;
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
            transition: all 0.3s ease;
        }

        .theme-btn:hover {
            transform: scale(1.08);
        }

        body.dark .theme-btn {
            background: #173d51;
            color: #aee9ff;
        }

        /* =========================
           BALLOONS
        ========================== */
        .balloon-container {
            position: fixed;
            inset: 0;
            overflow: hidden;
            pointer-events: none;
            z-index: 0;
        }

        .balloon {
            position: absolute;
            bottom: -160px;
            width: 55px;
            height: 70px;
            border-radius: 50% 50% 45% 45%;
            opacity: 0.75;
            animation: floatUp linear infinite;
        }

        .balloon::before {
            content: "";
            position: absolute;
            width: 2px;
            height: 100px;
            background: rgba(70, 100, 110, 0.5);
            top: 65px;
            left: 50%;
        }

        .balloon::after {
            content: "";
            position: absolute;
            bottom: -6px;
            left: 23px;
            border-left: 5px solid transparent;
            border-right: 5px solid transparent;
            border-top: 8px solid currentColor;
        }

        .b1 {
            left: 5%;
            background: #8edfff;
            color: #8edfff;
            animation-duration: 14s;
        }

        .b2 {
            left: 18%;
            background: #b4e9ff;
            color: #b4e9ff;
            animation-duration: 18s;
            animation-delay: 2s;
        }

        .b3 {
            left: 35%;
            background: #6ec8f0;
            color: #6ec8f0;
            animation-duration: 16s;
            animation-delay: 4s;
        }

        .b4 {
            left: 55%;
            background: #a4ddff;
            color: #a4ddff;
            animation-duration: 20s;
            animation-delay: 1s;
        }

        .b5 {
            left: 72%;
            background: #74c8ee;
            color: #74c8ee;
            animation-duration: 15s;
            animation-delay: 5s;
        }

        .b6 {
            left: 88%;
            background: #c4efff;
            color: #c4efff;
            animation-duration: 19s;
            animation-delay: 3s;
        }

        @keyframes floatUp {
            0% {
                transform: translateY(0) rotate(-5deg);
            }

            50% {
                transform: translateY(-55vh) rotate(7deg);
            }

            100% {
                transform: translateY(-120vh) rotate(-5deg);
            }
        }

        /* =========================
           MAIN
        ========================== */
        .page {
            position: relative;
            z-index: 2;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 70px 20px;
        }

        /* =========================
           ENVELOPE
        ========================== */
        .envelope-wrapper {
            width: min(430px, 95vw);
            text-align: center;
            transition: all 0.7s ease;
        }

        .envelope {
            position: relative;
            width: 100%;
            height: 270px;
            background: #8ed9f5;
            border-radius: 12px;
            box-shadow: 0 25px 60px rgba(27, 110, 145, 0.3);
            cursor: pointer;
            overflow: hidden;
            transition: transform 0.5s ease;
        }

        .envelope:hover {
            transform: translateY(-8px);
        }

        .envelope-front {
            position: absolute;
            inset: 0;
            background: linear-gradient(145deg, #8edcf8, #63bfe6);
            z-index: 3;
            clip-path: polygon(0 0, 50% 52%, 100% 0, 100% 100%, 0 100%);
        }

        .flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 150px;
            background: #b8eaff;
            clip-path: polygon(0 0, 100% 0, 50% 100%);
            transform-origin: top;
            transition: transform 1.2s cubic-bezier(.68,-0.55,.27,1.55);
            z-index: 5;
        }

        .seal {
            position: absolute;
            top: 115px;
            left: 50%;
            transform: translateX(-50%);
            width: 55px;
            height: 55px;
            border-radius: 50%;
            background: #ffffff;
            color: #49a9d1;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 25px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.15);
            z-index: 6;
            transition: opacity 0.5s ease;
        }

        .envelope-text {
            position: absolute;
            bottom: 30px;
            width: 100%;
            z-index: 7;
            color: white;
            font-size: 18px;
            font-weight: bold;
            letter-spacing: 1px;
        }

        .click-text {
            margin-top: 18px;
            font-size: 14px;
            opacity: 0.75;
            animation: pulse 1.8s infinite;
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 0.45;
            }
            50% {
                opacity: 1;
            }
        }

        /* =========================
           OPEN LETTER
        ========================== */
        .letter {
            display: none;
            width: min(800px, 95vw);
            background: rgba(255,255,255,0.94);
            border-radius: 22px;
            padding: 55px;
            box-shadow: 0 30px 80px rgba(28, 108, 145, 0.25);
            position: relative;
            animation: letterAppear 1.2s ease forwards;
            backdrop-filter: blur(12px);
        }

        body.dark .letter {
            background: rgba(17, 43, 58, 0.96);
            color: #e8f8ff;
        }

        @keyframes letterAppear {
            0% {
                opacity: 0;
                transform: translateY(70px) scale(0.8);
            }

            100% {
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        .letter.open {
            display: block;
        }

        .close-btn {
            position: absolute;
            top: 18px;
            right: 20px;
            width: 35px;
            height: 35px;
            border: none;
            border-radius: 50%;
            background: #dff6ff;
            color: #267c9f;
            font-size: 18px;
            cursor: pointer;
            transition: 0.3s;
        }

        .close-btn:hover {
            transform: rotate(90deg) scale(1.1);
        }

        .header-icon {
            font-size: 55px;
            text-align: center;
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 100% {
                transform: translateY(0);
            }

            50% {
                transform: translateY(-8px);
            }
        }

        h1 {
            text-align: center;
            font-size: clamp(28px, 5vw, 48px);
            color: #2385ae;
            margin: 10px 0;
        }

        body.dark h1 {
            color: #8bdcff;
        }

        .subtitle {
            text-align: center;
            font-size: 16px;
            color: #6c9bad;
            margin-bottom: 35px;
        }

        body.dark .subtitle {
            color: #a4cfdf;
        }

        .divider {
            width: 100px;
            height: 4px;
            background: #72c8eb;
            border-radius: 20px;
            margin: 20px auto 35px;
        }

        .letter p {
            font-size: 17px;
            line-height: 1.9;
            margin-bottom: 20px;
        }

        .highlight {
            color: #2385ae;
            font-weight: bold;
        }

        body.dark .highlight {
            color: #8bdcff;
        }

        .quote {
            background: #e8f8ff;
            border-left: 5px solid #67c3e8;
            padding: 20px;
            margin: 30px 0;
            border-radius: 10px;
            font-style: italic;
            color: #39728a;
        }

        body.dark .quote {
            background: #153b4d;
            color: #b8e7f6;
        }

        .signature {
            margin-top: 40px;
            text-align: right;
        }

        .signature-name {
            font-family: "Brush Script MT", cursive;
            font-size: 32px;
            color: #2786aa;
        }

        body.dark .signature-name {
            color: #8bdcff;
        }

        .footer {
            text-align: center;
            margin-top: 40px;
            font-size: 14px;
            color: #7aa5b4;
        }

        /* =========================
           BUTTON
        ========================== */
        .back-btn {
            display: block;
            margin: 30px auto 0;
            border: none;
            padding: 12px 25px;
            border-radius: 30px;
            background: linear-gradient(135deg, #69c7eb, #3ca4d0);
            color: white;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .back-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(52, 153, 195, 0.3);
        }

        /* =========================
           RESPONSIVE
        ========================== */
        @media (max-width: 600px) {
            .letter {
                padding: 35px 22px;
            }

            .letter p {
                font-size: 15px;
            }

            .envelope {
                height: 240px;
            }
        }
    </style>
</head>

<body>

    <!-- =========================
         THEME BUTTON
    ========================== -->
    <div class="top-bar">
        <button class="theme-btn" id="themeBtn">
            🌙 Dark Mode
        </button>
    </div>

    <!-- =========================
         BALLOONS
    ========================== -->
    <div class="balloon-container">
        <div class="balloon b1"></div>
        <div class="balloon b2"></div>
        <div class="balloon b3"></div>
        <div class="balloon b4"></div>
        <div class="balloon b5"></div>
        <div class="balloon b6"></div>
    </div>

    <!-- =========================
         MAIN PAGE
    ========================== -->
    <main class="page">

        <!-- ENVELOPE -->
        <div class="envelope-wrapper" id="envelopeWrapper">

            <div class="envelope" id="envelope">

                <div class="flap" id="flap"></div>

                <div class="seal">
                    💙
                </div>

                <div class="envelope-front"></div>

                <div class="envelope-text">
                    For Sir Randy Bello
                </div>

            </div>

            <div class="click-text">
                💌 Click the letter to open
            </div>

        </div>

        <!-- =========================
             LETTER
        ========================== -->
        <section class="letter" id="letter">

            <button class="close-btn" id="closeBtn">
                ×
            </button>

            <div class="header-icon">
                👨‍🏫💙
            </div>

            <h1>Happy Teacher's Day!</h1>

            <div class="subtitle">
                A Special Letter for Sir Randy Bello
            </div>

            <div class="divider"></div>

            <p>
                Dear <span class="highlight">Sir Randy Bello</span>,
            </p>

            <p>
                Happy Teacher's Day, Sir Randy! 💙
                I would like to take this opportunity to thank you for
                being a wonderful and dedicated <span class="highlight">
                Web Development instructor</span>.
            </p>

            <p>
                Thank you for patiently teaching us the different
                concepts of web development and for helping us understand
                HTML, CSS, JavaScript, and other important skills.
                Your lessons have helped us become more confident in
                exploring the world of technology.
            </p>

            <div class="quote">
                “A great teacher doesn't just teach lessons;
                they inspire students to believe in what they can become.”
            </div>

            <p>
                We truly appreciate your patience, effort, and dedication
                in guiding us. Even when programming becomes challenging,
                you encourage us to keep learning, practicing, and improving.
            </p>

            <p>
                As your student, I am grateful for the knowledge and
                experiences you share with us. Thank you for being more
                than just an instructor, but also someone who motivates us
                to become better students and future professionals.
            </p>

            <p>
                May you continue inspiring many more students through your
                passion for teaching and technology. We wish you happiness,
                success, good health, and many more achievements.
            </p>

            <p>
                Once again, <span class="highlight">
                Happy Teacher's Day, Sir Randy!</span>
                Thank you for everything you do for your students. 💙🎈
            </p>

            <div class="signature">
                <p>With sincere appreciation,</p>

                <div class="signature-name">
                    Your Student
                </div>

                <p>
                    💻 Web Development Student
                </p>
            </div>

            <div class="footer">
                Made with 💙, appreciation, and a little bit of JavaScript.
            </div>

            <button class="back-btn" id="backBtn">
                💌 Close Letter
            </button>

        </section>

    </main>

    <!-- =========================
         JAVASCRIPT
    ========================== -->
    <script>

        const envelope = document.getElementById("envelope");
        const flap = document.getElementById("flap");
        const letter = document.getElementById("letter");
        const envelopeWrapper = document.getElementById("envelopeWrapper");

        const closeBtn = document.getElementById("closeBtn");
        const backBtn = document.getElementById("backBtn");

        const themeBtn = document.getElementById("themeBtn");

        /* =========================
           OPEN LETTER
        ========================== */

        envelope.addEventListener("click", function () {

            flap.style.transform = "rotateX(180deg)";

            setTimeout(() => {

                envelopeWrapper.style.opacity = "0";
                envelopeWrapper.style.transform = "scale(0.7)";

            }, 600);

            setTimeout(() => {

                envelopeWrapper.style.display = "none";
                letter.classList.add("open");

                window.scrollTo({
                    top: 0,
                    behavior: "smooth"
                });

            }, 1100);

        });

        /* =========================
           CLOSE LETTER
        ========================== */

        function closeLetter() {

            letter.classList.remove("open");

            setTimeout(() => {

                envelopeWrapper.style.display = "block";

                setTimeout(() => {

                    envelopeWrapper.style.opacity = "1";
                    envelopeWrapper.style.transform = "scale(1)";
                    flap.style.transform = "rotateX(0deg)";

                }, 50);

            }, 300);
        }

        closeBtn.addEventListener("click", closeLetter);

        backBtn.addEventListener("click", closeLetter);

        /* =========================
           DARK / LIGHT MODE
        ========================== */

        themeBtn.addEventListener("click", function () {

            document.body.classList.toggle("dark");

            if (document.body.classList.contains("dark")) {

                themeBtn.innerHTML = "☀️ Light Mode";

            } else {

                themeBtn.innerHTML = "🌙 Dark Mode";

            }

        });

        /* =========================
           EXTRA BALLOON EFFECT
        ========================== */

        function createBalloon() {

            const balloon = document.createElement("div");

            balloon.classList.add("balloon");

            balloon.style.left = Math.random() * 100 + "%";
            balloon.style.animationDuration =
                (12 + Math.random() * 10) + "s";

            balloon.style.width =
                (40 + Math.random() * 25) + "px";

            balloon.style.height =
                (55 + Math.random() * 30) + "px";

            const colors = [
                "#8edfff",
                "#b4e9ff",
                "#6ec8f0",
                "#a4ddff",
                "#74c8ee",
                "#c4efff"
            ];

            balloon.style.background =
                colors[Math.floor(Math.random() * colors.length)];

            balloon.style.color = balloon.style.background;

            document
                .querySelector(".balloon-container")
                .appendChild(balloon);

            setTimeout(() => {
                balloon.remove();
            }, 22000);
        }

        setInterval(createBalloon, 5000);

    </script>

</body>
</html>
```

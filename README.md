# Happy-Valantine-s-Day
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Valentine’s Treasure</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    background: #7a0012;
    font-family: 'Poppins', sans-serif;
    overflow-x: hidden;
}

.page {
    min-height: 100vh;
    display: none;
    justify-content: center;
    align-items: center;
    padding: 20px;
    text-align: center;
}
.page.active {
    display: flex;
}

.card {
    background: rgba(255,255,255,0.15);
    padding: 30px;
    border-radius: 20px;
    max-width: 520px;
    width: 100%;
    color: white;
}

.map {
    background: #f5e6c8;
    color: #5a3b1a;
    padding: 30px;
    border-radius: 15px;
    max-width: 550px;
    width: 100%;
}

.map h2 {
    font-family: 'Great Vibes', cursive;
    font-size: 42px;
}

.chests {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 15px;
    margin-top: 20px;
}

.chest {
    background: #c49a6c;
    padding: 20px;
    border-radius: 15px;
    cursor: pointer;
    font-size: 18px;
}

.letter {
    background: #fff8ee;
    color: #5a1a1a;
    padding: 30px;
    border-radius: 15px;
    max-width: 520px;
    width: 100%;
    text-align: left;
    line-height: 1.9;
}

.letter h2 {
    text-align: center;
    font-family: 'Great Vibes', cursive;
    font-size: 42px;
}

button {
    margin-top: 20px;
    padding: 10px 25px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    background: white;
    color: #7a0012;
}

.heart {
    position: fixed;
    bottom: -20px;
    font-size: 20px;
    animation: float 6s linear infinite;
}

@keyframes float {
    from { transform: translateY(0); opacity: 1; }
    to { transform: translateY(-100vh); opacity: 0; }
}
</style>
</head>

<body>

<!-- INTRO -->
<div class="page active" id="page1">
    <div class="card">
        <h1 style="font-family:'Great Vibes', cursive; font-size:52px;">
            Happy Valentine’s Day ❤️
        </h1>
        <p>
            This isn’t just a website.<br>
            It’s a journey through my heart.<br>
            Open each chest and discover my love 💖
        </p>
        <button onclick="showPage('map')">Start the Journey 🗺️</button>
    </div>
</div>

<!-- MAP -->
<div class="page" id="map">
    <div class="map">
        <h2>Treasure Map 🗺️</h2>
        <p>Every chest holds a piece of my heart 💝</p>

        <div class="chests">
            <div class="chest" onclick="openChest(1)">💎 Chest One</div>
            <div class="chest" onclick="openChest(2)">💖 Chest Two</div>
            <div class="chest" onclick="openChest(3)">💌 Chest Three</div>
            <div class="chest" onclick="openChest(4)">✨ Final Treasure</div>
        </div>
    </div>
</div>

<!-- CHEST 1 -->
<div class="page" id="chest1">
    <div class="letter">
        <h2>Chest One 💎</h2>
        <p>
            From the moment you came into my life, everything started to feel different.
            The smallest moments became meaningful, and ordinary days turned into memories
            I never want to forget.
        </p>
        <p>
            You are precious to me in ways words can never fully explain.
            Just like this chest holds a treasure, my heart holds you —
            carefully, deeply, and forever.
        </p>
        <button onclick="showPage('map')">Back to Map</button>
    </div>
</div>

<!-- CHEST 2 -->
<div class="page" id="chest2">
    <div class="letter">
        <h2>Chest Two 💖</h2>
        <p>
            I know our journey hasn’t always been easy.
            We’ve had moments of doubt, distance, and silence.
            But even in those moments, my heart never stopped choosing you.
        </p>
        <p>
            I truly believe that every challenge we face is only shaping us
            into something stronger, something more meaningful.
            As long as we keep moving forward together,
            I know we can face anything.
        </p>
        <button onclick="showPage('map')">Back to Map</button>
    </div>
</div>

<!-- CHEST 3 -->
<div class="page" id="chest3">
    <div class="letter">
        <h2>Chest Three 💌</h2>
        <p>
            I love you today, tomorrow, and forever.
            Not just in the happy moments,
            but also in the quiet, imperfect, real ones.
        </p>
        <p>
            My love for you isn’t temporary or conditional.
            It’s a promise I carry with me every single day —
            to stand by you, support you, and choose you again and again.
        </p>
        <button onclick="showPage('map')">Back to Map</button>
    </div>
</div>

<!-- FINAL CHEST -->
<div class="page" id="chest4">
    <div class="letter">
        <h2>The Final Treasure ✨</h2>
        <p>
            If there’s one thing I want you to remember,
            it’s this: you are my home.
            In your presence, I feel safe, loved, and understood.
        </p>
        <p>
            I want to be the only one for you,
            just as you are the only one for me.
            No matter where life takes us,
            my heart will always find its way back to you.
        </p>
        <p style="text-align:right; font-family:'Great Vibes', cursive; font-size:32px;">
            Happy Valentine’s Day ❤️
        </p>
    </div>
</div>

<script>
function showPage(id) {
    document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
    document.getElementById(id).classList.add('active');
}

function openChest(num) {
    showPage('chest' + num);
}

setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "❤️";
    heart.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
}, 600);
</script>

</body>
</html>

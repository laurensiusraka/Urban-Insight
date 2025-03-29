<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projek HTML Pertama Saya</title>
</head>
<body>
    <h1>Halo Selamat Pagi, Aku Laurensius Raka Yudha!</h1>
    <p>Selamat datang di projek aku dalam membuat website pribadi menggunakan code HTML.</p>
    <p>Di projek ini aku kan mengulik, gimana cara mendesain website menggunakan code HTML. Saya bukan seorang ahli cooding, dan saya menggunakan bantuan AI untuk merancang dan mengembangkan code website ini.</p>
    <p>Tujuannya adalah memberikan edukasi bahwa dalam belajar kita bisa memaksimalkan pemanfaatan AI untuk menunjang proses belajar kita. Tanpa berlama-lama</p>
    <p>Let's get start, see You On Top Guyss!!</p>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Website Pribadi</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #05013ed2;
            margin: 0;
            padding: 0;
        }
        .container {
            width: 60%;
            margin: auto;
            background: rgb(59, 2, 2);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
        }
        img {
            width: 150px;
            border-radius: 50%;
        }
        h1 {
            color: #f7fbfb;
        }
        p {
            color: #faf7f7;
        }
        .social-links a {
            text-decoration: none;
            color: rgb(9, 0, 0);
            background: #caf811;
            padding: 10px 15px;
            margin: 5px;
            border-radius: 5px;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Urban Insight</h1>
        <p>Hello, Im Urban and Regional Planning student with a strong passion for creating sustainable urban environments. With a background in urban planning, I possess skills in social analysis and mapping, which enable me to understand the dynamics of communities and spatial structures in various contexts</p>
        <p>I firmly believe that ecological aspects are the foundation of creating harmonious and sustainable cities. By adopting an approach that balances people, the environment, and technology, I aspire to contribute to designing innovative solutions that positively impact urban life.</p>
        <p>Let's shape sustainable cities together!</p>
        <div class="social-links">
            <a href="https://www.linkedin.com/in/laurensiusrakaa" target="_blank">LinkedIn</a>
            <a href="https://www.instagram.com/laurensiusrakaa" target="_blank">Instagram</a>
            <a href="https://laurensiusraka.wordpress.com/" target="_blank">Wordpress</a>
        </div>
    </div>
    <div class="second-container">
        <div class="nav-buttons">
            <a href="#">Book</a>
            <a href="#">Podcast</a>
            <a href="#">Comingsoon</a>
        </div>
        <p class="quote">“Ketika kuat, bertindaklah lemah; ketika lemah, bertindaklah kuat. -Sun Tzu (Art of War)”</p>
    <style>
        .second-container {
    width: 60%;
    margin: 20px auto;
    background: #007bff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    color: white;
    text-align: center;
}

.nav-buttons {
    margin-bottom: 15px;
}

.nav-buttons a {
    text-decoration: none;
    color: #007bff;
    background: white;
    padding: 10px 15px;
    margin: 5px;
    border-radius: 5px;
    display: inline-block;
    font-weight: bold;
    transition: background 0.3s ease, color 0.3s ease;
}

.nav-buttons a:hover {
    background: #0056b3;
    color: white;
}

.quote {
    font-style: italic;
    font-size: 18px;
}
</style>
    </div>
    <div class="tetris-container">
        <h2>Permainan Tetris</h2>
        <canvas id="tetris" width="200" height="400"></canvas>
    <style>
        .tetris-container {
    text-align: center;
    margin-top: 20px;
}

canvas {
    background: black;
    display: block;
    margin: auto;
}

    </div>
    
    <script>
    const canvas = document.getElementById("tetris");
    const ctx = canvas.getContext("2d");
    const ROWS = 20;
    const COLS = 10;
    const BLOCK_SIZE = 20;
    let board = Array.from({ length: ROWS }, () => Array(COLS).fill(0));

    function drawBoard() {
        ctx.fillStyle = "black";
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        for (let row = 0; row < ROWS; row++) {
            for (let col = 0; col < COLS; col++) {
                if (board[row][col]) {
                    ctx.fillStyle = "cyan";
                    ctx.fillRect(col * BLOCK_SIZE, row * BLOCK_SIZE, BLOCK_SIZE, BLOCK_SIZE);
                    ctx.strokeStyle = "white";
                    ctx.strokeRect(col * BLOCK_SIZE, row * BLOCK_SIZE, BLOCK_SIZE, BLOCK_SIZE);
                }
            }
        }
    }

    function dropBlock() {
        for (let row = ROWS - 2; row >= 0; row--) {
            for (let col = 0; col < COLS; col++) {
                if (board[row][col] && !board[row + 1][col]) {
                    board[row + 1][col] = board[row][col];
                    board[row][col] = 0;
                }
            }
        }
        drawBoard();
    }

    function placeBlock() {
        board[0][Math.floor(COLS / 2)] = 1;
    }

    document.addEventListener("keydown", (event) => {
        if (event.key === "ArrowDown") {
            dropBlock();
        }
    });

    placeBlock();
    drawBoard();
    setInterval(dropBlock, 1000);
</script>
</body>
</html>

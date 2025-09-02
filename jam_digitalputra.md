<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jam Digital</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="clock">
        <div class="time">
            <span id="hours">00</span>:
            <span id="minutes">00</span>:
            <span id="seconds">00</span>
        </div>
    </div>
    <im style="width:100%; height: 30%"src="jam.jpg" alt="jam"/>
    
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    background-color: black;
    
}

.clock {
    width: 300px;
    height: 100px;
    margin: 50px auto;
    text-align: center;
    background-color: #f1f1f1;
    border-radius: 10px;
    box-shadow: 0 0 100px blue;
}


.time {
    font-size: 48px;
    font-weight: bold;
    color: black;
    text-shadow: 0 0 100px blue;
}

function updateClock() {
    const now = new Date();
    const hours = now.getHours().toString().padStart(2, '0');
    const minutes = now.getMinutes().toString().padStart(2, '0');
    const seconds = now.getSeconds().toString().padStart(2, '0');

    document.getElementById('hours').textContent = hours;
    document.getElementById('minutes').textContent = minutes;
    document.getElementById('seconds').textContent = seconds;
}

setInterval(updateClock, 1000);
updateClock();

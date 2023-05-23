<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>relógio</title>
    <link rel="stylesheet" href="styles.css">
    
</head>
<body>
    <main>
        <span id="hour">00</span>
        <span>:</span>
        <span id="min">00</span>
        <span>:</span>
        <apan id="sec">00</apan>
    </main>
    <script src="script.js"></script>
</body>
</html>



//css 

body {
    background-color: rgb(217, 255, 0);
}

main {
    width: 100%;
    height: 100hv;
    justify-content: center;
    align-items: center;
    display: flex;
}
span { 
    font-size: 50px;
    margin: 50px;
    padding: 50px;
    border-radius: 100px;
}

#hour, #min, #sec {
      background-color: #01ffc0;
}


//SCRPIT.JS

const hour = document.querySelector('#hour');
const min = document.querySelector('#min');
const sec = document.querySelector('#sec');

setInterval(() => {
    let date = new Date();
    let hours = date.getHours();
    let minutes = date.getMinutes();
    let seconds = date.getSeconds();

    hour.innerHTML = `${formatTime(hours)}`;
    min.innerHTML = `${formatTime(minutes)}`;
    sec.innerHTML = `${formatTime(seconds)}`;

}, 1000);

function formatTime(time){
    return time < 10 ? "0" + time : time
}

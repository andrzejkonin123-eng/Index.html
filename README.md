<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Barber Shop Elite</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial, sans-serif;
}

body{
    background:#0f0f0f;
    color:#fff;
}

/* NAV */
nav{
    position:fixed;
    width:100%;
    background:#000;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px 30px;
    z-index:1000;
}

nav h1{
    color:#f5c542;
}

nav ul{
    display:flex;
    gap:20px;
    list-style:none;
}

nav ul li a{
    color:white;
    text-decoration:none;
    transition:0.3s;
}

nav ul li a:hover{
    color:#f5c542;
}

/* HERO */
.hero{
    height:100vh;
    background:url('https://images.unsplash.com/photo-1503951914875-452162b0f3f1?auto=format&fit=crop&w=1400&q=80') center/cover;
    display:flex;
    align-items:center;
    justify-content:center;
    text-align:center;
}

.hero h2{
    font-size:50px;
    background:rgba(0,0,0,0.6);
    padding:20px;
    border-radius:10px;
}

/* SEKCJE */
section{
    padding:80px 20px;
    text-align:center;
}

h2.title{
    color:#f5c542;
    margin-bottom:20px;
}

/* USŁUGI */
.services{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:20px;
}

.card{
    background:#1a1a1a;
    padding:20px;
    width:250px;
    border-radius:10px;
    transition:0.3s;
}

.card:hover{
    transform:scale(1.05);
    background:#222;
}

/* GALERIA */
.gallery{
    display:grid;
    grid-template-columns:repeat(auto-fit, minmax(200px, 1fr));
    gap:10px;
}

.gallery img{
    width:100%;
    height:200px;
    object-fit:cover;
    border-radius:10px;
}

/* FORMULARZ */
form{
    max-width:400px;
    margin:auto;
    display:flex;
    flex-direction:column;
    gap:10px;
}

input, select, button{
    padding:10px;
    border:none;
    border-radius:5px;
}

button{
    background:#f5c542;
    cursor:pointer;
    font-weight:bold;
}

button:hover{
    background:#d4a92f;
}

/* STOPKA */
footer{
    padding:20px;
    background:#000;
    text-align:center;
    margin-top:40px;
}
</style>
</head>

<body>

<nav>
    <h1>BARBER ELITE</h1>
    <ul>
        <li><a href="#services">Usługi</a></li>
        <li><a href="#gallery">Galeria</a></li>
        <li><a href="#booking">Rezerwacja</a></li>
    </ul>
</nav>

<div class="hero">
    <h2>Twój styl. Nasze nożyczki.</h2>
</div>

<section id="services">
    <h2 class="title">Usługi</h2>
    <div class="services">
        <div class="card">
            <h3>Strzyżenie</h3>
            <p>Profesjonalne cięcie dopasowane do stylu.</p>
        </div>
        <div class="card">
            <h3>Broda</h3>
            <p>Modelowanie i pielęgnacja zarostu.</p>
        </div>
        <div class="card">
            <h3>Fade</h3>
            <p>Najczystsze przejścia w mieście.</p>
        </div>
    </div>
</section>

<section id="gallery">
    <h2 class="title">Galeria</h2>
    <div class="gallery">
        <img src="https://images.unsplash.com/photo-1517832606299-7ae9b720a186" />
        <img src="https://images.unsplash.com/photo-1520975916090-3105956dac38" />
        <img src="https://images.unsplash.com/photo-1621607512022-6aecc4fed814" />
        <img src="https://images.unsplash.com/photo-1516975080664-ed2fc6a32937" />
    </div>
</section>

<section id="booking">
    <h2 class="title">Rezerwacja</h2>

    <form id="form">
        <input type="text" id="name" placeholder="Twoje imię" required>
        <input type="date" id="date" required>
        <select id="service">
            <option>Strzyżenie</option>
            <option>Broda</option>
            <option>Fade</option>
        </select>
        <button type="submit">Zarezerwuj</button>
    </form>

    <p id="msg"></p>
</section>

<footer>
    © 2026 Barber Elite
</footer>

<script>
document.getElementById("form").addEventListener("submit", function(e){
    e.preventDefault();

    let name = document.getElementById("name").value;
    let date = document.getElementById("date").value;

    document.getElementById("msg").innerText =
        "Zarezerwowano dla " + name + " na " + date + " 💈";
});
</script>

</body>
</html>

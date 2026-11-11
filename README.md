# kevin.github.io
pagina web 

<!DOCTYPE html>
<html lang="es">
<head>
<title>Página de Lamborghini</title>
<link rel="icon" type="image/x-icon" href="logo favicon.ico">
<style>
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:#050505;color:white;font-family:Arial,Helvetica,sans-serif}
nav{position:fixed;top:0;width:100%;z-index:1000;background:rgba(0,0,0,0.88);backdrop-filter:blur(10px);padding:15px 40px;display:flex;justify-content:space-between;align-items:center;border-bottom:1px solid #333}
.logo{color:#f5c400;font-size:24px;font-weight:bold;letter-spacing:3px}
nav a{color:white;text-decoration:none;margin-left:25px;font-size:14px;transition:0.3s}
nav a:hover{color:#f5c400}
.hero{height:100vh;min-height:600px;background:linear-gradient(rgba(0,0,0,0.35),rgba(0,0,0,0.85)),url("lambo.jpg") center/cover no-repeat;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;padding:20px}
.hero h1{font-size:clamp(50px,10vw,120px);letter-spacing:15px;text-shadow:0 0 30px rgba(255,200,0,0.4);margin-bottom:15px}
.linea{width:120px;height:4px;background:#f5c400;margin:25px auto}
.contenedor{width:90%;max-width:1300px;margin:auto;padding:80px 0}
.titulo{text-align:center;font-size:38px;margin-bottom:15px;color:#f5c400;letter-spacing:3px}
.subtitulo{text-align:center;color:#aaa;margin-bottom:45px}
#formulario{max-width:600px;margin:0 auto;background:linear-gradient(145deg,#161616,#090909);padding:40px;border-radius:20px;border:1px solid #333;box-shadow:0 15px 50px rgba(0,0,0,0.6)}
label{display:block;margin-top:20px;margin-bottom:8px;color:#f5c400;font-weight:bold}
input,select{width:100%;padding:15px;background:#111;color:white;border:1px solid #444;border-radius:8px;outline:none;transition:0.3s}
input:focus,select:focus{border-color:#f5c400;box-shadow:0 0 12px rgba(245,196,0,0.25)}
button{width:100%;margin-top:25px;padding:15px;border:none;border-radius:8px;background:linear-gradient(90deg,#f5c400,#ff8c00);color:black;font-weight:bold;font-size:16px;cursor:pointer;transition:0.3s}
button:hover{transform:translateY(-3px);box-shadow:0 8px 25px rgba(245,196,0,0.35)}
#bienvenida{display:none;text-align:center;margin-top:40px;animation:aparecer 0.8s ease}
#saludo{font-size:30px;color:#f5c400}
#modelos{display:none;margin-top:80px;animation:aparecer 0.8s ease}
.selector{max-width:500px;margin:0 auto 70px}
.tarjetas{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:30px}
.card{position:relative;overflow:hidden;height:350px;border-radius:20px;background:#111;border:1px solid #333;transition:0.4s;cursor:pointer}
.card:hover{transform:translateY(-10px);border-color:#f5c400;box-shadow:0 15px 40px rgba(245,196,0,0.25)}
.card img{width:100%;height:100%;object-fit:cover;transition:0.6s}
.card:hover img{transform:scale(1.1)}
.card::after{content:"";position:absolute;inset:0;background:linear-gradient(transparent 40%,rgba(0,0,0,0.95))}
.card-info{position:absolute;z-index:2;bottom:0;width:100%;padding:30px 25px}
.card-info h3{color:white;font-size:25px;margin-bottom:8px}
.card-info p{color:#f5c400;font-size:14px;letter-spacing:1px}
#detalleModelo{display:none;margin-top:60px;padding:40px;background:linear-gradient(145deg,#161616,#080808);border:1px solid #444;border-radius:20px;animation:aparecer 0.8s ease}
#detalleModelo h2{color:#f5c400;font-size:35px;text-align:center;margin-bottom:25px}
#detalleModelo p{color:#ddd;font-size:16px;line-height:2}
#detalleModelo strong{color:#f5c400}
.precio-modelo{text-align:center;font-size:30px;color:#f5c400;margin:30px 0;font-weight:bold}
#pago{display:none;max-width:650px;margin:50px auto;padding:35px;background:linear-gradient(145deg,#161616,#090909);border:1px solid #444;border-radius:20px;animation:aparecer 0.8s ease}
#pago h2{text-align:center;color:#f5c400;margin-bottom:20px}
#ticket{display:none;max-width:650px;margin:50px auto;padding:35px;background:linear-gradient(145deg,#161616,#090909);border:2px solid #f5c400;border-radius:20px;box-shadow:0 15px 50px rgba(0,0,0,0.6);animation:aparecer 0.8s ease}
#ticket h2{text-align:center;color:#f5c400;font-size:32px;letter-spacing:4px;margin-bottom:10px}
.linea-ticket{height:2px;background:#f5c400;margin:20px 0}
#ticket p{color:#ddd;line-height:2;font-size:15px}
#ticket strong{color:#f5c400}
#ticket .total{text-align:center;color:#f5c400;font-size:27px;font-weight:bold;margin-top:25px}
#ticket .gracias{text-align:center;color:#aaa;margin-top:25px}
footer{margin-top:80px;padding:35px;text-align:center;background:#080808;border-top:1px solid #333;color:#777}
footer span{color:#f5c400}
@keyframes aparecer{from{opacity:0;transform:translateY(25px)}to{opacity:1;transform:translateY(0)}}
@media(max-width:700px){nav{padding:15px 20px}nav div:last-child{display:none}.hero h1{letter-spacing:5px}#formulario{padding:25px}.titulo{font-size:30px}.card{height:280px}#detalleModelo,#pago,#ticket{padding:25px}}
@media print{body *{visibility:hidden}#ticket,#ticket *{visibility:visible}#ticket{display:block;position:absolute;left:0;top:0;width:100%;background:white;color:black;border:2px solid black}#ticket p,#ticket .gracias{color:black}#ticket strong,#ticket h2,#ticket .total{color:black}#ticket button{display:none}}
</style>
</head>
<body>
<nav>
<div class="logo">LAMBORGHINI</div>
<div>
<a href="#inicio">INICIO</a>
<a href="#registro">REGISTRO</a>
<a href="#modelos">MODELOS</a>
</div>
</nav>
<section class="hero" id="inicio">
<h1>LAMBORGHINI</h1>
<div class="linea"></div>
</section>
<section class="contenedor" id="registro">
<h2 class="titulo">BIENVENIDO</h2>
<p class="subtitulo">Ingresa tus datos para explorar nuestros modelos</p>
<div id="formulario">
<label for="fname">NOMBRE</label>
<input type="text" id="fname" placeholder="Escribe tu nombre">
<label for="lname">APELLIDO</label>
<input type="text" id="lname" placeholder="Escribe tu apellido">
<button type="button" onclick="entrar()">ENTRAR</button>
</div>
<div id="bienvenida">
<h2 id="saludo"></h2>
</div>
<div id="modelos">
<h2 class="titulo">MODELOS</h2>
<p class="subtitulo">Explora nuestra colección de Lamborghini</p>
<div class="selector">
<select id="carros">
<option value="">-- SELECCIONA UN MODELO --</option>
<option value="revuelto">REVUELTO</option>
<option value="revueltosv">REVUELTO SV</option>
<option value="urusseper">URUS SE PERFORMANTE</option>
<option value="urusse">URUS SE</option>
<option value="temerario">TEMERARIO</option>
</select>
<button type="button" onclick="enviarModelo()">VER MODELO</button>
</div>
<div class="tarjetas">
<div class="card">
<img src="revuelto.jpg" alt="Lamborghini Revuelto">
<div class="card-info"><h3>REVUELTO</h3><p>V12 HÍBRIDO</p></div>
</div>
<div class="card">
<img src="revueltosv.jpg" alt="Lamborghini Revuelto SV">
<div class="card-info"><h3>REVUELTO SV</h3><p>ALTO RENDIMIENTO</p></div>
</div>
<div class="card">
<img src="urusseper.jpg" alt="Lamborghini Urus SE Performante">
<div class="card-info"><h3>URUS SE PERFORMANTE</h3><p>SUPER SUV</p></div>
</div>
<div class="card">
<img src="urusse.jpg" alt="Lamborghini Urus SE">
<div class="card-info"><h3>URUS SE</h3><p>SUV HÍBRIDO</p></div>
</div>
<div class="card">
<img src="temerario.jpg" alt="Lamborghini Temerario">
<div class="card-info"><h3>TEMERARIO</h3><p>NUEVA GENERACIÓN</p></div>
</div>
</div>
<div id="detalleModelo">
<h2 id="nombreModelo"></h2>
<p id="descripcionModelo"></p>
<div class="precio-modelo" id="precioModelo"></div>
</div>
<div id="pago">
<h2>FORMA DE PAGO</h2>
<p class="subtitulo">Selecciona tu moneda y método de pago</p>
<label for="moneda">SELECCIONA TU MONEDA</label>
<select id="moneda" onchange="actualizarPrecio()">
<option value="MXN">PESO MEXICANO (MXN)</option>
<option value="USD">DÓLAR ESTADOUNIDENSE (USD)</option>
<option value="EUR">EURO (EUR)</option>
<option value="GBP">LIBRA ESTERLINA (GBP)</option>
<option value="JPY">YEN JAPONÉS (JPY)</option>
</select>
<label for="metodo">MÉTODO DE PAGO</label>
<select id="metodo">
<option value="">-- SELECCIONA TU MÉTODO --</option>
<option value="Tarjeta de crédito">TARJETA DE CRÉDITO</option>
<option value="Tarjeta de débito">TARJETA DE DÉBITO</option>
<option value="Transferencia bancaria">TRANSFERENCIA BANCARIA</option>
<option value="Pago de contado">PAGO DE CONTADO</option>
</select>
<p class="precio-modelo" id="precioPago"></p>
<button type="button" onclick="generarTicket()">GENERAR TICKET</button>
</div>
<div id="ticket">
<h2>LAMBORGHINI</h2>
<p style="text-align:center;color:#f5c400">TICKET DE COMPRA</p>
<div class="linea-ticket"></div>
<p><strong>CLIENTE:</strong> <span id="ticketCliente"></span></p>
<p><strong>MODELO:</strong> <span id="ticketModelo"></span></p>
<p><strong>CARACTERÍSTICAS:</strong></p>
<p id="ticketCaracteristicas"></p>
<div class="linea-ticket"></div>
<p><strong>MONEDA:</strong> <span id="ticketMoneda"></span></p>
<p><strong>MÉTODO DE PAGO:</strong> <span id="ticketMetodo"></span></p>
<div class="linea-ticket"></div>
<div class="total" id="ticketTotal"></div>
<div class="linea-ticket"></div>
<p class="gracias">GRACIAS POR ELEGIR LAMBORGHINI</p>
<p class="gracias">LA EXPERIENCIA DE LA VELOCIDAD Y EL LUJO.</p>
<button type="button" onclick="window.print()">IMPRIMIR TICKET</button>
</div>
</div>
</section>
<footer>
<p>0% AI</p>
</footer>
<script>
const modelos={
revuelto:{nombre:"LAMBORGHINI REVUELTO",motor:"V12 de 6.5 litros híbrido",potencia:"1015 CV",velocidad:"Más de 350 km/h",aceleracion:"0 a 100 km/h en 2.5 segundos",tipo:"Superdeportivo híbrido",precio:9000000},
revueltosv:{nombre:"LAMBORGHINI REVUELTO SV",motor:"Motor V12 híbrido (versión ilustrativa)",potencia:"Versión de demostración",velocidad:"Dato ilustrativo",aceleracion:"Dato ilustrativo",tipo:"Superdeportivo de alto rendimiento",precio:11000000},
urusseper:{nombre:"LAMBORGHINI URUS SE PERFORMANTE",motor:"V8 biturbo híbrido",potencia:"Versión ilustrativa",velocidad:"Dato ilustrativo",aceleracion:"Dato ilustrativo",tipo:"SUV deportivo",precio:6500000},
urusse:{nombre:"LAMBORGHINI URUS SE",motor:"V8 biturbo híbrido",potencia:"800 CV",velocidad:"312 km/h",aceleracion:"0 a 100 km/h en 3.4 segundos",tipo:"SUV híbrido",precio:5500000},
temerario:{nombre:"LAMBORGHINI TEMERARIO",motor:"V8 biturbo híbrido",potencia:"920 CV",velocidad:"Más de 340 km/h",aceleracion:"0 a 100 km/h en 2.7 segundos",tipo:"Superdeportivo híbrido",precio:7000000}
};
const monedas={MXN:1,USD:0.055,EUR:0.051,GBP:0.044,JPY:8.5};
let modeloSeleccionado=null;
let precioActual=0;
function entrar(){
let nombre=document.getElementById("fname").value.trim();
let apellido=document.getElementById("lname").value.trim();
if(nombre===""||apellido===""){alert("POR FAVOR, RELLENA TU NOMBRE Y APELLIDO");return}
document.getElementById("saludo").innerText="HOLA, "+nombre.toUpperCase()+" "+apellido.toUpperCase()+" 👋";
document.getElementById("bienvenida").style.display="block";
document.getElementById("modelos").style.display="block";
document.getElementById("modelos").scrollIntoView({behavior:"smooth"});
}
function enviarModelo(){
let modelo=document.getElementById("carros").value;
if(modelo===""){alert("SELECCIONA UN MODELO");return}
modeloSeleccionado=modelos[modelo];
let datos=modeloSeleccionado;
document.getElementById("nombreModelo").innerText=datos.nombre;
document.getElementById("descripcionModelo").innerHTML="<strong>MOTOR:</strong> "+datos.motor+"<br><strong>POTENCIA:</strong> "+datos.potencia+"<br><strong>VELOCIDAD MÁXIMA:</strong> "+datos.velocidad+"<br><strong>ACELERACIÓN:</strong> "+datos.aceleracion+"<br><strong>TIPO:</strong> "+datos.tipo;
document.getElementById("detalleModelo").style.display="block";
document.getElementById("pago").style.display="block";
document.getElementById("ticket").style.display="none";
actualizarPrecio();
document.getElementById("detalleModelo").scrollIntoView({behavior:"smooth"});
}
function actualizarPrecio(){
if(!modeloSeleccionado)return;
let moneda=document.getElementById("moneda").value;
precioActual=modeloSeleccionado.precio*monedas[moneda];
let formato=new Intl.NumberFormat("es-MX",{style:"currency",currency:moneda,maximumFractionDigits:0}).format(precioActual);
document.getElementById("precioModelo").innerText="PRECIO: "+formato;
document.getElementById("precioPago").innerText="TOTAL: "+formato;
}
function generarTicket(){
if(!modeloSeleccionado){alert("SELECCIONA UN MODELO");return}
let metodo=document.getElementById("metodo").value;
if(metodo===""){alert("SELECCIONA UNA FORMA DE PAGO");return}
let nombre=document.getElementById("fname").value.trim();
let apellido=document.getElementById("lname").value.trim();
let moneda=document.getElementById("moneda").value;
let formato=new Intl.NumberFormat("es-MX",{style:"currency",currency:moneda,maximumFractionDigits:0}).format(precioActual);
let datos=modeloSeleccionado;
document.getElementById("ticketCliente").innerText=nombre.toUpperCase()+" "+apellido.toUpperCase();
document.getElementById("ticketModelo").innerText=datos.nombre;
document.getElementById("ticketCaracteristicas").innerHTML="Motor: "+datos.motor+"<br>Potencia: "+datos.potencia+"<br>Velocidad: "+datos.velocidad+"<br>Aceleración: "+datos.aceleracion+"<br>Tipo: "+datos.tipo;
document.getElementById("ticketMoneda").innerText=moneda;
document.getElementById("ticketMetodo").innerText=metodo;
document.getElementById("ticketTotal").innerText="TOTAL: "+formato;
document.getElementById("ticket").style.display="block";
document.getElementById("ticket").scrollIntoView({behavior:"smooth"});
}
</script>
</body>
</html>

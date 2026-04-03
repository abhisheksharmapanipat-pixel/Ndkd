# Ndkd
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Luxury Estate</title>

<style>
*{
  margin:0;
  padding:0;
  box-sizing:border-box;
  font-family: 'Poppins', sans-serif;
}

body{
  background:#0f172a;
  color:white;
}

/* NAVBAR */
nav{
  display:flex;
  justify-content:space-between;
  padding:20px 10%;
  position:fixed;
  width:100%;
  background:rgba(0,0,0,0.5);
  backdrop-filter: blur(10px);
  z-index:1000;
}

nav h1{
  color:#38bdf8;
}

nav a{
  margin-left:20px;
  text-decoration:none;
  color:white;
}

/* HERO */
.hero{
 .hero{
  height:100vh;
  background:url('https://images.unsplash.com/photo-1568605114967-8130f3a36994') center/cover;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;

  margin-top:80px; 
 
  height:100vh;
  background:url('https://images.unsplash.com/photo-1568605114967-8130f3a36994') center/cover;
  display:flex;
  align-items:center;
  justify-content:center;
  text-align:center;
}

.hero h2{
  font-size:3rem;
  animation:fadeIn 2s;
}

.btn{
  padding:12px 25px;
  background:#38bdf8;
  border:none;
  margin-top:20px;
  cursor:pointer;
}

/* SECTIONS */
section{
  padding:80px 10%;
}

.cards{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
  gap:20px;
}

.card{
  background:#1e293b;
  padding:15px;
  border-radius:10px;
  transition:0.3s;
}

.card:hover{
  transform:translateY(-10px);
}

.card img{
  width:100%;
  border-radius:10px;
}

/* ABOUT */
.about{
  display:flex;
  flex-wrap:wrap;
  gap:30px;
  align-items:center;
}

/* CONTACT */
input,textarea{
  width:100%;
  padding:10px;
  margin:10px 0;
}

footer{
  text-align:center;
  padding:20px;
  background:#020617;
}

/* ANIMATION */
@keyframes fadeIn{
  from{opacity:0; transform:translateY(20px);}
  to{opacity:1; transform:translateY(0);}
}

/* RESPONSIVE */
@media(max-width:768px){
  .hero h2{
    font-size:2rem;
  }
}
</style>
</head>

<body>

<nav>
  <h1>LuxuryEstate</h1>
  <div>
    <a href="#">Home</a>
    <a href="#properties">Properties</a>
    <a href="#about">About</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div>
    <h2>Find Your Dream Home</h2>
    <button class="btn" onclick="contact()">Contact Now</button>
  </div>
</div>

<!-- PROPERTIES -->
<section id="properties">
  <h2>Featured Properties</h2>
  <div class="cards">
    <div class="card">
      <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c">
      <h3>Modern Villa</h3>
      <p>₹1.5 Cr</p>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1572120360610-d971b9d7767c">
      <h3>Luxury Apartment</h3>
      <p>₹90 Lakh</p>
    </div>
    <div class="card">
      <img src="https://images.unsplash.com/photo-1600607687939-ce8a6c25118c">
      <h3>Farm House</h3>
      <p>₹2 Cr</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about" class="about">
  <img src="https://images.unsplash.com/photo-1560518883-ce09059eeffa" width="400">
  <div>
    <h2>About Us</h2>
    <p>We provide best real estate deals with trust and quality. Our mission is to help you find your perfect home.</p>
  </div>
</section>

<!-- SERVICES -->
<section>
  <h2>Our Services</h2>
  <div class="cards">
    <div class="card">Property Buying</div>
    <div class="card">Property Selling</div>
    <div class="card">Rental Services</div>
  </div>
</section>

<!-- TESTIMONIAL -->
<section>
  <h2>Testimonials</h2>
  <div class="cards">
    <div class="card">"Best service ever!"</div>
    <div class="card">"Got my dream home"</div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <h2>Contact Us</h2>
  <input type="text" placeholder="Your Name">
  <input type="email" placeholder="Your Email">
  <textarea placeholder="Message"></textarea>
  <button class="btn" onclick="contact()">Send</button>
</section>

<footer>
  <p>© 2026 LuxuryEstate</p>
</footer>

<script>
function contact(){
  window.open("https://wa.me/919050953173","_blank");
}

/* SCROLL ANIMATION */
const cards = document.querySelectorAll('.card');

window.addEventListener('scroll', () => {
  cards.forEach(card => {
    const top = card.getBoundingClientRect().top;
    if(top < window.innerHeight - 50){
      card.style.opacity = 1;
      card.style.transform = "translateY(0)";
    }
  });
});
</script>

</body>
</html>

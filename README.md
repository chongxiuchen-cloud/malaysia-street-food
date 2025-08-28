<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Home Eat APA</title>
<style>

  * {
    box-sizing: border-box;
  }
  
  body {
    background-color: burlywood;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }


  .header {
    background-color: #ff8c00;
    color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 30px;
    font-size: 28px;
    font-weight: bold;
    position: relative;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    animation: slideDown 0.7s ease-out;
  }


  .user-box {
    background-color: white;
    color: black;
    padding: 8px 15px;
    border-radius: 8px;
    font-size: 16px;
    display: flex;
    align-items: center;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    transition: all 0.3s ease;
  }

  .user-box:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 12px rgba(0,0,0,0.15);
  }


  .container {
    display: flex;
    justify-content: center;
    gap: 25px;
    margin-top: 30px;
    flex-wrap: wrap;
    padding: 0 20px;
    animation: fadeIn 1s ease-out;
  }
  
  .container2 {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 100px;
    flex-wrap: wrap;
    padding: 0 20px;
  }
  

  .curve {
    border-radius: 20px;
    overflow: hidden;
    transition: all 0.4s ease;
    box-shadow: 0 6px 15px rgba(0,0,0,0.1);
    position: relative;
  }
  
  .curve2 {
    border-radius: 20px;
    overflow: hidden;
  }
  
  .curve:hover {
    transform: translateY(-8px) scale(1.03);
    box-shadow: 0 12px 20px rgba(0,0,0,0.2);
  }
  
  .curve img {
    display: block;
    user-select: none;
    -webkit-user-drag: none;
    transition: transform 0.5s ease;
  }
  
  .curve:hover img {
    transform: scale(1.1);
  }
  

  button {
    padding: 8px 15px;
    margin-left: 10px;
    border-radius: 8px;
    border: none;
    background-color: darkorange;
    color: white;
    cursor: pointer;
    transition: all 0.3s ease;
    font-weight: bold;
  }
  
  button:hover {
    background-color: orange;
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
  }


  .about-us {
    background-color: #333;
    color: white;
    padding: 40px 30px;
    margin-top: 80px;
    text-align: center;
    animation: fadeInUp 1s ease-out;
  }
  
  .about-us h2 {
    color: orange;
    margin-bottom: 20px;
    font-size: 32px;
    position: relative;
    display: inline-block;
  }
  
  .about-us h2::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
    background-color: orange;
  }
  
  .about-us p {
    max-width: 800px;
    margin: 15px auto;
    line-height: 1.6;
    font-size: 17px;
  }
  

  .scroll-indicator {
    position: fixed;
    bottom: 30px;
    right: 30px;
    width: 50px;
    height: 50px;
    background-color: rgba(255, 140, 0, 0.8);
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    opacity: 0;
    visibility: hidden;
    transition: all 0.4s ease;
    z-index: 1000;
    box-shadow: 0 4px 12px rgba(0,0,0,0.2);
  }
  
  .scroll-indicator.show {
    opacity: 1;
    visibility: visible;
  }
  
  .scroll-indicator:hover {
    background-color: #ff8c00;
    transform: translateY(-5px);
  }
  
  .scroll-indicator i {
    color: white;
    font-size: 24px;
    font-weight: bold;
  }
  

  .section-title {
    text-align: center;
    margin: 40px 0 30px;
    position: relative;
    font-size: 28px;
    color: #333;
    animation: pulse 2s infinite;
  }
  

  @keyframes slideDown {
    from {
      transform: translateY(-100%);
      opacity: 0;
    }
    to {
      transform: translateY(0);
      opacity: 1;
    }
  }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes fadeInUp {
    from {
      opacity: 0;
      transform: translateY(40px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes pulse {
    0% {
      transform: scale(1);
    }
    50% {
      transform: scale(1.05);
    }
    100% {
      transform: scale(1);
    }
  }
  
  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
      transform: translateY(0);
    }
    40% {
      transform: translateY(-20px);
    }
    60% {
      transform: translateY(-10px);
    }
  }
  

  @media (max-width: 768px) {
    .header {
      flex-direction: column;
      text-align: center;
      padding: 15px;
    }
    
    .header h1 {
      margin: 15px 0;
      font-size: 24px;
    }
    
    .container {
      gap: 15px;
    }
    
    .curve {
      width: 130px;
    }
    
    .curve img {
      width: 130px;
      height: auto;
    }
  }
  

  .card-label {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    background-color: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 8px;
    text-align: center;
    font-size: 14px;
    transform: translateY(100%);
    transition: transform 0.3s ease;
  }
  
  .curve:hover .card-label {
    transform: translateY(0);
  }
</style>
</head>
<body onload="initUser()">

<div class="header">
  <div class="curve">
    <img src="LOGO.png" height="100" alt="eatlogo">
  </div>
  <h1>EAT APA?</h1>

  <div class="user-box">
    User: <span id="username-box"></span>
    <button onclick="logoutUser()">Logout</button>
  </div>
</div>


<div class="scroll-indicator" id="scrollToTop">
  <i>↑</i>
</div>

<div class="section-title">Explore Malaysian Cuisine</div>

<div class="container" id="main-container" style="display:none;">
  <div class="curve">
    <a href="disher.html">
      <img src="DISHES.jpg" width="150" height="100" alt="dishes">
      <div class="card-label">Dishes</div>
    </a>
  </div>

  <div class="curve">
    <a href="map.html">
      <img src="MAP.jpg" width="150" height="100" alt="map">
      <div class="card-label">Map</div>
    </a>
  </div>

  <div class="curve">
    <a href="streetfoodguide.html">
      <img src="guide.jpg" width="150" height="100" alt="guide">
      <div class="card-label">Street Food</div>
    </a>
  </div>

  <div class="curve">
    <a href="regional.html">
      <img src="regional.jpg" width="150" height="100" alt="religion">
      <div class="card-label">Regional</div>
    </a>
  </div>

  <div class="curve">
    <a href="desserts.html">
      <img src="dessert.jpg" width="150" height="100" alt="dessert">
      <div class="card-label">Desserts</div>
    </a>
  </div>

  <div class="curve">
    <a href="culture.html">
      <img src="foodculture.jpg" width="150" height="100" alt="foodculture">
      <div class="card-label">Food Culture</div>
    </a>
  </div>

  <div class="curve">
    <a href="recipe.html">
      <img src="recipe.jpg" width="150" height="100" alt="recipe">
      <div class="card-label">Recipes</div>
    </a>
  </div>

  <div class="curve">
    <a href="about.html">
      <img src="aboutus.jpg" width="150" height="100" alt="aboutus">
      <div class="card-label">About Us</div>
    </a>
  </div>
</div>

<div class="container2">
  <div class="curve2">
    <img src="blackfeature.jpg" height="50" alt="blackfeature">
  </div>
</div>

<div class="container">
  <div class="curve">
    <a href="desserts.html">
      <img src="nasikandar1.jpg" height="200" alt="NasiKandar">
      <div class="card-label">Nasi Kandar</div>
    </a>
  </div>
</div>

<div class="container">
  <div class="curve">
     <a href="recipe.html">
      <img src="satayy.jpg" height="200" alt="satay">
      <div class="card-label">Satay</div>
     </a>
  </div>
</div>

<div class="container2">
  <div class="curve2">
    <img src="TOP3.jpg" height="50" alt="TOP3">
  </div>
</div>

<div class="container">
  <div class="curve">
    <a href="regional.html">
    <img src="penang.jpg" height="100" alt="penang">
    <div class="card-label">Penang</div>
      </a>
  </div>
  <div class="curve">
      <a href="regional.html">
    <img src="johor.jpg" height="100" alt="johor">
    <div class="card-label">Johor</div>
      </a>
  </div>
  <div class="curve">
        <a href="regional.html">
    <img src="perak.jpg" height="100" alt="perak">
    <div class="card-label">Perak</div>
      </a>
  </div>
</div>

<footer class="about-us">
  <h2>About Us</h2>
  <p>
    Welcome to <strong>EAT APA</strong> — your ultimate guide to exploring delicious food, culture, and recipes. 
    Our mission is to bring together food lovers from around the world, sharing authentic dishes, 
    local specialties, and cultural stories behind every bite. Whether you're here to discover 
    new flavors, learn cooking tips, or explore food culture, we've got something for you.
  </p>
  <p>
    Developed with passion by our team of food enthusiasts, EAT APA is not just a website, 
    but a journey into the heart of culinary adventures.
  </p>
  <p>&copy; 2025 EAT APA. All Rights Reserved.</p>
</footer>

<script>

  function getCookie(name) {
    let cookies = document.cookie.split(';');
    for (let c of cookies) {
      let [key, val] = c.trim().split('=');
      if (key === name) return decodeURIComponent(val);
    }
    return null;
  }

  function initUser() {
    if (sessionStorage.getItem("isLoggedIn") !== "true") {
      alert("Please login first!");
      window.location.href = "index.html";
      return;
    }

    let emailFromCookie = getCookie("email");
    let emailFromLocal = localStorage.getItem("userEmail");
    let emailFromSession = sessionStorage.getItem("sessionEmail");

    let displayEmail = emailFromSession || emailFromCookie || emailFromLocal || "Guest";

    document.getElementById("username-box").textContent = displayEmail;
    document.getElementById("main-container").style.display = "flex";
    

    initScrollIndicator();
  }

  function logoutUser() {
    sessionStorage.clear();
    alert("Logged out successfully!");
    window.location.href = "index.html";
  }
  

  function initScrollIndicator() {
    const scrollBtn = document.getElementById('scrollToTop');
    
    window.addEventListener('scroll', function() {
      if (window.pageYOffset > 300) {
        scrollBtn.classList.add('show');
      } else {
        scrollBtn.classList.remove('show');
      }
    });
    
    scrollBtn.addEventListener('click', function() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth'
      });
    });
  }
</script>
</body>
</html>

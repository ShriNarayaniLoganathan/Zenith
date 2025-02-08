# Zenith
A desktop app that tracks expenses
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>SmartSpend - Your Journey to Better Spending Starts Here - Welcome to SmartSpend!</title>
  <style>
    /* Styling for the Welcome Message */
    h1 {
      text-align: center;
      font-size: 3em;
      margin-top: 50px;
      color: #333;
    }
.slideshow-container {
      position: relative;
      max-width: 100%;
      margin: auto;
.slides {
      display: none;
      width: 100%;
      height: 400px;
    }

    .slides img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    /* Navigation dots */
    .dot {
      height: 15px;
      width: 15px;
      margin: 0 4px;
      background-color: #bbb;
      border-radius: 50%;
      display: inline-block;
      transition: background-color 0.6s ease;
    }

    .active {
      background-color: #717171;
    }

    /* Optional: Button styling for login/signup */
    .login-signup-button {
      text-align: center;
      margin-top: 20px;
    }

    .login-signup-button a {
      padding: 10px 20px;
      background-color: #4CAF50;
      color: white;
      text-decoration: none;
      border-radius: 5px;
    }

    .login-signup-button a:hover {
      background-color: #45a049;
    }
  </style>
</head>
<body>

  <h1>Welcome to SmartSpend</h1>

  <!-- Slideshow Container -->
  <div class="slideshow-container">
    <div class="slides fade">
      <img src="C:\Users\hp\OneDrive\Desktop\Zenith\Zenith\IMG-20250208-WA0008.jpg" alt="Login Slide 1">
    </div>
    <div class="slides fade">
      <img src="C:\Users\hp\OneDrive\Desktop\Zenith\Zenith\IMG-20250208-WA0008.jpg" alt="Sign Up Slide 2">
    </div>
    <div class="slides fade">
      <img src="C:\Users\hp\OneDrive\Desktop\Zenith\Zenith\IMG-20250208-WA0008.jpg" alt="Login Slide 3">
    </div>

    <!-- Navigation dots -->
    <div style="text-align:center">
      <span class="dot"></span>
      <span class="dot"></span>
      <span class="dot"></span>
    </div>
  </div>

  <!-- Login/Signup Buttons -->
  <div class="login-signup-button">
    <a href="login.html">Login</a> | <a href="signup.html">Sign Up</a>
  </div>

  <script>
    let slideIndex = 0;

    // Function to show slides
    function showSlides() {
      let slides = document.getElementsByClassName("slides");
      let dots = document.getElementsByClassName("dot");

      for (let i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";  
      }

      slideIndex++;
      if (slideIndex > slides.length) { slideIndex = 1 }    

      for (let i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" active", "");
      }

      slides[slideIndex-1].style.display = "block";  
      dots[slideIndex-1].className += " active";

      setTimeout(showSlides, 3000); // Change slide every 3 seconds
    }

    showSlides(); // Initial call to start the slideshow
  </script>

</body>
</html>
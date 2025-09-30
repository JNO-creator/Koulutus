<html lang="fi">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Self-Help-You</title>
    <style>
      /* Reset default margin and padding */
      body, html {
        margin: 0;
        padding: 0;
        font-family: Arial, sans-serif;
      }

      /* Styling the navigation bar */
      .navbar {
        background-color: #e1705d;
        overflow: hidden;
        text-align: center;
      }

      .navbar a {
        display: inline-block;
        padding: 14px 20px;
        text-decoration: none;
        color: white;
        font-size: 14px;
        transition: background-color 0.3s ease;
      }

      .navbar a:hover {
        background-color: #ddd;
        color: black;
      }

      .navbar a.active {
        background-color: #0e194d;
        color: white;
      }

      .navbar .icon {
        z-index: 2;
        display: none;
        font-size: 27px;
        color: white;
        padding: 14px 20px;
        background-color: #0e194d;
        cursor: pointer;
      }

      @media screen and (max-width: 768px) {
        .navbar a {
          display: none;
          width: 100%;
          text-align: left;
          padding: 14px;
        }

        .navbar a.active {
          background-color: #0e194d;
          color: white;
        }

        .navbar .icon {
          display: block;
        }

        .navbar.responsive a {
          display: block;
        }

        .navbar.responsive .icon {
          position: absolute;
          right: 0;
          top: 0;
        }
      }

      .header {
        background-color: #0e194d;
        color: white;
        padding: 20px;
        text-align: center;
        position: relative;
        overflow: hidden;
      }

      .header h1 {
        display: inline-block;
        font-size: 27px;
        white-space: nowrap;
        animation: rollText 10s linear infinite;
        position: relative;
        z-index: 2;
      }

      @keyframes rollText {
        0% {
          transform: translateX(100%);
        }
        100% {
          transform: translateX(-100%);
        }
      }

      .intro-text {
        text-align: center;
        padding: 40px;
        background-color: #f0f0f0;
      }

      .intro-text h2 {
        font-size: 24px;
        color: #0e194d;
      }

      .intro-text p {
        font-size: 14px;
        color: #0e194d;
      }

      .box-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
        margin-top: 40px;
      }

      .box-container .box-image {
        grid-column: span 2;
      }

      .box {
        background-color: #0e194d;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3),
          -2px -2px 5px rgba(92, 97, 102, 0.5);
        border: 1px solid #ddd;
        border-radius: 8px;
        text-align: center;
        padding: 20px;
        transition: transform 0.3s ease;
      }

      .box h3 {
        margin-bottom: 15px;
        font-size: 24px;
        text-shadow: 2px 2px 5px black;
        color: #0e194d;
      }

      .box p {
        font-size: 14px;
        color: #0e194d;
      }

      .box:hover {
        transform: translateY(-10px);
      }

      .box-small {
        background-image: url('Pallot.jpg');
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3),
          -2px -2px 5px rgba(92, 97, 102, 0.5);
        padding: 20px;
        height: auto; /* Changed from fixed 150px */
        border-radius: 8px;
        text-align: center;
        transition: transform 0.3s ease;
      }

      .box-image {
        background-image: url('Kuva21.jpg');
        background-size: cover;
        background-position: center;
        color: #0e194d;
        padding: 100px;
        text-align: center;
        width: 100%;
        border-radius: 8px;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3),
          -2px -2px 5px rgba(92, 97, 102, 0.5);
      }

      .box-image h3 {
        margin-bottom: 40px;
        font-size: 24px;
        color: #e1705d;
      }

      .box-image p {
        font-size: 14px;
        color: #e1705d;
      }

      /* New spacing class for iframe */
      .video-wrapper {
        margin-top: 20px;
      }

      footer {
        background-color: #0e194d;
        box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3),
          -2px -2px 5px rgba(92, 97, 102, 0.5);
        border-radius: 8px;
        padding: 40px 20px;
        color: white;
        margin-top: 40px;
        text-align: center;
      }

      footer a {
        text-decoration: none;
        color: white;
        font-size: 16px;
        margin: 0 10px;
        transition: color 0.3s ease;
      }

      footer a:hover {
        color: #ff5733;
      }

      footer a:visited {
        color: #8e44ad;
      }

      .footer-bottom {
        padding-top: 10px;
      }

      section {
        padding-bottom: 40px;
      }
    </style>
  </head>
  <body>

    <!-- Top Navigation Bar placed before the header -->
    <div class="navbar" id="myNavbar">
      <a href="/Self-Help-You">Koti</a>
      <a href="/Meista">Meistä</a>
      <a href="/Yritys">Yritys</a>
      <a href="/Palvelut">Palvelut</a>
      <a href="#Koulutus" class="active">Koulutus</a>
      <a href="javascript:void(0);" class="icon" onclick="toggleNavbar()">&#9776;</a>
    </div>

    <!-- Header with rolling text effect -->
    <div class="header">
      <h1>Self-Help-You</h1>
    </div>

    <!-- New Text Section -->
    <div class="intro-text">
      <h2>Kouluttautuminen on avain tiedon löytymiseen ja sisäistämiseen</h2>
      <p>Haluamme poistaa digitaalisen eriarvoisuuden yhteiskuntamme rakenteista.</p>
    </div>

    <!-- Embedded Video Box -->
    <section>
      <div class="box-small">
        <h3>Tutustu koulutuksiimme</h3>
        <div class="video-wrapper">
          <iframe width="100%" height="100" src="https://www.youtube.com/embed/dQw4w9WgXcQ"
            title="Koulutusvideo" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen style="border-radius: 8px;">
          </iframe>
        </div>
      </div>
    </section>
        <!-- Form and Table Section -->
    <section>
      <div class="box-container">
        <!-- Form Box -->
        <div class="box-small" style="background-image: none; background-color: #f9f9f9;">
          <h3>Ota yhteyttä</h3>
          <form action="#" method="post" style="text-align: left; font-size: 14px;">
            <label for="name">Nimi:</label><br />
            <input type="text" id="name" name="name" style="width: 100%; padding: 5px; margin-bottom: 10px;" /><br />

            <label for="email">Sähköposti:</label><br />
            <input type="email" id="email" name="email" style="width: 100%; padding: 5px; margin-bottom: 10px;" /><br />

            <label for="message">Viesti:</label><br />
            <textarea id="message" name="message" rows="4" style="width: 100%; padding: 5px;"></textarea><br />

            <button type="submit" style="margin-top: 10px; padding: 8px 12px; background-color: #0e194d; color: white; border: none; border-radius: 4px; cursor: pointer;">Lähetä</button>
          </form>
        </div>

        <!-- Table Box -->
        <div class="box-small" style="background-image: none; background-color: #f9f9f9;">
          <h3>Koulutusohjelmat</h3>
          <table style="width: 100%; font-size: 14px; border-collapse: collapse;">
            <thead>
              <tr style="background-color: #e1705d; color: white;">
                <th style="padding: 8px; border: 1px solid #ccc;">Kurssi</th>
                <th style="padding: 8px; border: 1px solid #ccc;">Kesto</th>
              </tr>
            </thead>
            <tbody>
              <tr>
                <td style="padding: 8px; border: 1px solid #ccc;">Digitaidot 101</td>
                <td style="padding: 8px; border: 1px solid #ccc;">4 viikkoa</td>
              </tr>
              <tr>
                <td style="padding: 8px; border: 1px solid #ccc;">Tietoturva</td>
                <td style="padding: 8px; border: 1px solid #ccc;">2 viikkoa</td>
              </tr>
              <tr>
                <td style="padding: 8px; border: 1px solid #ccc;">Sosiaalinen media</td>
                <td style="padding: 8px; border: 1px solid #ccc;">3 viikkoa</td>
              </tr>
            </tbody>
          </table>
       </div>
          </div>
      </section>
       
      <!-- Footer -->
      <footer>
      <div class="footer-section contact">
    <h4>Self-Help-You - osana yrityksesi tulevaisuuden suunnittelua</h4>
    <a href="#Otayhteytta">Ota yhteyttä</a>
    <a href="#Sahkoposti">Sähköposti</a>
    <a href="#Kanavat">Kanavat</a>
    </div>
    <div class="footer-bottom">
    <p>&copy; 2025 Self-Help-You. Kaikki oikeudet pidätetään.</p>
    </div>
    </footer>
      <script>
          /* Function to toggle the navbar on small screens */
          function toggleNavbar() {
              var navbar = document.getElementById("myNavbar");
              navbar.classList.toggle("responsive");
          }
      </script>

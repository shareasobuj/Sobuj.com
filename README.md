# Sobuj.com

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Sobuj Travels</title>
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; }
    body { font-family: Arial, sans-serif; background: #f0f0f0; }
    header { background-color: #2d6a4f; color: white; padding: 20px; text-align: center; }
    nav a { color: white; margin: 0 15px; text-decoration: none; font-weight: bold; }
    .hero {
      background: url('https://images.unsplash.com/photo-1518684079-2ca5ec9eb271?auto=format&fit=crop&w=1600&q=60') center/cover no-repeat;
      height: 300px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 2.5rem;
      font-weight: bold;
      text-shadow: 2px 2px 8px #000;
    }
    .section { padding: 40px 20px; }
    .section h2 { text-align: center; margin-bottom: 30px; color: #1b4332; }
    .packages {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
      max-width: 1000px;
      margin: auto;
    }
    .card {
      background: white;
      padding: 15px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .card img {
      width: 100%;
      height: 160px;
      object-fit: cover;
      border-radius: 8px;
    }
    .card h3 { margin: 10px 0 5px; color: #2d6a4f; }
    .card p { font-size: 0.9rem; color: #555; }
    .contact-form {
      max-width: 500px;
      margin: auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    .contact-form input,
    .contact-form textarea {
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .contact-form button {
      background: #2d6a4f;
      color: white;
      border: none;
      padding: 12px 20px;
      border-radius: 5px;
      cursor: pointer;
    }
    .contact-form button:hover {
      background: #1b4332;
    }
    footer {
      background: #1b4332;
      color: white;
      text-align: center;
      padding: 15px;
      margin-top: 40px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Sobuj Travels</h1>
    <nav>
      <a href="#packages">Packages</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <div class="hero">
    Explore the World with Sobuj.com
  </div>

  <div class="section" id="packages">
    <h2>Our Travel Packages</h2>
    <div class="packages" id="packageContainer"></div>
  </div>

  <div class="section" id="contact">
    <h2>Contact Us</h2>
    <form class="contact-form" onsubmit="sendMessage(event)">
      <input type="text" placeholder="Your Name" required />
      <input type="email" placeholder="Your Email" required />
      <textarea rows="5" placeholder="Your Message" required></textarea>
      <button type="submit">Send Message</button>
    </form>
  </div>

  <footer>
    &copy; 2025 Sobuj Travels | All Rights Reserved
  </footer>

  <script>
    const packages = [
      {
        title: "Cox's Bazar Tour",
        image: "https://images.unsplash.com/photo-1607532941433-522cd002f9f5?auto=format&fit=crop&w=800&q=60",
        description: "3 Days 2 Nights beach package with hotel & meals included.",
      },
      {
        title: "Sajek Valley Adventure",
        image: "https://images.unsplash.com/photo-1695902188434-bd3c9baf39d5?auto=format&fit=crop&w=800&q=60",
        description: "2 Days jungle & hill trip with full local guidance.",
      },
      {
        title: "Sundarban Safari",
        image: "https://images.unsplash.com/photo-1613327448057-bf6f782a1224?auto=format&fit=crop&w=800&q=60",
        description: "Explore the largest mangrove forest and wildlife safari experience.",
      }
    ];

    const container = document.getElementById("packageContainer");

    packages.forEach(pkg => {
      const card = document.createElement("div");
      card.className = "card";
      card.innerHTML = `
        <img src="${pkg.image}" alt="${pkg.title}">
        <h3>${pkg.title}</h3>
        <p>${pkg.description}</p>
      `;
      container.appendChild(card);
    });

    function sendMessage(e) {
      e.preventDefault();
      alert("Thanks for contacting Sobuj Travels! We will get back to you soon.");
    }
  </script>

</body>
</html>

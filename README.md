<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0b0b0d">
  <title>Redline Auto Spa | Premium Car Care</title>
  <meta name="description" content="Premium car wash, detailing, wax polish and ceramic coating. Book your Redline Auto Spa appointment today.">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Outfit:wght@400;500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #0b0b0d;
      --surface: #121214;
      --surface-light: #19191d;
      --red: #c8102e;
      --red-bright: #ed1738;
      --text: #f6f3f2;
      --muted: #a4a1a1;
      --line: rgba(255,255,255,.1);
      --font-heading: "Outfit", sans-serif;
      --font-body: "DM Sans", sans-serif;
    }

    * { box-sizing: border-box; }
    html { scroll-behavior: smooth; scroll-padding-top: 85px; }
    body {
      margin: 0;
      background: var(--bg);
      color: var(--text);
      font-family: var(--font-body);
      line-height: 1.6;
    }
    a { color: inherit; text-decoration: none; }
    button, input, select, textarea { font: inherit; }
    img { display: block; max-width: 100%; }
    .container { width: min(1120px, calc(100% - 40px)); margin: 0 auto; }

    .topbar {
      background: var(--red);
      color: #fff;
      text-align: center;
      padding: 8px 16px;
      font-size: .82rem;
      font-weight: 600;
      letter-spacing: .04em;
    }
    header {
      position: sticky;
      top: 0;
      z-index: 20;
      background: rgba(11,11,13,.92);
      border-bottom: 1px solid var(--line);
      backdrop-filter: blur(14px);
    }
    .nav {
      min-height: 74px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 24px;
    }
    .logo {
      font-family: var(--font-heading);
      font-size: 1.35rem;
      font-weight: 800;
      letter-spacing: .03em;
      white-space: nowrap;
    }
    .logo span { color: var(--red-bright); }
    .nav-links { display: flex; align-items: center; gap: 28px; }
    .nav-links a { color: #d3d0d0; font-size: .91rem; transition: color .2s; }
    .nav-links a:hover { color: #fff; }
    .nav-toggle {
      display: none;
      color: #fff;
      background: none;
      border: 1px solid var(--line);
      border-radius: 8px;
      padding: 8px 11px;
      cursor: pointer;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      border: 1px solid transparent;
      border-radius: 7px;
      padding: 12px 19px;
      background: var(--red);
      color: white;
      font-weight: 700;
      transition: transform .2s, background .2s, border-color .2s;
      cursor: pointer;
    }
    .button:hover { background: var(--red-bright); transform: translateY(-2px); }
    .button-outline { background: transparent; border-color: rgba(255,255,255,.35); }
    .button-outline:hover { border-color: var(--red-bright); background: rgba(200,16,46,.12); }
    .button-small { padding: 9px 14px; font-size: .88rem; }

    .hero {
      min-height: 640px;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      background:
        linear-gradient(90deg, rgba(8,8,10,.97) 0%, rgba(8,8,10,.82) 48%, rgba(8,8,10,.28) 100%),
        linear-gradient(0deg, var(--bg) 0%, transparent 22%),
        url("https://images.unsplash.com/photo-1607860108855-64acf2078ed9?auto=format&fit=crop&w=2000&q=85") center 55% / cover;
    }
    .hero::after {
      content: "";
      position: absolute;
      width: 420px;
      height: 420px;
      right: -170px;
      top: 10%;
      border-radius: 50%;
      background: rgba(200,16,46,.2);
      filter: blur(90px);
      pointer-events: none;
    }
    .hero-content { position: relative; z-index: 1; max-width: 690px; padding: 90px 0 110px; }
    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      color: #ff657d;
      font-size: .78rem;
      font-weight: 700;
      letter-spacing: .18em;
      text-transform: uppercase;
    }
    .eyebrow::before { content: ""; height: 2px; width: 25px; background: var(--red-bright); }
    h1, h2, h3 { font-family: var(--font-heading); line-height: 1.12; }
    h1 { margin: 20px 0; font-size: clamp(3rem, 7vw, 5.7rem); letter-spacing: -.045em; }
    h1 span { color: var(--red-bright); }
    .hero p { color: #cbc7c7; max-width: 540px; font-size: 1.05rem; }
    .hero-actions { display: flex; flex-wrap: wrap; gap: 13px; margin-top: 30px; }
    .hero-note { display: flex; gap: 22px; flex-wrap: wrap; margin-top: 38px; color: #ddd; font-size: .88rem; }
    .hero-note span::before { content: "✓"; color: #ff526d; font-weight: 800; margin-right: 8px; }

    section { padding: 92px 0; }
    .section-heading { max-width: 670px; margin-bottom: 38px; }
    .section-heading h2 { margin: 12px 0; font-size: clamp(2.1rem, 4vw, 3.2rem); letter-spacing: -.035em; }
    .section-heading p { color: var(--muted); margin: 0; }
    .center { text-align: center; margin-left: auto; margin-right: auto; }
    .center .eyebrow { justify-content: center; }

    .stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      border: 1px solid var(--line);
      background: var(--surface);
      border-radius: 12px;
      margin-top: -1px;
      position: relative;
      z-index: 2;
    }
    .stat { text-align: center; padding: 24px 12px; }
    .stat + .stat { border-left: 1px solid var(--line); }
    .stat strong { display: block; color: #fff; font-family: var(--font-heading); font-size: 1.6rem; }
    .stat span { color: var(--muted); font-size: .85rem; }

    .packages { background: linear-gradient(180deg, #0b0b0d, #101012 45%, #0b0b0d); }
    .package-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 18px; align-items: stretch; }
    .package {
      display: flex;
      flex-direction: column;
      position: relative;
      padding: 27px;
      border: 1px solid var(--line);
      border-radius: 12px;
      background: var(--surface);
      transition: transform .2s, border-color .2s;
    }
    .package:hover { transform: translateY(-5px); border-color: rgba(237,23,56,.55); }
    .package.featured { border-color: var(--red); box-shadow: 0 0 35px rgba(200,16,46,.12); }
    .popular {
      position: absolute;
      right: 15px;
      top: 15px;
      background: var(--red);
      border-radius: 20px;
      padding: 5px 10px;
      font-size: .68rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: .07em;
    }
    .package h3 { margin: 0 0 7px; font-size: 1.4rem; }
    .package .description { min-height: 45px; margin: 0; color: var(--muted); font-size: .9rem; }
    .price { margin: 22px 0; font-family: var(--font-heading); font-size: 2.25rem; font-weight: 700; }
    .price small { color: var(--muted); font: 500 .82rem var(--font-body); }
    .package ul { list-style: none; padding: 0; margin: 0 0 25px; flex: 1; }
    .package li { color: #dedbdb; padding: 9px 0; border-bottom: 1px solid rgba(255,255,255,.07); font-size: .9rem; }
    .package li::before { content: "✓"; color: #ff526d; font-weight: 800; margin-right: 10px; }
    .package .button { width: 100%; }
    .price-note { text-align: center; margin-top: 22px; color: var(--muted); font-size: .82rem; }

    .services-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px; }
    .service {
      padding: 24px;
      border: 1px solid var(--line);
      background: var(--surface);
      border-radius: 10px;
    }
    .service-icon {
      display: grid;
      place-items: center;
      width: 46px;
      height: 46px;
      margin-bottom: 16px;
      background: rgba(200,16,46,.15);
      color: #ff536e;
      border-radius: 10px;
      font-size: 1.35rem;
    }
    .service h3 { margin: 0 0 7px; font-size: 1.1rem; }
    .service p { margin: 0; color: var(--muted); font-size: .89rem; }

    .process { background: #101012; }
    .steps { display: grid; grid-template-columns: repeat(3, 1fr); gap: 25px; }
    .step { border-top: 1px solid var(--line); padding-top: 20px; }
    .step-number { color: var(--red-bright); font-family: var(--font-heading); font-size: .9rem; font-weight: 800; letter-spacing: .1em; }
    .step h3 { margin: 10px 0 7px; font-size: 1.25rem; }
    .step p { margin: 0; color: var(--muted); font-size: .9rem; }

    .booking-wrap { display: grid; grid-template-columns: .85fr 1.15fr; gap: 55px; align-items: start; }
    .booking-copy h2 { margin: 12px 0; font-size: clamp(2.1rem, 4vw, 3rem); }
    .booking-copy p { color: var(--muted); }
    .contact-line { margin-top: 25px; color: #e4e0e0; }
    .contact-line strong { color: white; }
    .booking-form {
      padding: 27px;
      border: 1px solid var(--line);
      border-radius: 12px;
      background: var(--surface);
    }
    .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 15px; }
    .field { display: flex; flex-direction: column; gap: 7px; }
    .field.full { grid-column: 1 / -1; }
    label { color: #e7e3e3; font-size: .85rem; font-weight: 600; }
    input, select, textarea {
      width: 100%;
      padding: 12px 13px;
      color: #fff;
      background: #0d0d0f;
      border: 1px solid rgba(255,255,255,.13);
      border-radius: 6px;
      outline: none;
    }
    input:focus, select:focus, textarea:focus { border-color: var(--red-bright); }
    select option { background: #121214; }
    textarea { min-height: 90px; resize: vertical; }
    .booking-form .button { width: 100%; margin-top: 17px; }
    .form-message { display: none; margin: 13px 0 0; color: #8fe1a2; font-size: .9rem; }

    footer { border-top: 1px solid var(--line); background: #080809; padding: 27px 0; }
    .footer-inner { display: flex; align-items: center; justify-content: space-between; gap: 15px; flex-wrap: wrap; }
    .footer-inner p { color: var(--muted); margin: 0; font-size: .83rem; }
    .footer-links { display: flex; gap: 18px; color: #c7c3c3; font-size: .84rem; }

    @media (max-width: 820px) {
      .nav-links {
        display: none;
        position: absolute;
        left: 0;
        right: 0;
        top: 74px;
        padding: 18px 22px 22px;
        flex-direction: column;
        align-items: stretch;
        gap: 17px;
        background: #111113;
        border-bottom: 1px solid var(--line);
      }
      .nav-links.open { display: flex; }
      .nav-links .button { text-align: center; }
      .nav-toggle { display: block; }
      .package-grid { grid-template-columns: 1fr 1fr; }
      .package:last-child { grid-column: 1 / -1; }
      .booking-wrap { grid-template-columns: 1fr; gap: 25px; }
    }
    @media (max-width: 580px) {
      .container { width: min(100% - 30px, 1120px); }
      .hero { min-height: 590px; background-position: 58% center; }
      .hero-content { padding: 75px 0 88px; }
      .hero p { font-size: .97rem; }
      section { padding: 70px 0; }
      .stats { grid-template-columns: 1fr; }
      .stat + .stat { border-left: 0; border-top: 1px solid var(--line); }
      .package-grid, .services-grid, .steps { grid-template-columns: 1fr; }
      .package:last-child { grid-column: auto; }
      .package .description { min-height: 0; }
      .form-grid { grid-template-columns: 1fr; }
      .field.full { grid-column: auto; }
      .booking-form { padding: 20px; }
      .footer-inner { align-items: flex-start; flex-direction: column; }
    }
  </style>
</head>

<body>
  <div class="topbar">Premium car care, without compromise — Book your visit today</div>

  <header>
    <div class="container nav">
      <a class="logo" href="#home">REDLINE <span>AUTO SPA</span></a>
      <button class="nav-toggle" aria-label="Open navigation" aria-expanded="false">☰</button>
      <nav class="nav-links" aria-label="Main navigation">
        <a href="#packages">Packages</a>
        <a href="#services">Services</a>
        <a href="#process">How it works</a>
        <a href="#booking">Contact</a>
        <a class="button button-small" href="#booking">Book a wash <span>↗</span></a>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="home">
      <div class="container">
        <div class="hero-content">
          <span class="eyebrow">The Redline difference</span>
          <h1>Make every drive<br>feel <span>brand new.</span></h1>
          <p>From a quick, spotless wash to a full showroom-quality detail — give your car the care it deserves.</p>
          <div class="hero-actions">
            <a class="button" href="#packages">Explore packages <span>→</span></a>
            <a class="button button-outline" href="#booking">Book an appointment</a>
          </div>
          <div class="hero-note">
            <span>Careful hand wash</span>
            <span>Premium products</span>
            <span>Detailing experts</span>
          </div>
        </div>
      </div>
    </section>

    <div class="container">
      <div class="stats">
        <div class="stat"><strong>Premium</strong><span>Quality products</span></div>
        <div class="stat"><strong>Expert care</strong><span>For every vehicle</span></div>
        <div class="stat"><strong>Made easy</strong><span>Simple booking</span></div>
      </div>
    </div>

    <section class="packages" id="packages">
      <div class="container">
        <div class="section-heading center">
          <span class="eyebrow">Our packages</span>
          <h2>Choose your shine.</h2>
          <p>Simple packages for every car and every kind of day. Prices below are sample rates in PKR.</p>
        </div>

        <div class="package-grid">
          <article class="package">
            <h3>Essential Wash</h3>
            <p class="description">A fresh, clean car — inside and out.</p>
            <div class="price">Rs. 1,500 <small>/ from</small></div>
            <ul>
              <li>Exterior hand wash</li>
              <li>Wheel and tyre cleaning</li>
              <li>Interior vacuum</li>
              <li>Dashboard wipe-down</li>
              <li>Window cleaning</li>
            </ul>
            <a class="button button-outline" href="#booking" data-package="Essential Wash">Choose package</a>
          </article>

          <article class="package featured">
            <span class="popular">Most popular</span>
            <h3>Signature Detail</h3>
            <p class="description">A deeper clean with a brilliant finish.</p>
            <div class="price">Rs. 4,500 <small>/ from</small></div>
            <ul>
              <li>Everything in Essential Wash</li>
              <li>Interior deep cleaning</li>
              <li>Wax polish finish</li>
              <li>Tyre dressing</li>
              <li>Door jamb cleaning</li>
              <li>Fresh interior fragrance</li>
            </ul>
            <a class="button" href="#booking" data-package="Signature Detail">Choose package</a>
          </article>

          <article class="package">
            <h3>Ultimate Protection</h3>
            <p class="description">Maximum gloss, care and lasting protection.</p>
            <div class="price">Rs. 12,000 <small>/ from</small></div>
            <ul>
              <li>Everything in Signature Detail</li>
              <li>Paint decontamination</li>
              <li>Machine polish</li>
              <li>Premium paint sealant</li>
              <li>Leather conditioning</li>
              <li>Engine bay cleaning</li>
            </ul>
            <a class="button button-outline" href="#booking" data-package="Ultimate Protection">Choose package</a>
          </article>
        </div>
        <p class="price-note">Final price may vary depending on vehicle size and condition. Please confirm when booking.</p>
      </div>
    </section>

    <section id="services">
      <div class="container">
        <div class="section-heading">
          <span class="eyebrow">More than a wash</span>
          <h2>Complete care for your car.</h2>
          <p>Pick a package or ask us about individual services to keep your car looking its best.</p>
        </div>
        <div class="services-grid">
          <article class="service">
            <div class="service-icon">✦</div>
            <h3>Wax & polish</h3>
            <p>Bring back the paint's shine and add a layer of protection against everyday dirt.</p>
          </article>
          <article class="service">
            <div class="service-icon">◈</div>
            <h3>Interior detailing</h3>
            <p>Deep cleaning for seats, carpets, dashboard and those hard-to-reach spots.</p>
          </article>
          <article class="service">
            <div class="service-icon">◉</div>
            <h3>Ceramic coating</h3>
            <p>Long-lasting gloss and paint protection. Ask us for a vehicle-specific quote.</p>
          </article>
          <article class="service">
            <div class="service-icon">⌁</div>
            <h3>Engine bay cleaning</h3>
            <p>Careful cleaning to make your engine bay look neat and well-maintained.</p>
          </article>
          <article class="service">
            <div class="service-icon">◇</div>
            <h3>Headlight restoration</h3>
            <p>Help cloudy headlights look clearer and give your car a fresher appearance.</p>
          </article>
          <article class="service">
            <div class="service-icon">✧</div>
            <h3>Tyre & wheel care</h3>
            <p>Remove built-up grime and finish with a clean, rich look for your wheels.</p>
          </article>
        </div>
      </div>
    </section>

    <section class="process" id="process">
      <div class="container">
        <div class="section-heading">
          <span class="eyebrow">Easy as 1, 2, 3</span>
          <h2>Your clean-car day, sorted.</h2>
        </div>
        <div class="steps">
          <article class="step">
            <span class="step-number">STEP 01</span>
            <h3>Pick your package</h3>
            <p>Choose the service that fits your car and the result you're after.</p>
          </article>
          <article class="step">
            <span class="step-number">STEP 02</span>
            <h3>Send a booking request</h3>
            <p>Tell us your preferred date and vehicle details using the form below.</p>
          </article>
          <article class="step">
            <span class="step-number">STEP 03</span>
            <h3>Show up and shine</h3>
            <p>Bring your car in and let our team take care of the rest.</p>
          </article>
        </div>
      </div>
    </section>

    <section id="booking">
      <div class="container booking-wrap">
        <div class="booking-copy">
          <span class="eyebrow">Let’s get you booked</span>
          <h2>Ready for that fresh-car feeling?</h2>
          <p>Fill in the form with your preferred package and we’ll be ready to confirm your appointment.</p>
          <div class="contact-line"><strong>Location:</strong> Your City, Pakistan</div>
          <div class="contact-line"><strong>Hours:</strong> Monday – Sunday, 10:00 AM – 10:00 PM</div>
          <div class="contact-line"><strong>Phone:</strong> +92 300 1234567</div>
        </div>

        <form class="booking-form" id="bookingForm">
          <div class="form-grid">
            <div class="field">
              <label for="name">Your name</label>
              <input id="name" name="name" type="text" placeholder="e.g. Ali Khan" required>
            </div>
            <div class="field">
              <label for="phone">Phone number</label>
              <input id="phone" name="phone" type="tel" placeholder="+92 300 1234567" required>
            </div>
            <div class="field">
              <label for="vehicle">Vehicle</label>
              <input id="vehicle" name="vehicle" type="text" placeholder="e.g. Honda Civic" required>
            </div>
            <div class="field">
              <label for="package">Choose a package</label>
              <select id="package" name="package" required>
                <option value="">Select a package</option>
                <option>Essential Wash</option>
                <option>Signature Detail</option>
                <option>Ultimate Protection</option>
                <option>Individual service</option>
              </select>
            </div>
            <div class="field full">
              <label for="date">Preferred date</label>
              <input id="date" name="date" type="date" required>
            </div>
            <div class="field full">
              <label for="notes">Anything else? (optional)</label>
              <textarea id="notes" name="notes" placeholder="Tell us about your car or the service you need"></textarea>
            </div>
          </div>
          <button class="button" type="submit">Request a booking <span>→</span></button>
          <p class="form-message" id="formMessage" role="status">Thanks! Your sample booking request has been received.</p>
        </form>
      </div>
    </section>
  </main>

  <footer>
    <div class="container footer-inner">
      <a class="logo" href="#home">REDLINE <span>AUTO SPA</span></a>
      <p>© <span id="year"></span> Redline Auto Spa. Sample website — update contact details before publishing.</p>
      <div class="footer-links">
        <a href="#packages">Packages</a>
        <a href="#services">Services</a>
        <a href="#booking">Book now</a>
      </div>
    </div>
  </footer>

  <script>
    const navToggle = document.querySelector(".nav-toggle");
    const navLinks = document.querySelector(".nav-links");

    navToggle.addEventListener("click", () => {
      const isOpen = navLinks.classList.toggle("open");
      navToggle.setAttribute("aria-expanded", String(isOpen));
      navToggle.textContent = isOpen ? "✕" : "☰";
    });

    document.querySelectorAll(".nav-links a").forEach((link) => {
      link.addEventListener("click", () => {
        navLinks.classList.remove("open");
        navToggle.setAttribute("aria-expanded", "false");
        navToggle.textContent = "☰";
      });
    });

    document.querySelectorAll("[data-package]").forEach((button) => {
      button.addEventListener("click", () => {
        document.querySelector("#package").value = button.dataset.package;
      });
    });

    document.querySelector("#bookingForm").addEventListener("submit", (event) => {
      event.preventDefault();
      document.querySelector("#formMessage").style.display = "block";
      event.target.reset();
    });

    document.querySelector("#year").textContent = new Date().getFullYear();
    document.querySelector("#date").min = new Date().toISOString().split("T")[0];
  </script>
</body>
</html>

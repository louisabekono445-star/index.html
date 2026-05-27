<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Leandra Studio | African Hair Braiding & Beauty</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root {
      --primary: #c89b3c;   /* gold */
      --primary-dark: #8a6b24;
      --accent: #e75480;    /* pink */
      --bg: #050505;
      --text: #f7f7f7;
      --muted: #bbbbbb;
      --card-bg: #111111;
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: radial-gradient(circle at top, #1b1b1b 0, #050505 55%, #000 100%);
      color: var(--text);
      line-height: 1.6;
    }
    a { color: inherit; text-decoration: none; }
    img { max-width: 100%; display: block; }

    header {
      padding: 1.5rem 1.5rem 0.5rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 20;
      background: linear-gradient(to bottom, rgba(0,0,0,0.9), rgba(0,0,0,0.4), transparent);
      backdrop-filter: blur(10px);
    }
    .logo {
      font-weight: 700;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      font-size: 0.9rem;
    }
    .logo span {
      color: var(--primary);
    }
    nav a {
      margin-left: 1.2rem;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--muted);
    }
    nav a:hover { color: var(--primary); }

    .hero {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 2.5rem;
      padding: 3rem 1.5rem 4rem;
      max-width: 1100px;
      margin: 0 auto;
      align-items: center;
    }
    .hero-tag {
      text-transform: uppercase;
      letter-spacing: 0.25em;
      font-size: 0.75rem;
      color: var(--accent);
      margin-bottom: 0.75rem;
    }
    .hero h1 {
      font-size: clamp(2.4rem, 4vw, 3.2rem);
      line-height: 1.1;
      margin-bottom: 1rem;
    }
    .hero h1 span {
      color: var(--primary);
    }
    .hero-sub {
      font-size: 0.98rem;
      color: var(--muted);
      max-width: 30rem;
      margin-bottom: 1.5rem;
    }
    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-bottom: 1.75rem;
    }
    .badge {
      border-radius: 999px;
      border: 1px solid rgba(200,155,60,0.4);
      padding: 0.25rem 0.75rem;
      font-size: 0.75rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--muted);
    }
    .hero-cta {
      display: flex;
      flex-wrap: wrap;
      gap: 0.75rem;
      align-items: center;
      margin-bottom: 1.5rem;
    }
    .btn-primary {
      background: linear-gradient(135deg, var(--primary), var(--accent));
      border-radius: 999px;
      padding: 0.7rem 1.6rem;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      border: none;
      cursor: pointer;
      color: #000;
      font-weight: 600;
    }
    .btn-primary:hover {
      filter: brightness(1.05);
    }
    .btn-ghost {
      border-radius: 999px;
      padding: 0.7rem 1.4rem;
      font-size: 0.85rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      border: 1px solid rgba(255,255,255,0.18);
      background: transparent;
      cursor: pointer;
      color: var(--muted);
    }
    .btn-ghost:hover {
      border-color: var(--primary);
      color: var(--primary);
    }
    .hero-meta {
      font-size: 0.8rem;
      color: var(--muted);
    }
    .hero-meta strong { color: var(--text); }

    .hero-right {
      position: relative;
    }
    .hero-card {
      background: radial-gradient(circle at top, #222 0, #111 55%, #050505 100%);
      border-radius: 1.5rem;
      padding: 1.25rem;
      border: 1px solid rgba(255,255,255,0.08);
      box-shadow: 0 24px 60px rgba(0,0,0,0.8);
    }
    .hero-card-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.75rem;
    }
    .hero-card-title {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      color: var(--muted);
    }
    .hero-card-pill {
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--accent);
      border-radius: 999px;
      border: 1px solid rgba(231,84,128,0.5);
      padding: 0.2rem 0.7rem;
    }
    .hero-card-main {
      display: grid;
      grid-template-columns: 1.1fr 1fr;
      gap: 0.75rem;
      align-items: center;
    }
    .hero-card-main h2 {
      font-size: 1.1rem;
      margin-bottom: 0.25rem;
    }
    .hero-card-main p {
      font-size: 0.8rem;
      color: var(--muted);
      margin-bottom: 0.5rem;
    }
    .hero-card-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.35rem;
      margin-bottom: 0.5rem;
    }
    .hero-card-tag {
      font-size: 0.7rem;
      padding: 0.15rem 0.55rem;
      border-radius: 999px;
      background: rgba(255,255,255,0.04);
      border: 1px solid rgba(255,255,255,0.06);
      color: var(--muted);
    }
    .hero-card-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 0.75rem;
      font-size: 0.75rem;
      color: var(--muted);
    }
    .hero-card-footer span strong {
      color: var(--primary);
    }
    .hero-card-photo {
      border-radius: 1.1rem;
      background: linear-gradient(145deg, #333, #111);
      height: 190px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--muted);
      font-size: 0.8rem;
      text-align: center;
      padding: 0.75rem;
      border: 1px solid rgba(255,255,255,0.06);
    }

    section {
      padding: 3rem 1.5rem;
      max-width: 1100px;
      margin: 0 auto;
    }
    .section-title {
      text-transform: uppercase;
      letter-spacing: 0.22em;
      font-size: 0.8rem;
      color: var(--accent);
      margin-bottom: 0.4rem;
    }
    .section-heading {
      font-size: 1.6rem;
      margin-bottom: 0.75rem;
    }
    .section-sub {
      font-size: 0.95rem;
      color: var(--muted);
      max-width: 34rem;
      margin-bottom: 1.75rem;
    }

    .about-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 2rem;
    }
    .about-card {
      background: var(--card-bg);
      border-radius: 1.2rem;
      padding: 1.5rem;
      border: 1px solid rgba(255,255,255,0.06);
    }
    .about-card h3 {
      font-size: 1rem;
      margin-bottom: 0.5rem;
    }
    .about-card p {
      font-size: 0.9rem;
      color: var(--muted);
    }
    .about-list {
      list-style: none;
      margin-top: 0.75rem;
      font-size: 0.85rem;
      color: var(--muted);
    }
    .about-list li::before {
      content: "• ";
      color: var(--primary);
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(230px, 1fr));
      gap: 1.25rem;
    }
    .service-card {
      background: var(--card-bg);
      border-radius: 1rem;
      padding: 1rem 1.1rem;
      border: 1px solid rgba(255,255,255,0.06);
      font-size: 0.9rem;
    }
    .service-card h3 {
      font-size: 0.95rem;
      margin-bottom: 0.25rem;
    }
    .service-meta {
      font-size: 0.8rem;
      color: var(--muted);
      margin-bottom: 0.4rem;
    }
    .service-price {
      font-size: 0.9rem;
      color: var(--primary);
      margin-bottom: 0.4rem;
    }
    .service-note {
      font-size: 0.75rem;
      color: var(--muted);
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
      gap: 1rem;
    }
    .gallery-item {
      background: var(--card-bg);
      border-radius: 0.9rem;
      padding: 0.8rem;
      border: 1px solid rgba(255,255,255,0.06);
      font-size: 0.8rem;
      color: var(--muted);
      text-align: center;
    }
    .gallery-thumb {
      border-radius: 0.7rem;
      background: linear-gradient(135deg, #333, #111);
      height: 140px;
      margin-bottom: 0.5rem;
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 0.5rem;
    }
    .gallery-label {
      font-size: 0.8rem;
      color: var(--text);
    }

    .booking-layout {
      display: grid;
      grid-template-columns: minmax(0, 1.2fr) minmax(0, 1fr);
      gap: 2rem;
    }
    .booking-card {
      background: var(--card-bg);
      border-radius: 1.1rem;
      padding: 1.25rem;
      border: 1px solid rgba(255,255,255,0.06);
      font-size: 0.85rem;
    }
    .booking-card label {
      display: block;
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.14em;
      color: var(--muted);
      margin-bottom: 0.25rem;
    }
    .booking-card select,
    .booking-card input,
    .booking-card textarea {
      width: 100%;
      padding: 0.55rem 0.6rem;
      border-radius: 0.6rem;
      border: 1px solid rgba(255,255,255,0.12);
      background: #050505;
      color: var(--text);
      font-size: 0.85rem;
      margin-bottom: 0.75rem;
    }
    .booking-card small {
      font-size: 0.7rem;
      color: var(--muted);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.1fr) minmax(0, 1fr);
      gap: 2rem;
    }
    .contact-card {
      background: var(--card-bg);
      border-radius: 1.1rem;
      padding: 1.25rem;
      border: 1px solid rgba(255,255,255,0.06);
      font-size: 0.9rem;
      color: var(--muted);
    }
    .contact-card h3 {
      font-size: 1rem;
      margin-bottom: 0.5rem;
      color: var(--text);
    }
    .contact-line {
      margin-bottom: 0.4rem;
      font-size: 0.9rem;
    }
    .contact-label {
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-size: 0.7rem;
      color: var(--muted);
    }
    .contact-value {
      font-size: 0.9rem;
      color: var(--text);
    }
    .social-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin-top: 0.5rem;
      font-size: 0.8rem;
    }
    .social-pill {
      border-radius: 999px;
      border: 1px solid rgba(255,255,255,0.12);
      padding: 0.25rem 0.7rem;
      color: var(--muted);
    }

    footer {
      padding: 1.5rem;
      text-align: center;
      font-size: 0.75rem;
      color: var(--muted);
      border-top: 1px solid rgba(255,255,255,0.08);
      margin-top: 2rem;
    }

    @media (max-width: 800px) {
      .hero, .about-grid, .booking-layout, .contact-grid {
        grid-template-columns: 1fr;
      }
      header {
        flex-direction: column;
        align-items: flex-start;
        gap: 0.5rem;
      }
      nav {
        display: flex;
        flex-wrap: wrap;
      }
      .hero {
        padding-top: 2rem;
      }
    }
  </style>
</head>
<body>

<header>
  <div class="logo"><span>Leandra</span> Studio</div>
  <nav>
    <a href="#about">About</a>
    <a href="#services">Services</a>
    <a href="#gallery">Gallery</a>
    <a href="#booking">Book</a>
    <a href="#contact">Contact</a>
  </nav>
</header>

<main>
  <!-- HERO -->
  <section class="hero" id="home">
    <div>
      <div class="hero-tag">African hair braiding & beauty · Chicago</div>
      <h1>Enhance your beauty with <span>Leandra Studio</span></h1>
      <p class="hero-sub">
        Professional braids for women, men, and kids. Clean, precise, long‑lasting styles that keep you looking flawless.
      </p>
      <div class="hero-badges">
        <div class="badge">Style · Elegance · Confidence</div>
        <div class="badge">All styles · All occasions</div>
        <div class="badge">Satisfaction guaranteed</div>
      </div>
      <div class="hero-cta">
        <button class="btn-primary" onclick="document.getElementById('booking').scrollIntoView({behavior:'smooth'})">
          Book appointment
        </button>
        <button class="btn-ghost" onclick="document.getElementById('gallery').scrollIntoView({behavior:'smooth'})">
          View styles
        </button>
      </div>
      <div class="hero-meta">
        <div><strong>Address:</strong> 8153 S Colfax Ave, Apt 1, Chicago, IL 60617</div>
        <div><strong>Phone:</strong> 872‑325‑6833</div>
      </div>
    </div>

    <div class="hero-right">
      <div class="hero-card">
        <div class="hero-card-header">
          <div class="hero-card-title">Featured styles</div>
          <div class="hero-card-pill">Your style, my passion</div>
        </div>
        <div class="hero-card-main">
          <div>
            <h2>Knotless · Box · Boho</h2>
            <p>Choose from a curated selection of braids designed to match your personality and lifestyle.</p>
            <div class="hero-card-tags">
              <div class="hero-card-tag">Knotless braids</div>
              <div class="hero-card-tag">Box braids</div>
              <div class="hero-card-tag">Goddess / Boho</div>
              <div class="hero-card-tag">Cornrows</div>
              <div class="hero-card-tag">Men & kids</div>
            </div>
            <div class="hero-card-footer">
              <span>From <strong>$40</strong> · Kids, men & women</span>
              <span>Clean · Hygienic · On‑time</span>
            </div>
          </div>
          <div class="hero-card-photo">
            Upload your best hairstyle photo here to showcase your work.
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="section-title">About</div>
    <div class="section-heading">Meet Clotilde Louisa Bekono</div>
    <p class="section-sub">
      I am a professional hair stylist and braider, dedicated to creating styles that highlight your natural beauty and
      give you confidence every time you look in the mirror.
    </p>

    <div class="about-grid">
      <div>
        <div class="about-card">
          <h3>Leandra Studio · African Hair Braiding & Beauty</h3>
          <p>
            At Leandra Studio, every braid is done with care, precision, and passion. From classic box braids to modern
            knotless and boho styles, I focus on protective, long‑lasting looks that feel as good as they look.
          </p>
          <ul class="about-list">
            <li>Clean & hygienic environment</li>
            <li>On‑time appointments</li>
            <li>Personalized advice and attentive listening</li>
            <li>Styles for all ages and hair types</li>
          </ul>
        </div>
      </div>
      <div>
        <div class="about-card">
          <h3>Your style, my passion</h3>
          <p>
            Whether you’re getting ready for work, vacation, a special event, or just a fresh new look, I work with you
            to choose the right style, length, and size for your hair and lifestyle.
          </p>
          <p style="margin-top:0.6rem;">
            Book your appointment and experience professional quality, neat parts, and long‑lasting results.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- SERVICES -->
  <section id="services">
    <div class="section-title">Services & pricing</div>
    <div class="section-heading">Braids for her & him</div>
    <p class="section-sub">
      Below are sample price ranges. Final price depends on length, size, and hair density. Contact me if you have
      questions or want a custom style.
    </p>

    <div class="services-grid">
      <div class="service-card">
        <h3>Knotless braids (small)</h3>
        <div class="service-meta">Mid‑back length · Women</div>
        <div class="service-price">$220 – $280</div>
        <div class="service-note">Lightweight, flexible, and gentle on your scalp.</div>
      </div>
      <div class="service-card">
        <h3>Knotless braids (medium)</h3>
        <div class="service-meta">Mid‑back length · Women</div>
        <div class="service-price">$180 – $220</div>
        <div class="service-note">Perfect balance of fullness and time.</div>
      </div>
      <div class="service-card">
        <h3>Knotless braids (large)</h3>
        <div class="service-meta">Shoulder to mid‑back</div>
        <div class="service-price">$140 – $180</div>
        <div class="service-note">Bold, beautiful, and quicker to install.</div>
      </div>
      <div class="service-card">
        <h3>Box braids</h3>
        <div class="service-meta">Small · Medium · Large</div>
        <div class="service-price">$140 – $250</div>
        <div class="service-note">Classic, versatile braids for any occasion.</div>
      </div>
      <div class="service-card">
        <h3>Goddess / Boho braids</h3>
        <div class="service-meta">Curly ends · Boho finish</div>
        <div class="service-price">$200 – $300</div>
        <div class="service-note">Soft, romantic, and full of movement.</div>
      </div>
      <div class="service-card">
        <h3>Tribal braids</h3>
        <div class="service-meta">Middle part · Feed‑in</div>
        <div class="service-price">$180 – $260</div>
        <div class="service-note">Statement styles inspired by African heritage.</div>
      </div>
      <div class="service-card">
        <h3>Cornrows (women)</h3>
        <div class="service-meta">Straight back · Designs</div>
        <div class="service-price">$60 – $120</div>
        <div class="service-note">Clean, sleek, and protective.</div>
      </div>
      <div class="service-card">
        <h3>Cornrows (men)</h3>
        <div class="service-meta">Straight back · Designs</div>
        <div class="service-price">$40 – $100</div>
        <div class="service-note">Sharp, neat braids for men.</div>
      </div>
      <div class="service-card">
        <h3>Kids’ braids</h3>
        <div class="service-meta">Ages 4–12</div>
        <div class="service-price">$40 – $120</div>
        <div class="service-note">Gentle, cute, and age‑appropriate styles.</div>
      </div>
      <div class="service-card">
        <h3>Braids with extensions</h3>
        <div class="service-meta">Hair can be provided</div>
        <div class="service-price">+ $20 – $40</div>
        <div class="service-note">Ask about available colors and lengths.</div>
      </div>
      <div class="service-card">
        <h3>Touch‑ups</h3>
        <div class="service-meta">Front or perimeter</div>
        <div class="service-price">$40 – $80</div>
        <div class="service-note">Refresh your style and extend wear time.</div>
      </div>
    </div>
  </section>

  <!-- GALLERY -->
  <section id="gallery">
    <div class="section-title">Gallery</div>
    <div class="section-heading">Hairstyle inspiration</div>
    <p class="section-sub">
      Replace the placeholders below with your own photos. Use clear, well‑lit images that show neat parts, clean
      braids, and different angles.
    </p>

    <div class="gallery-grid">
      <div class="gallery-item">
        <div class="gallery-thumb">Knotless braids photo placeholder</div>
        <div class="gallery-label">Knotless braids</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Box braids photo placeholder</div>
        <div class="gallery-label">Box braids</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Goddess / Boho braids photo placeholder</div>
        <div class="gallery-label">Goddess / Boho braids</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Tribal braids photo placeholder</div>
        <div class="gallery-label">Tribal braids</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Cornrows (men) photo placeholder</div>
        <div class="gallery-label">Cornrows for men</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Cornrows (women) photo placeholder</div>
        <div class="gallery-label">Cornrows for women</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Kids’ braids photo placeholder</div>
        <div class="gallery-label">Kids’ braids</div>
      </div>
      <div class="gallery-item">
        <div class="gallery-thumb">Passion twists / Senegalese twists photo placeholder</div>
        <div class="gallery-label">Twists & more</div>
      </div>
    </div>
  </section>

  <!-- BOOKING -->
  <section id="booking">
    <div class="section-title">Booking</div>
    <div class="section-heading">Book your appointment</div>
    <p class="section-sub">
      Choose your style, date, and time. This form is a placeholder—your booking link (Square, Fresha, Acuity, etc.)
      can be connected to the “Confirm booking” button.
    </p>

    <div class="booking-layout">
      <div class="booking-card">
        <label for="style">Style</label>
        <select id="style">
          <option>Knotless braids</option>
          <option>Box braids</option>
          <option>Goddess / Boho braids</option>
          <option>Tribal braids</option>
          <option>Cornrows (women)</option>
          <option>Cornrows (men)</option>
          <option>Kids’ braids</option>
          <option>Other / custom style</option>
        </select>

        <label for="size">Size / length</label>
        <select id="size">
          <option>Small · Mid‑back</option>
          <option>Medium · Mid‑back</option>
          <option>Large · Shoulder / mid‑back</option>
          <option>Short / bob</option>
          <option>Waist length</option>
        </select>

        <label for="date">Preferred date</label>
        <input type="date" id="date" />

        <label for="time">Preferred time</label>
        <input type="time" id="time" />

        <label for="notes">Notes</label>
        <textarea id="notes" rows="3" placeholder="Tell me about your hair, color preference, or any questions."></textarea>

        <button class="btn-primary" style="margin-top:0.5rem;">Confirm booking (placeholder)</button>
        <small>
          After your booking system is set up, this button will redirect clients to your official booking page.
        </small>
      </div>

      <div class="booking-card">
        <h3 style="margin-bottom:0.5rem;">Booking tips</h3>
        <p>
          Please arrive with your hair clean, detangled, and product‑free unless we’ve discussed a wash service.
        </p>
        <p style="margin-top:0.5rem;">
          A deposit may be required to secure your appointment. Late arrivals and cancellations are subject to studio
          policy.
        </p>
        <p style="margin-top:0.75rem; font-size:0.8rem; color:var(--muted);">
          For same‑day or urgent appointments, call or text:
          <strong style="color:var(--primary);">872‑325‑6833</strong>.
        </p>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <div class="section-title">Contact</div>
    <div class="section-heading">Visit Leandra Studio</div>
    <p class="section-sub">
      Have questions about a style, price, or availability? Reach out and I’ll be happy to help.
    </p>

    <div class="contact-grid">
      <div class="contact-card">
        <h3>Studio details</h3>
        <div class="contact-line">
          <div class="contact-label">Address</div>
          <div class="contact-value">8153 S Colfax Ave, Apt 1, Chicago, IL 60617</div>
        </div>
        <div class="contact-line">
          <div class="contact-label">Phone</div>
          <div class="contact-value">872‑325‑6833</div>
        </div>
        <div class="contact-line">
          <div class="contact-label">Hours</div>
          <div class="contact-value">By appointment · Call or text to confirm availability.</div>
        </div>
      </div>

      <div class="contact-card">
        <h3>Follow Leandra Studio</h3>
        <p>Stay updated with new styles, promotions, and behind‑the‑scenes content.</p>
        <div class="social-row">
          <div class="social-pill">Instagram</div>
          <div class="social-pill">TikTok</div>
          <div class="social-pill">Facebook</div>
          <div class="social-pill">YouTube</div>
        </div>
        <p style="margin-top:0.75rem; font-size:0.8rem;">
          Once your social media handles are ready, they can be linked here so clients can tap and follow.
        </p>
      </div>
    </div>
  </section>
</main>

<footer>
  © Leandra Studio · African Hair Braiding & Beauty · Chicago, IL
</footer>

</body>
</html>

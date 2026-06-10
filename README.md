# AS GEO ZEMİN — Corporate Website

Official website of **AS GEO ZEMİN Laboratuvar Mühendislik İnşaat Müşavirlik Sondaj Maden Tic. Ltd. Şti.**, a geotechnical engineering and soil investigation firm with over 20 years of experience in the Marmara Region of Turkey.

**Live site:** [www.asgeozemin.com](http://www.asgeozemin.com)

![Homepage Screenshot](https://github.com/user-attachments/assets/1d98f50e-cc98-4856-93a5-f2ca07399602)

---

## Overview

A responsive, multi-page static website built with vanilla HTML, CSS, and JavaScript. It includes a dynamic component system for shared navbar and footer, a contact form backed by PHP (PHPMailer + Telegram Bot API), an image gallery with lightbox and filtering, and a hero section with an animated slider.

---

## Project Structure

```
/
├── index.html          # Home page
├── about.html          # Corporate — about, vision, mission
├── services.html       # Services — soil survey, drilling, lab, mining
├── projects.html       # Projects — filterable photo gallery
├── references.html     # References — clients, testimonials, certificates
├── contact.html        # Contact — form, map, FAQ
│
├── assets/
│   ├── images/         # Photography and hero slider images
│   └── icons/          # Favicons and logo
│
├── styles/
│   ├── style.css       # Global reset and shared styles
│   ├── navbar.css      # Header and navigation
│   ├── footer.css      # Footer
│   ├── home.css        # Home page
│   ├── about.css       # About page
│   ├── services.css    # Services page
│   ├── projects.css    # Projects gallery page
│   ├── references.css  # References page
│   └── contact.css     # Contact page
│
├── js/
│   └── script.js       # Hero slider, animations, scroll effects
│
├── components/
│   ├── navbar.html     # Shared navbar markup (loaded dynamically)
│   ├── footer.html     # Shared footer markup (loaded dynamically)
│   ├── favicon.html    # Favicon link tags (loaded into <head>)
│   └── component-loader.js  # Fetch-based component loader
│
├── contact-submit.php  # Form handler — sends email (PHPMailer) + Telegram notification
├── mail-config.php     # SMTP credentials and mail settings (not committed)
├── favicon.ico
├── LICENSE
└── README.md
```

---

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero slider, services preview, news, announcements |
| About | `about.html` | Company history, vision, mission, principles, statistics |
| Services | `services.html` | Soil survey, drilling, laboratory analysis, mining consulting |
| Projects | `projects.html` | Filterable photo gallery with lightbox (Sondaj, Pressiometre, MASW, Rezistivite) |
| References | `references.html` | Client sectors, testimonials, success stories, certifications |
| Contact | `contact.html` | Contact form, office map, FAQ, quick-contact buttons |

---

## Tech Stack

- **HTML5** — Semantic markup, ARIA-friendly structure
- **CSS3** — Custom properties, Flexbox, Grid, animations (no framework)
- **Vanilla JavaScript** — ES6+, IntersectionObserver, Fetch API
- **PHP** — Form submission handler (server-side validation, PHPMailer, Telegram Bot)
- **Font Awesome 6** — Icon library (CDN)
- **Google Fonts** — Inter typeface (CDN)

---

## Features

- **Responsive design** — Mobile-first, works on all screen sizes
- **Dynamic components** — Navbar and footer loaded via `fetch()` to avoid duplication
- **Hero slider** — Auto-advancing with keyboard, touch/swipe, and dot navigation
- **Gallery** — Category filter buttons, lightbox modal, lazy loading, load-more pagination
- **Contact form** — Client-side validation, AJAX submission, email + Telegram notification
- **Animations** — Scroll-triggered fade-in, parallax floating elements, counter animation
- **Accessibility** — Focus management, ARIA attributes, keyboard navigation

---

## Getting Started

### Static preview (no PHP)

Open `index.html` directly in a browser or serve with any static file server:

```bash
npx serve .
# or
python -m http.server 8000
```

> Note: The contact form requires a PHP server to function. All other pages work as static files.

### With PHP (contact form)

1. Deploy to a PHP-capable web host or run locally with XAMPP / WAMP / Laragon.
2. Install PHPMailer via Composer:
   ```bash
   composer require phpmailer/phpmailer
   ```
3. Configure SMTP credentials in `mail-config.php`:
   ```php
   define('SMTP_HOST', 'smtp.example.com');
   define('SMTP_USERNAME', 'you@example.com');
   define('SMTP_PASSWORD', 'your-password');
   define('SMTP_PORT', 587);
   define('SMTP_ENCRYPTION', 'tls');
   define('FROM_EMAIL', 'you@example.com');
   define('FROM_NAME',  'AS GEO ZEMİN');
   define('TO_EMAIL',   'info@asgeozemin.com');
   define('TO_NAME',    'AS GEO ZEMİN');
   ```

---

## Contact

**AS GEO ZEMİN**
Barbaros Mah. Atatürk Cad. No:28/2, Başiskele / Kocaeli, Turkey

- Phone: +90 262 343 22 21
- Mobile: +90 532 714 89 02
- Email: [info@asgeozemin.com](mailto:info@asgeozemin.com)
- Web: [www.asgeozemin.com](http://www.asgeozemin.com)

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

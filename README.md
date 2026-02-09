# 🦕 Dino 101 Math Website

A modern, responsive website for **Dino 101 Math** – making math visual, intuitive, and fun!

![Dino 101 Math](images/Background.png)

## 🌟 Features

- **Animated Hero Section** - Eye-catching entrance with sequential text animations and smooth scroll arrow
- **Social Media Integration** - Beautiful card-based design for YouTube, Instagram, and TikTok links
- **Merch Showcase** - Dynamic scroll-triggered animations with rotated product images
- **Contact Form** - Fully functional contact form powered by Formspree
- **Responsive Design** - Optimized for all devices from mobile to desktop
- **Modern UI/UX** - Clean, professional design with smooth transitions and hover effects

## 📁 Project Structure
```
dino-101-math/
├── index.html          # Homepage with hero, media links, and merch section
├── about.html          # About page with mission and story
├── media.html          # Social media links page
├── contact.html        # Contact form page
├── styles.css          # Main stylesheet
├── images/             # Image assets
│   ├── Background.png
│   ├── 5 FAV.png
│   ├── youtube.svg
│   ├── instagram.svg
│   ├── tiktok.svg
│   ├── tshirt.png
│   └── mug.png
└── README.md
```

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, Edge)
- A text editor (VS Code, Sublime Text, etc.)
- Optional: Local server for development (Live Server extension for VS Code)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/dino-101-math.git
```

2. Navigate to the project directory:
```bash
cd dino-101-math
```

3. Open `index.html` in your browser or use a local development server:
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server
```

4. Visit `http://localhost:8000` in your browser

## 🎨 Customization

### Updating Content

- **Hero Text**: Edit the `#hero-subtitle` paragraph in `index.html`
- **Social Media Links**: Update URLs in the media card sections
- **About Page**: Modify content in `about.html`
- **Contact Form**: Change the Formspree action URL in `contact.html`

### Styling

All styles are contained in `styles.css`. Key sections include:

- **Hero Section**: Line 51-100
- **Media Cards**: Line 180-250
- **Merch Section**: Line 260-340
- **Contact Form**: Line 400-450

### Colors

Main color palette:
- Primary: `#111` (Black)
- Background: `#fff` (White)
- Accent Gradient: `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`
- Media Section: `linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%)`

## 📱 Pages Overview

### Homepage (`index.html`)
- Hero section with parallax background
- Animated subtitle and CTA button
- Scroll arrow to navigate to content
- Social media cards with hover effects
- Merch showcase with scroll-triggered animations

### About (`about.html`)
- Mission statement
- Content overview
- Community information
- Call-to-action buttons

### Media (`media.html`)
- YouTube, Instagram, and TikTok links
- Platform-specific gradient backgrounds
- Clean card-based layout

### Contact (`contact.html`)
- Functional contact form
- Name, email, and message fields
- Formspree integration for form submissions

## 🛠️ Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Modern styling with flexbox, grid, and animations
- **Vanilla JavaScript** - Scroll animations and intersection observers
- **Formspree** - Contact form backend
- **SVG Icons** - Scalable vector graphics for social media logos

## ✨ Key Features Explained

### Hero Animation
The hero subtitle uses JavaScript to split text into individual words, each animated with a sequential delay:
```javascript
const words = subtitle.innerText.split(" ");
words.forEach((word, index) => {
  span.style.animationDelay = `${index * 0.6}s`;
});
```

### Scroll Arrow
Smooth scrolling to the media section with bouncing animation:
```javascript
scrollArrow.addEventListener('click', () => {
  document.getElementById('home-media-section').scrollIntoView({
    behavior: 'smooth'
  });
});
```

### Merch Section Animation
Uses Intersection Observer API to trigger animations when scrolled into view:
```javascript
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
}, { threshold: 0.2 });
```

## 🌐 Live Demo

Visit the live site: [Dino 101 Math](https://yourusername.github.io/dino-101-math)

## 📧 Contact

For questions or feedback, use the [contact form](contact.html) or reach out via:

- **YouTube**: [@Dino101YT](https://www.youtube.com/@Dino101YT)
- **Instagram**: [@dino.101.yt](https://www.instagram.com/dino.101.yt/)
- **TikTok**: [@dino101math](https://www.tiktok.com/@dino101math)

## 🛒 Merch

Check out exclusive Dino 101 Math merchandise at [the official store](https://dino-101-math-store.printify.me/)!

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Background images and graphics created for Dino 101 Math
- Social media icons from custom SVG assets
- Formspree for contact form backend
- Printify for merch platform

---

Made with 💚 by Dino 101 Math | © 2026

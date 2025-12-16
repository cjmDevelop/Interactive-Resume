# Interactive Resume Website

A modern, professional single-page portfolio website built with vanilla JavaScript, HTML5, and CSS3. Features smooth animations, responsive design, and a stunning Three.js particle background.

## Features

### Design & UI
- Modern, professional design with blue color scheme
- Fully responsive layout (mobile, tablet, desktop)
- Smooth scroll animations and transitions
- Interactive Three.js particle system in hero section
- Clean, semantic HTML5 structure
- CSS custom properties for easy theming

### Sections
1. **Hero Section** - Eye-catching introduction with 3D particle background
2. **About** - Personal introduction with statistics
3. **Skills** - Animated skill bars organized by category
4. **Projects** - Featured project showcase with hover effects
5. **Experience** - Professional timeline with detailed work history
6. **Contact** - Contact form and social media links

### Technical Features
- Pure vanilla JavaScript (no frameworks required)
- Fast loading and optimized performance
- Smooth scroll navigation
- Intersection Observer API for scroll animations
- Mobile-responsive navigation menu
- Form validation and submission handling
- Accessibility features (ARIA labels, semantic HTML)
- Debounced resize handlers for performance

## Project Structure

```
interactive-resume/
│
├── index.html          # Main HTML file with semantic structure
├── styles.css          # CSS with custom properties and responsive design
├── script.js           # JavaScript for interactivity and animations
└── README.md           # Project documentation
```

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A local web server (optional, but recommended for testing)

### Installation

1. Clone or download this repository
2. Open `index.html` in your web browser

**Using a local server (recommended):**

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (with http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## Customization

### Personal Information
Edit the following sections in `index.html`:

1. **Hero Section** - Update name, title, and tagline
2. **About Section** - Replace description and statistics
3. **Skills Section** - Modify skill categories and progress values
4. **Projects Section** - Add your projects with descriptions and links
5. **Experience Section** - Update work history and achievements
6. **Contact Section** - Change email, phone, location, and social links

### Color Scheme
The color palette can be easily customized in `styles.css` by modifying the CSS custom properties:

```css
:root {
    --color-primary: #1e3a8a;        /* Primary brand color */
    --color-primary-light: #2563eb;   /* Lighter brand color */
    --color-primary-lighter: #60a5fa; /* Lightest brand color */
}
```

### Adding Your Photo
Replace the SVG placeholder in the About section with an image:

```html
<div class="about-image">
    <img src="path/to/your/photo.jpg" alt="Your Name">
</div>
```

### Project Images
Replace the placeholder gradients in the Projects section with actual project screenshots:

```html
<div class="project-image">
    <img src="path/to/project-image.jpg" alt="Project Name">
</div>
```

## Features in Detail

### Three.js Particle System
The hero section features an animated 3D particle system created with Three.js. The particles rotate slowly, creating a dynamic and engaging visual effect. The system is:
- GPU-accelerated for smooth performance
- Responsive to window resizing
- Optimized for mobile devices

### Smooth Scroll Animations
Elements fade in and slide up as you scroll through the page using the Intersection Observer API. This creates a polished, professional feel without sacrificing performance.

### Skill Bars
Animated progress bars that fill when scrolled into view, showing proficiency levels for different technologies and tools.

### Responsive Navigation
- Fixed navigation bar that becomes opaque on scroll
- Mobile hamburger menu for small screens
- Active link highlighting based on scroll position
- Smooth scrolling to sections

### Contact Form
Functional contact form with:
- Client-side validation
- Visual feedback on submission
- Success/error notifications
- Easy integration with backend services

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Android)

## Performance Optimization

- Debounced scroll and resize handlers
- Efficient CSS animations using transforms
- Lazy loading with Intersection Observer
- Reduced motion support for accessibility
- Minimal dependencies (only Three.js for 3D effects)

## Accessibility

- Semantic HTML5 elements
- ARIA labels for interactive elements
- Keyboard navigation support
- Sufficient color contrast ratios
- Respects prefers-reduced-motion settings

## Deployment

### GitHub Pages
1. Push your code to a GitHub repository
2. Go to Settings > Pages
3. Select your branch and root folder
4. Your site will be live at `https://username.github.io/repository-name`

### Netlify
1. Drag and drop your project folder to Netlify
2. Your site will be live instantly with a custom URL

### Vercel
1. Import your GitHub repository
2. Deploy with zero configuration

## Connecting the Contact Form

The contact form currently logs to the console. To make it functional, you have several options:

### Option 1: Formspree
```javascript
// In script.js, replace simulateFormSubmission with:
async function submitToFormspree(data) {
    const response = await fetch('https://formspree.io/f/YOUR_FORM_ID', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify(data)
    });
    return response.json();
}
```

### Option 2: EmailJS
1. Sign up at [EmailJS](https://www.emailjs.com/)
2. Add the EmailJS SDK to your HTML
3. Update the form submission function

### Option 3: Custom Backend
Implement your own API endpoint and update the form submission logic accordingly.

## Customization Tips

1. **Fonts**: Add Google Fonts or custom fonts by updating the CSS `font-family`
2. **Icons**: Add Font Awesome or other icon libraries for better visuals
3. **Animations**: Adjust animation speeds in CSS custom properties
4. **Sections**: Add or remove sections as needed
5. **Theme**: Easily create a dark mode by adding alternate color schemes

## License

This project is open source and available for personal and commercial use.

## Credits

- Three.js for 3D graphics
- Design inspired by modern portfolio trends
- Built with vanilla JavaScript for maximum compatibility

## Support

For issues, questions, or suggestions, please open an issue in the repository or contact me directly.

---

Built with passion and vanilla JavaScript

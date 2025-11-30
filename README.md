# Shoreline Tech - Software Consultancy Website

Professional software consultancy website showcasing technical expertise, services, and architecture capabilities.

## Features

- **Modern Design**: Clean, professional design inspired by top tech consultancy firms
- **Responsive Layout**: Fully responsive across all devices (desktop, tablet, mobile)
- **Smooth Animations**: Intersection Observer animations and smooth scrolling
- **Technical Showcase**: Highlights architecture patterns, tech stack, and expertise
- **Contact Form**: Integrated contact form with email functionality
- **Performance Optimized**: Fast loading, optimized CSS and JavaScript

## Tech Stack

- HTML5
- CSS3 (Modern CSS with CSS Grid and Flexbox)
- Vanilla JavaScript (No frameworks needed)
- Google Fonts (Inter)

## Setup Instructions

1. **Open the website:**
   - Simply open `index.html` in your web browser
   - Or use a local development server for best results:

   ```bash
   # Using Python 3
   python3 -m http.server 8000

   # Using Node.js (if you have http-server installed)
   npx http-server
   ```

2. **View in browser:**
   - Open `http://localhost:8000` in your browser
   - The website will be fully functional

## Customization

### Update Contact Information

Edit the contact section in `index.html` (around line 320):
```html
<a href="mailto:bhoomikars28@gmail.com">bhoomikars28@gmail.com</a>
<a href="tel:+918123536803">+91 8123536803</a>
```

### Modify Services

Edit the services section in `index.html` (around line 90) to add/remove/modify services offered.

### Change Colors

Edit CSS variables in `styles.css` (lines 11-24):
```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #7c3aed;
    --accent-color: #06b6d4;
    /* ... more colors */
}
```

### Add Projects/Portfolio

You can extend the website by adding a portfolio section to showcase completed projects.

## Sections

1. **Hero Section**: Eye-catching introduction with value proposition
2. **Services**: Four main service offerings (Design, Architecture, Development, DevOps)
3. **Technical Expertise**: Highlighting key technical capabilities
4. **Architecture Showcase**: Enterprise-grade architectural patterns
5. **Process Timeline**: 5-step engineering process
6. **Contact Form**: Direct contact with founder information
7. **Footer**: Navigation and company information

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Deployment

### Deploy to Netlify (Recommended)

1. Create a free account on [Netlify](https://www.netlify.com/)
2. Drag and drop the `shoreline-tech-website` folder
3. Your site will be live instantly with a free Netlify domain
4. Optional: Connect your custom domain

### Deploy to Vercel

1. Create a free account on [Vercel](https://vercel.com/)
2. Import the project
3. Deploy with one click

### Deploy to GitHub Pages

1. Push code to GitHub repository
2. Go to repository Settings > Pages
3. Select main branch as source
4. Your site will be live at `https://yourusername.github.io/repo-name`

## Performance Optimizations

- Minimal external dependencies
- Optimized images (use WebP format for production)
- Lazy loading for images (can be added)
- Minified CSS and JS (for production)

## Future Enhancements

- Add portfolio/case studies section
- Integrate CMS for easy content updates
- Add blog section for technical content
- Implement analytics (Google Analytics/Plausible)
- Add testimonials section
- Create dark mode toggle

## License

All rights reserved © 2024 Shoreline Tech

## Contact

**Bhoomika RS**
Founder & Technical Architect
Email: bhoomikars28@gmail.com
Phone: +91 8123536803

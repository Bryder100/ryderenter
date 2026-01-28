# Ryder Entertainment Website

A bold, retro-futuristic website for Ryder Entertainment featuring dynamic video backgrounds and immersive animations.

## Features

- 🎬 Full-screen video hero background
- ✨ Smooth scroll animations
- 🎨 Retro-futuristic design with neon accents
- 📱 Fully responsive design
- ⚡ Interactive hover effects and micro-interactions
- 🌐 Ready for GitHub Pages deployment

## Technologies Used

- HTML5
- CSS3 (with advanced animations and gradients)
- Vanilla JavaScript
- Google Fonts (Bebas Neue & Archivo)

## Quick Start

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/yourusername/ryder-entertainment.git
cd ryder-entertainment
```

2. Open `index.html` in your browser or use a local server:
```bash
# Using Python
python -m http.server 8000

# Or using Node.js
npx serve
```

3. Navigate to `http://localhost:8000`

### GitHub Pages Deployment

1. Push this repository to GitHub
2. Go to Settings > Pages
3. Under "Source", select the main branch
4. Click Save
5. Your site will be live at `https://yourusername.github.io/ryder-entertainment/`

## File Structure

```
ryder-entertainment/
├── index.html          # Main HTML file
├── hero-bg.mp4         # Hero section video background
├── README.md           # This file
└── LICENSE             # MIT License
```

## Customization

### Colors

The color scheme is defined in CSS variables at the top of `index.html`:

```css
:root {
    --primary: #FF2E63;    /* Hot Pink */
    --secondary: #FFA500;   /* Orange */
    --dark: #0A0E27;        /* Dark Blue */
    --accent: #00F5FF;      /* Cyan */
    --light: #F8F9FA;       /* Light Gray */
}
```

### Content

Edit the content directly in `index.html`:
- Company name and tagline in the hero section
- Service cards in the features section
- Statistics in the stats section
- Social media links in the footer

### Video Background

Replace `hero-bg.mp4` with your own video file. For best results:
- Use MP4 format
- Keep file size under 10MB for faster loading
- Recommended resolution: 1920x1080 or higher
- Consider using a compressed version for web

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance Tips

- Optimize the video file size for web delivery
- Consider lazy loading for below-the-fold content
- Use CDN for faster font loading

## License

MIT License - feel free to use this template for your own projects!

## Credits

Design and Development: Created with Claude AI
Fonts: Google Fonts (Bebas Neue, Archivo)

## Contact

For questions or support, please open an issue on GitHub.

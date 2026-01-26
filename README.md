# Multidisciplinary Artist Portfolio

A beautiful, fully-featured portfolio website for showcasing your work across multiple artistic disciplines: Visual Art, Photography, Fibre Art, Music/Compositions, and Writing.

## Features

### ✨ Core Features
- **Multi-disciplinary sections** - Dedicated spaces for each art form
- **Lightbox gallery** - Click images to view them in full-screen mode
- **Audio player** - Built-in player for music compositions
- **Tagging system** - Organize and filter posts by tags
- **Blog-style writing** - Clean layout for essays and creative writing
- **Contact form** - Let visitors reach out to you
- **Add new posts** - Easy interface to add content (click the + button)
- **Responsive design** - Works beautifully on all devices

### 🎨 Design Elements
- Sophisticated typography using Cormorant Garamond, Libre Baskerville, and Space Mono
- Warm, earthy color palette with rust and blue-grey accents
- Smooth animations and transitions
- Professional, gallery-quality presentation

## How to Use

### Getting Started
1. Open `portfolio.html` in any modern web browser
2. Customize the content to showcase your own work
3. Add your own posts using the floating "+" button

### Adding New Posts

Click the **+** button in the bottom-right corner to add new content:

1. **Select Category** - Choose which section (Visual Art, Photography, etc.)
2. **Add Title** - Give your work a name
3. **Set Date** - When was it created?
4. **Write Description** - Describe your work
5. **Add Media**:
   - For visual posts: paste an image URL
   - For music: paste an audio file URL
6. **Add Tags** - Comma-separated tags (e.g., "abstract, acrylic, experimental")

### Organizing with Tags

Tags help visitors explore your work by theme, medium, or style:
- Each post can have multiple tags
- Click any tag to filter posts
- Tags automatically appear in the filter section
- Click "All" to see everything

**Example tags:**
- Visual Art: abstract, portrait, acrylic, oil, watercolor, mixed-media
- Photography: landscape, portrait, black-and-white, urban, nature
- Fibre Art: weaving, textile, embroidery, natural-dyes, tapestry
- Music: ambient, classical, experimental, electronic, acoustic
- Writing: essay, poetry, fiction, reflection, critique

## Customization Guide

### Changing Colors

Edit the CSS variables at the top of the `<style>` section:

```css
:root {
    --primary-dark: #1a1a1a;        /* Dark backgrounds */
    --primary-light: #f8f6f3;       /* Light backgrounds */
    --accent-warm: #d4a574;         /* Warm accent color */
    --accent-cool: #6b8e9f;         /* Cool accent color */
    --accent-rust: #a75838;         /* Primary accent (buttons, links) */
    --text-dark: #2d2d2d;           /* Main text */
    --text-muted: #6a6a6a;          /* Secondary text */
    --border-subtle: #e0ddd8;       /* Borders */
}
```

### Changing Fonts

The site uses three Google Fonts. To change them:

1. Find new fonts at [Google Fonts](https://fonts.google.com)
2. Update the `<link>` tag in the `<head>` section
3. Update the `font-family` properties in CSS:
   - `.logo`, `h1`, `h2`, `h3` - Currently Cormorant Garamond (decorative)
   - `body`, paragraphs - Currently Libre Baskerville (body text)
   - `.nav a`, labels - Currently Space Mono (UI elements)

### Updating Personal Information

1. **Site Title**: Change "Portfolio" in the navigation logo
2. **Hero Section**: Update the main heading and description
3. **Footer**: Add your name and copyright info
4. **Contact Form**: Connect to a backend service (see below)

### Adding Images

For images, you can:
1. **Use image URLs** from services like:
   - Unsplash (free stock photos)
   - Your own image hosting
   - Cloud storage (Dropbox, Google Drive - get public links)
   
2. **Host locally**:
   - Create an `images` folder next to your HTML file
   - Save images there
   - Reference them as `images/your-photo.jpg`

### Adding Audio Files

For music compositions:
1. Upload audio files (MP3, WAV) to cloud storage
2. Get a direct link to the file
3. Add the URL when creating a music post

Popular hosting options:
- SoundCloud (get embed code or direct link)
- Google Drive (make public, get shareable link)
- Dropbox (get direct download link)

## Making the Contact Form Work

The contact form currently shows an alert. To make it functional:

### Option 1: Formspree (Easiest)
1. Sign up at [Formspree.io](https://formspree.io)
2. Get your form endpoint
3. Replace the form's `submit` event handler with:
```javascript
contactForm.action = 'https://formspree.io/f/YOUR_FORM_ID';
contactForm.method = 'POST';
```

### Option 2: EmailJS
1. Sign up at [EmailJS](https://www.emailjs.com/)
2. Follow their setup guide
3. Add their JavaScript library
4. Connect the form to your email

### Option 3: Backend Service
If you have a server, create a backend endpoint to handle form submissions and send emails.

## Publishing Your Portfolio

### Option 1: GitHub Pages (Free)
1. Create a GitHub account
2. Create a repository named `username.github.io`
3. Upload your HTML file (rename to `index.html`)
4. Your site will be live at `https://username.github.io`

### Option 2: Netlify (Free)
1. Sign up at [Netlify](https://www.netlify.com)
2. Drag and drop your HTML file
3. Get a free subdomain or connect your own domain

### Option 3: Traditional Web Hosting
Upload your HTML file to any web hosting service via FTP or their file manager.

## Advanced Customization

### Persisting Data

Currently, posts are stored in the browser session. To save them permanently:

1. **LocalStorage** (basic, browser-only):
   - Uncomment the `savePosts()` function
   - Posts will persist in the browser
   - Won't sync across devices

2. **Backend Database** (advanced):
   - Set up a backend (Node.js, Python, PHP)
   - Create a database (MongoDB, PostgreSQL, MySQL)
   - Connect the add/remove post functions to API calls

### Adding More Features

Some ideas for enhancement:
- **Search functionality** - Search across all posts
- **Categories within sections** - Sub-categorize your work
- **Comments** - Let visitors leave feedback
- **Social sharing** - Share posts on social media
- **Analytics** - Track visitor engagement
- **Dark mode toggle** - Let users switch themes
- **Multiple languages** - Internationalization

## Browser Compatibility

Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

## File Structure

```
portfolio/
├── portfolio.html          # Main website file (contains everything)
├── README.md              # This documentation
└── images/                # (Optional) Your image files
    ├── art/
    ├── photography/
    └── fibre/
```

## Tips for Best Results

1. **Image Optimization**
   - Resize images to web-appropriate sizes (1200px wide max)
   - Compress images to load faster
   - Use tools like TinyPNG or Squoosh

2. **Consistent Tagging**
   - Create a standard list of tags
   - Use the same tags across similar works
   - Keep tags lowercase for consistency

3. **Regular Updates**
   - Add new work frequently
   - Keep descriptions concise but meaningful
   - Date your posts accurately

4. **Professional Presentation**
   - Use high-quality images
   - Proofread descriptions
   - Maintain consistent image sizes within each section

## Need Help?

Common issues and solutions:

**Images not showing?**
- Check that URLs are correct and public
- Ensure URLs start with `https://`
- Try the image URL directly in your browser

**Audio not playing?**
- Verify the audio file URL is direct (ends in .mp3, .wav)
- Check that the file is publicly accessible
- Try different audio formats (MP3 is most compatible)

**Tags not filtering?**
- Make sure tags in posts match exactly (case-insensitive)
- Check for extra spaces in tag names
- Verify tags are comma-separated

## License

This portfolio template is free to use and customize for your personal or commercial projects.

---

**Made with care for multidisciplinary artists** 🎨📸🧵🎵✍️

Customize this template to make it uniquely yours. Show the world your creative vision!

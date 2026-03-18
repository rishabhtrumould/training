# Mpoint × Trumould — Customer Journey Page

Case study page documenting the PASSalert IoT fire detection enclosure manufacturing journey.

## Project Structure

```
mpoint-vercel/
├── index.html              # Main page
├── vercel.json             # Vercel deployment config
├── public/
│   └── images/
│       ├── bulk-packaging.jpg
│       ├── enclosures-array.jpg
│       ├── passalert-branded.jpg
│       └── single-unit.jpg
└── README.md
```

## Deploy to Vercel

### Option 1: Via GitHub

1. Push this folder to a GitHub repository
2. Go to [vercel.com](https://vercel.com) and sign in
3. Click **"Add New" → "Project"**
4. Import your GitHub repository
5. Vercel will auto-detect the static site — click **"Deploy"**
6. Your site will be live at `your-project.vercel.app`

### Option 2: Via Vercel CLI

```bash
npm i -g vercel
cd mpoint-vercel
vercel
```

## Customization

### Update Stats
In `index.html`, find the `.stats-band` section and replace the `—` placeholders:
```html
<div class="stat-value">5,000+</div>   <!-- Units Produced -->
<div class="stat-value">6 weeks</div>  <!-- Lead Time -->
```

### Add Testimonial
Find the `.testimonial` section and replace the placeholder quote and author.

### Add More Gallery Images
1. Add images to `public/images/`
2. Replace the placeholder gallery items in `index.html`:
```html
<div class="gallery-item reveal" onclick="openLightbox(this)">
  <img src="./images/your-new-image.jpg" alt="Description" loading="lazy">
</div>
```

### Update Brand Colors
Edit the CSS variables at the top of `index.html`:
```css
:root {
  --orange: #FF6B00;        /* Primary brand color */
  --orange-light: #FFF3E8;  /* Light tint */
  --orange-dark: #E05E00;   /* Dark shade */
}
```

## Tech Stack
- Pure HTML/CSS/JS (no build step required)
- Google Fonts: Instrument Serif + DM Sans
- Scroll-triggered animations via Intersection Observer
- Image lightbox gallery
- Fully responsive (mobile, tablet, desktop)

# Image Reference Guide

## Images Used in Memorial Website

### Celta Camille Head Images

**Source Location in AI Drive**: `/whealton_family_project/photos/celta/`

1. **celta.png** (688.6 KB)
   - Drama club photo showing Celta with script
   - Used on: Homepage, Celta memorial page
   - Caption: "Celta in drama club, practicing lines for a performance"
   - Note: Other person in photo is not named (per your request)

2. **celtaCropped.jpg** (163.0 KB)
   - Cropped version of drama club photo
   - Used on: Homepage memorial card
   - Better for smaller displays

3. **celtaCroppedSm.jpg** (31.8 KB)
   - Smaller version available if needed

---

### Lynn Denise Krupey Images

**Source Location in AI Drive**: `/whealton_family_project/photos/lynn/`

1. **Lynn.png** (326.6 KB)
   - Sepia-toned portrait with curly hair
   - Used on: Homepage, Lynn memorial page header
   - Caption: "Lynn - A timeless beauty with a spirit that illuminated every room"

2. **couple-1706572_1920.jpg** (203.7 KB)
   - Couple silhouette representing your love story
   - Used on: Lynn memorial page photo gallery
   - Caption: "Our love story, an eternal bond"

3. **kiss-691995_1920.jpg** (160.6 KB)
   - Silhouette of couple kissing
   - Used on: Lynn memorial page photo gallery
   - Caption: "Our first kiss - October 1992, Wrightsville Beach"

---

### Additional Photos Available (Not Currently Used)

**In Lynn folder**:
- Lynn2.png, Lynn3.png (alternate portraits)
- Lynn1985FlagTeam.png (1985 flag team photo)
- Lynn2015.jpg (2015 photo)
- LynnAndBruce.jpg (couple photo together)
- PaperbackCoverImage.jpg (book cover)
- OvercomingShyness.png (book cover)
- Jetty - Copy.psd (original jetty image, Photoshop format)

**These can be added to the website later if desired.**

---

## Where Images Appear

### Homepage (index.html)
- Celta cropped photo (memorial card)
- Lynn portrait (memorial card)

### Celta's Memorial (celta-camille-head.html)
- Large drama club photo

### Lynn's Memorial (lynn-denise-krupey.html)
- Large portrait photo
- Couple silhouette
- Kiss silhouette

---

## Image Implementation

All images use this HTML structure:

```html
<img src="[URL]" 
     alt="[Descriptive alt text]" 
     class="[responsive-class]">
<figcaption>[Caption text]</figcaption>
```

---

## Responsive CSS Classes

Images automatically scale using:

```css
img {
    max-width: 100%;
    height: auto;
    display: block;
}
```

Special classes:
- `.memorial-photo` - Homepage cards (max-width: 300px)
- `.memorial-photo-large` - Memorial pages (max-width: 700px)
- `.photo-row` - Gallery grid layout

---

## Important: Image URL Expiration

⚠️ The current blob storage URLs expire after 1 hour.

### Permanent Solutions:

**Option 1**: Download images and host with website
```
website/
└── images/
    ├── celta/
    │   └── celta-drama-club.png
    └── lynn/
        ├── lynn-portrait.png
        ├── couple-silhouette.jpg
        └── kiss-silhouette.jpg
```

Then update HTML from:
```html
<img src="https://gensparkstorageprodwest.blob.core.windows.net/..." alt="...">
```

To:
```html
<img src="images/celta/celta-drama-club.png" alt="...">
```

**Option 2**: Keep in AI Drive and regenerate URLs periodically using AI Drive tools.

---

## Image Optimization Notes

Current images are web-ready:
- ✅ Reasonable file sizes (30KB - 700KB)
- ✅ Appropriate dimensions
- ✅ Good quality for web display

No further optimization needed before deployment.

---

## Alt Text Summary

**For Accessibility**: Every image has descriptive alt text:

1. Celta drama club: "Celta Camille Head in drama club, engaged in theatrical activities"
2. Lynn portrait: "Lynn Denise Krupey, sepia-toned portrait with curly hair"
3. Couple silhouette: "Couple silhouette representing Lynn and Bruce's love"
4. Kiss silhouette: "Silhouette of couple kissing, representing our first kiss at Wrightsville Beach"

These descriptions help screen readers and improve SEO.

---

## Adding More Images Later

To add additional photos:

1. Download from AI Drive
2. Place in appropriate folder (images/celta/ or images/lynn/)
3. Add to HTML:
   ```html
   <figure>
       <img src="images/lynn/new-photo.jpg" alt="Description">
       <figcaption>Caption text</figcaption>
   </figure>
   ```
4. CSS will automatically make them responsive

---

**Created**: November 4, 2024
**Purpose**: Reference guide for memorial website images

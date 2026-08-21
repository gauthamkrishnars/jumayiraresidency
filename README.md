# Jumayira Residency — Hotel Website

## Project Overview

A static website for **Jumayira Residency**, a budget hotel in Kovalam, Kerala.
Built by rebranding a previous client's website (Lakeside Meadows — a homestay in Kollam).

**Client:** Gautham Krishna
**GitHub:** https://github.com/gauthamkrishnars/jumayiraresidency
**Status:** Deployed but needs new photos from client

---

## Client Details

| Field | Value |
|-------|-------|
| Business Name | Jumayira Residency |
| Type | Hotel (NOT homestay) |
| Location | Nedumon Lane, Kovalam, Kerala 695527 |
| Phone | +91 94001 27085 |
| Email | jumayiraresidency2016@gmail.com |
| Google Maps | https://maps.app.goo.gl/C8prav9S9SSUh79D9 |
| Coordinates | 8.400034, 76.9753352 |
| WhatsApp Booking | https://wa.me/919400127085 |
| Netlify URL | https://jumayiraresidency.netlify.app/ |

---

## What We Did (Session Log)

### 1. Starting Point
- Cloned the Lakeside Meadows website (a homestay site in Kollam, Kerala)
- Client was charged ₹4,000 for the Lakeside Meadows site
- New client wants the same style but for a hotel in Kovalam

### 2. Initial Rebrand (First Pass)
- Copied `Lakeside Meadows - 4k/` folder → `Jumayira Residency/`
- Updated all text: Lakeside Meadows → Jumayira Residency
- Updated contact info, WhatsApp links, Google Maps embed
- Updated schema.org markup (LodgingBusiness → Hotel)
- Updated OG tags, meta description, keywords

### 3. Full Redesign (Second Pass)
Client said the site still looked like Lakeside Meadows. Redesigned from scratch:
- **Color scheme:** Pink (#E9919F) → Red (#B91C1C)
- **Fonts:** Playfair Display + Montserrat → Cormorant Garamond + Raleway
- **Layout:** Completely new structure
- **Removed:** Classification/certification section (not relevant for a hotel)
- **New elements:**
  - Dark black navbar (instead of white)
  - Stats strip (1.5 KM to beach, 24/7 front desk, Free WiFi, AC rooms)
  - Quote-style review cards with large quotation marks
  - Icon-based contact section
  - Modern card-based facilities grid

### 4. Copy Rewrite (Third Pass)
Client said the copy sounded too AI-generated. Rewrote everything:
- Removed words: "nestled", "iconic", "legendary", "unwind", "vibrant", "warm hospitality", "coastal getaway", "every stay feels special"
- Made it sound like a real person wrote it
- Made reviews sound like actual guest reviews (not generic "Guest Review" × 3)
- Changed title from "Premium Hotel" to just "Hotel"

### 5. Hero Dot Removal
- Removed the white circle/dot (`.heroLabel::before`) from the hero section
- Client said it looked AI-generated

### 6. Location Fix
- Client corrected: it's NOT Vizhinjam, it's Kovalam
- Updated all references from "Vizhinjam" to "Kovalam" across both HTML files

### 7. GitHub Setup
- Created new git repo in `Jumayira Residency/` folder
- Connected to remote: `gauthamkrishnars/jumayiraresidency`
- Added .gitignore, committed all files, pushed to main
- Fixed email privacy issue (GitHub GH007) by using noreply email

---

## Current File Structure

```
Jumayira Residency/
├── index.html              ← Main website (fully redesigned)
├── gallery.html            ← Photo gallery page
├── .gitignore              ← Ignores .DS_Store, Thumbs.db, etc.
├── README.md               ← This file
│
├── Logo.png                ← ✅ Correct logo (client provided, blue JR monogram)
├── Hero.jpg                ← ⚠️ NEEDS REPLACING (currently Lakeside Meadows image)
├── Property.jpg            ← ⚠️ NEEDS REPLACING
├── MasterBedroom.jpg       ← ⚠️ NEEDS REPLACING
├── GuestRoom.jpg           ← ⚠️ NEEDS REPLACING
├── LakeView.jpg            ← ⚠️ NEEDS REPLACING (rename to BeachView.jpg?)
├── LivingArea.jpg          ← ⚠️ NEEDS REPLACING
├── Kitchen.jpg             ← ⚠️ NEEDS REPLACING
├── Bathroom.jpg            ← ⚠️ NEEDS REPLACING
├── Balcony.jpg             ← ⚠️ NEEDS REPLACING
├── Stairs.jpg              ← ⚠️ NEEDS REPLACING
│
├── Classification.jpeg     ← Can be removed (was for Lakeside Meadows certification)
├── Facilities.jpeg         ← Can be removed (not used in new design)
├── Nearbyattractions.jpeg  ← Can be removed (not used in new design)
├── Houserules.jpeg         ← ⚠️ NEEDS REPLACING (hotel rules, not homestay)
├── Bathroomrules.jpeg      ← ⚠️ NEEDS REPLACING
│
├── Image10.jpg through Image36.jpeg  ← ⚠️ NEEDS REPLACING (gallery photos)
```

---

## ⚠️ TODO for Tomorrow

### Priority 1: Replace Images
Client will provide new photos. When they do:
1. Replace Hero.jpg, Property.jpg, and room photos with real hotel photos
2. Replace gallery images (Image10–Image36) with actual hotel photos
3. Replace Houserules.jpeg and Bathroomrules.jpeg with hotel-specific rules
4. Consider renaming LakeView.jpg → BeachView.jpg (or update alt text in code)

### Priority 2: Remove Old Lakeside Meadows Images
- Delete Classification.jpeg, Facilities.jpeg, Nearbyattractions.jpeg (not used in new design)

### Priority 3: Push New Images to GitHub
```bash
cd "Jumayira Residency"
git add -A
git commit -m "Replace placeholder images with actual hotel photos"
git push
```

### Priority 4: Deploy to Netlify
- Connect GitHub repo to Netlify
- Or manually upload the folder

---

## Technical Details

### Color Scheme
| Variable | Color | Use |
|----------|-------|-----|
| --red | #B91C1C | Primary accent, buttons, nav highlights |
| --redDark | #7F1D1D | Button hover states |
| --redLight | #DC2626 | Nav text highlights, footer headings |
| --black | #1A1A1A | Nav background, text, footer |
| --white | #FFFFFF | Main background |
| --cream | #FDF6F0 | Feature icons, quote marks |
| --warmGray | #6B6B6B | Body text |
| --lightGray | #F0F0F0 | Section backgrounds |

### Fonts
- **Headings:** Cormorant Garamond (serif, elegant)
- **Body:** Raleway (clean sans-serif)

### Key URLs in Code
- WhatsApp: `https://wa.me/919400127085?text=Hello%2C%20I%20would%20like%20to%20book%20a%20room.`
- Google Maps: `https://maps.app.goo.gl/C8prav9S9SSUh79D9`
- Netlify OG URL: `https://jumayiraresidency.netlify.app/`

### Sections in index.html
1. Nav (sticky, black background)
2. Hero (full-screen background image, gradient overlay)
3. Highlights Strip (red bar with 4 stats)
4. About (2-column: image + text)
5. Facilities (6 cards in 3-column grid)
6. Attractions (2 panels: places to visit + distance guide)
7. Gallery (3-column grid, 9 preview images)
8. Reviews (3 quote-style cards)
9. Contact (2-column: info + Google Maps embed)
10. Footer (3-column: brand + links + policies)
11. Modals (House Rules image, Terms text, Privacy text)

---

## Previous Client Reference (Lakeside Meadows)

If you need to reference the original Lakeside Meadows code, it's still in the repo:
- `../Lakeside Meadows - 4k/index.html`
- `../Lakeside Meadows - 4k/gallery.html`
- Same folder structure, same CSS framework, but pink color scheme and homestay content

---

## Git Commands Reference

```bash
# Navigate to project
cd "Jumayira Residency"

# Check status
git status

# Add all changes
git add -A

# Commit
git commit -m "Your message"

# Push to GitHub
git push

# Pull latest
git pull origin main
```

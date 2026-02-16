# Lab 2 - CSS Ricing (Stylus) + Styled Adventure (COYA)

This repository contains two deliverables:

1. **Ricing a real website using Stylus** (custom CSS injected by the Stylus browser extension).
2. **Styling my Choose Your Own Adventure story** from Lab 1 using **external CSS only** (no JavaScript).

## Repository Structure

- `old.reddit.com-Stylus/`
  - `theme.css` (the Stylus theme)
- `docs/`
  - `reddit-before.png`
  - `reddit-after.png`
- `adventure/`
  - `inicio/` (start + credits)
  - `rutas/` (choices / routes)
  - `finales/` (endings)
  - `img/` (images)
  - `css/`
    - `story.css` (external CSS used by all pages)

## Part 1 - Stylus Theme (Ricing)

**Website:** old.reddit.com  
**File:** `old.reddit.com-Stylus/theme.css`

### Before / After screenshots
- Before: `docs/reddit-before.png`
- After: `docs/reddit-after.png`

How I tested it:
- Install the Stylus extension
- Create a new style for the domain `old.reddit.com`
- Paste the CSS from `old.reddit.com-Stylus/theme.css`
- Enable/disable the style to compare results

## Part 2 - Styled Story (COYA)

This is a static HTML story made only with pages and links.
- No JavaScript used
- Consistent styling across pages using one external stylesheet:
  - `adventure/css/story.css`
- Different background colors for:
  - Start pages (`inicio`)
  - Route pages (`rutas`)
  - Ending pages (`finales`)
- Menu options are styled like buttons and have hover/active animations (CSS pseudo-classes)
- Images have a consistent frame and size

### Entry point
- `adventure/inicio/index.html`

## Run with NGINX (macOS Homebrew)

NGINX is served locally and the story is opened through localhost.

1. Make sure nginx is running:
```bash
brew services start nginx
...
```

2. Copy the adventure/ folder into the Homebrew NGINX web root:
PREFIX="$(brew --prefix)"
sudo rm -rf "$PREFIX/var/www/adventure"
sudo cp -R ./adventure "$PREFIX/var/www/adventure"
sudo chmod -R 755 "$PREFIX/var/www/adventure"
brew services restart nginx


3. Open in the browser:
http://localhost:8080/adventure/inicio/index.html

Demo Video
(Paste your video link here)
Author
Daniel Sandoval - 24885

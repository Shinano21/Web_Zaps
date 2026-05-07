# ZAPS Solutions — Images Folder

Place your images in this folder with the exact filenames listed below.
All images should be JPG or WebP format for best performance.

## Required Images

| Filename         | Section        | Recommended Size    | Description                                      |
|-----------------|----------------|---------------------|--------------------------------------------------|
| hero-bg.jpg     | Hero           | 1920×1080 px        | Full-screen background — pest control scene or city skyline |
| pharmcle-bg.jpg | Pharmcle       | 1920×1080 px        | Laboratory or chemical/biocide product background |
| about-bg.jpg    | About          | 1920×1080 px        | Office, field work, or team environment           |
| about-main.jpg  | About (card)   | 800×600 px          | Pharmcle HQ / office exterior                    |
| about-team.jpg  | About (card)   | 600×450 px          | Team or field technicians photo                  |
| iptmf-bg.jpg    | IPTMF Cycle    | 1920×1080 px        | Abstract, dark, tech-feel background              |
| services-bg.jpg | Services       | 1920×1080 px        | Pest control in action / spraying / treatment     |
| team-bg.jpg     | Team           | 1920×1080 px        | Office or field backdrop (dark-toned)            |
| clients-bg.jpg  | Clients        | 1920×1080 px        | Light/neutral background (overlaid with white)   |
| contact-bg.jpg  | Contact        | 1920×1080 px        | Professional or abstract dark background          |

## Tips for Best Results

- **Use dark images** for sections with dark overlays (hero, about, services, contact).
- **Compress your images** using tools like TinyJPG or Squoosh before uploading.
- **WebP format** is preferred for better performance — just rename to `.jpg` or update the CSS `url()` paths accordingly.
- If an image is missing, the section will fall back to its original gradient background — so nothing will break.

## How Backgrounds Work

Each section uses a layered approach:
1. **Image layer** — your photo (lowest)
2. **Overlay layer** — semi-transparent dark gradient (middle)
3. **Content** — text, cards, UI elements (top)

The overlay opacity is set so text stays readable. You can adjust overlay darkness in `css/styles.css` by finding the `.xxx-bg-overlay` class for each section.

## Example: Changing Hero Overlay Darkness

In `css/styles.css`, find:

```css
.hero-bg {
  background: linear-gradient(135deg, rgba(7,16,31,0.85) ...);
}
```

Increase the last value (e.g. `0.85` → `0.95`) to make it darker, or decrease it to show more of the photo.

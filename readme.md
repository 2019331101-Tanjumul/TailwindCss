# Tailwind CSS Setup Guide

# File Structure
```
project-root/
├── src/
│   └── input.css       # Tailwind source with @import  from tailwind website
├── public/
│   ├── index.html      # Your main HTML file
│   └── output.css      # Compiled Tailwind CSS
├── package.json
```

---

#Input File

The `src/input.css` file should contain:

```css
@import "tailwindcss";
```

This line imports Tailwind’s base, components, and utility classes. You don’t need to change this.

---

#Output File

Tailwind CSS will compile and output to `public/output.css`, which should be linked in your `public/index.html`.

---

#Build Command

Use the following command to compile Tailwind CSS and watch for changes:

```bash
npx @tailwindcss/cli -i ./src/input.css -o ./public/output.css --watch
```

You can also add it to your `package.json`:

```json
"scripts": {
  "dev": "npx @tailwindcss/cli -i ./src/input.css -o ./public/output.css --watch"
}
```

Then run it with:

```bash
npm run dev
```

This will watch your files and rebuild the CSS whenever changes are detected.

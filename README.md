# Mulax Prime: Message to My Muse

A beautiful, interactive webpage created to send a heartfelt message to **Lone**, the muse behind **Mulax Prime**.  
This page is designed to impress with glowing highlights, smooth paragraph reveals, and a visually appealing gradient background.

---

## Features

- **Animated Gradient Background**: Smoothly transitions colors for a dynamic, professional look.  
- **Glowing Title & Highlights**: Key words like *muse* and *Mulax Prime* are highlighted to draw attention.  
- **Automatic Paragraph Reveal**: Each paragraph fades in one by one for a storytelling effect.  
- **Responsive Design**: Works on desktops, tablets, and mobile devices.  
- **Clean Layout**: Centered content with subtle shadows for a polished appearance.  

---

## How It Works

### 1. HTML Structure
- Container holds the **title** and **message paragraphs**.  
- Key words wrapped in `<span>` tags are highlighted for emphasis.

### 2. CSS Styling
- Gradient background with flowing colors (pink, purple, blue, gold).  
- Glow effects on titles and highlighted words using `text-shadow`.  
- Fade-in animation for paragraphs using opacity + transition.

### 3. JavaScript Automation
- Paragraphs fade in one by one, creating a **dynamic reading experience**.

```javascript
const paragraphs = document.querySelectorAll('.fade');
let delay = 0;
paragraphs.forEach(p => {
  setTimeout(() => {
    p.style.transition = "opacity 1.5s ease-in";
    p.style.opacity = 1;
  }, delay);
  delay += 1500;
});

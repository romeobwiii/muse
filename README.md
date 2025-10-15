# Mulax Prime: Message to My Muse

A beautiful, interactive webpage created to send a heartfelt message to Lone, the muse behind Mulax Prime. This page is designed to impress with glowing animations, smooth paragraph reveal, and a visually appealing gradient background.

---

## Features

- **Animated Gradient Background**: Smoothly transitions colors to create a lively atmosphere.  
- **Glowing Title & Highlights**: Key words like *muse* and *Mulax Prime* are highlighted and glow for emphasis.  
- **Automatic Paragraph Reveal**: Each paragraph fades in one by one to create a storytelling effect.  
- **Responsive Design**: Works on desktops, tablets, and mobile devices.  
- **Clean and Elegant Layout**: Centered content with subtle shadows for a polished look.  

---

## How It Works

1. **HTML Structure**:  
   - Container holds the title and message paragraphs.  
   - Key words are wrapped in `<span class="highlight">` to make them glow.  

2. **CSS Styling**:  
   - Gradient background animation using `@keyframes`.  
   - Glow effect for the title and highlighted words.  
   - Fade-in animation controlled with opacity and JavaScript.  

3. **JavaScript Automation**:  
   - Automatically fades in paragraphs one by one with a small delay between each, creating a dynamic reading experience.

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

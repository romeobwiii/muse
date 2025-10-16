# Mulax Prime: Message to My Muse

<div style="font-family: 'Montserrat', sans-serif; font-size: 1rem; line-height: 1.6; color: #ff66b2;">

<span id="typed-text"></span><span id="cursor" style="display:inline-block; width:0.6em; background-color:#ff66b2; animation: blink 1s step-end infinite;">&nbsp;</span>

</div>

<style>
@keyframes blink {
  0%,100% { background-color: transparent; }
  50% { background-color: #ff66b2; }
}
</style>

<script>
const messageSections = [
`# Features

- Animated Gradient Background: Smoothly transitions colors for a dynamic, professional look.
- Glowing Title & Highlights: Key words like muse and Mulax Prime are highlighted to draw attention.
- Automatic Paragraph Reveal: Each paragraph fades in one by one for storytelling.
- Responsive Design: Works on desktops, tablets, and mobile devices.
- Clean Layout: Centered content with subtle shadows for a polished appearance.

`,

`# How It Works

## 1. HTML Structure
- Container holds the title and message paragraphs.
- Key words wrapped in <span> tags are highlighted for emphasis.

## 2. CSS Styling
- Gradient background with flowing colors (pink, purple, blue, gold).
- Glow effects on titles and highlighted words using text-shadow.
- Fade-in animation for paragraphs using opacity + transition.

## 3. JavaScript Automation
- Paragraphs fade in one by one, creating a dynamic reading experience.

`,

`# Message to Lone

Dear <span style="color:#facc15; font-weight:bold;">Lone</span>,

You are my inspiration, the spark that lights every idea, and the heartbeat of creativity in Mulax Prime.

Every word here, every line of code, carries your influence and energy.

Thank you, <span style="color:#facc15; font-weight:bold;">Lone</span>, for being the muse that makes Mulax Prime shine.

`,

`# Color Palette

| Color  | Hex       |
|--------|----------|
| Pink   | #ff66b2  |
| Purple | #a78bfa  |
| Blue   | #60a5fa  |
| Gold   | #facc15  |
| White  | #ffffff  |

`
];

const textEl = document.getElementById('typed-text');
let sectionIndex = 0;
let charIndex = 0;

function typeWriter() {
  if (sectionIndex < messageSections.length) {
    const section = messageSections[sectionIndex];
    if (charIndex < section.length) {
      textEl.innerHTML += section.charAt(charIndex);
      charIndex++;
      setTimeout(typeWriter, 30);
    } else {
      // Move to next section
      sectionIndex++;
      charIndex = 0;
      // Add small gap between sections
      textEl.innerHTML += "\n\n";
      setTimeout(typeWriter, 500);
    }
  } else {
    // Finished typing
    document.getElementById('cursor').style.display = 'none';
  }
}

window.onload = typeWriter;
</script>

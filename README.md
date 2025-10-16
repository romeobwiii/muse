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
const message = `Dear Lone,

You are my inspiration, the spark that lights every idea, and the heartbeat of creativity in Mulax Prime.

Every word here, every line of code, carries your influence and energy.

Thank you, Lone, for being the muse that makes Mulax Prime shine.`;

const textEl = document.getElementById('typed-text');
let i = 0;
const speed = 40;

function typeWriter() {
  if(i < message.length){
    // Highlight "Lone" in gold
    if(message.slice(i, i+4) === "Lone"){
      textEl.innerHTML += '<span style="color:#facc15; font-weight:bold;">Lone</span>';
      i += 4;
    } else {
      textEl.innerHTML += message.charAt(i);
      i++;
    }
    setTimeout(typeWriter, speed);
  }
}

window.onload = typeWriter;
</script>

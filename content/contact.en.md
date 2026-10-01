+++
title = "About me"
layout = "author"
+++

I entered the animation industry back in the traditional era (hand-painted cels!) and witnessed the advent of computer technology, quickly recognizing its potential. Fully grasping the concept of "informatics" (automated information processing), I have always sought to maximize the capabilities offered by software. Eventually, frustrated by software limitations—particularly regarding repetitive tasks—I began coding (in JavaScript and Python) to address these gaps. APIs have become my new playground for automation and the creation of specialized professional tools.  


<a id="phone-btn" 
   class="inline-flex items-center justify-center rounded-md bg-primary-600 px-4 py-2 text-neutral-100 hover:bg-primary-500 font-medium no-underline cursor-pointer">
  {{< icon "phone" >}} &nbsp; <span id="phone-text">Show Number</span>
</a>

<script>
  document.getElementById('phone-btn').addEventListener('click', function() {
    // Reconstitution dynamique au clic
    var part1 = "06";
    var part2 = "49951247"; // Remplace par tes chiffres
    var fullNumber = part1 + part2;
    
    this.href = "tel:" + fullNumber;
    document.getElementById('phone-text').innerText = part1 + " " + part2.match(/.{1,2}/g).join(" ");
  });
</script>

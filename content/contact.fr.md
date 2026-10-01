+++
title = "About me"
layout = "author"
+++


<a id="phone-btn" 
   class="inline-flex items-center justify-center rounded-md bg-primary-600 px-4 py-2 text-neutral-100 hover:bg-primary-500 font-medium no-underline cursor-pointer">
  {{< icon "phone" >}} &nbsp; <span id="phone-text">Afficher le numéro</span>
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

Rentré dans le monde de l'animation dans la période encore tradiditionnelle (cello peint à la main !) j'ai vu l'avénement de l'informatique et vite réalisé son potentiel. Pleinement conscient de la sémantique informatique (*l'information automatisée*), j'ai toujours exploité au mieux les possibilités qu'offrent les logiciels. Puis frustré du manque de fonction des logiciels, notament dans les tâches itératives, je me suis mis à coder (**javascript**  & **python**) pour pourvoir jutement à ces manques. Les **API** **Harmony**, **Adobe**, **Fusion**, **Kitsu** sont mon nouveau domaine de jeu pour automatiser et créer des outils métier.

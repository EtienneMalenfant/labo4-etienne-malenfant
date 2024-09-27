# Code injecté

   1. `<img src="./images/XSS.jpg" alt="img"></img>`
   2. `<script>alert(document.cookie)</script>` ou `<script>ajouterTexte($('#contenu'), document.cookie);</script>`
      1. Navigateur: Edge
   3. Certain navigateurs sont configurées pour automatiquement bloquer les cookies, en particulié ceux qui proviennent d'un parti tiers. Ils est ainsi parce qu'un cookie peut être un risque de sécurité. Par exemple, si le cookie n'est pas encrypté et n'est pas transmis en https, quelqu'un pourrait le récupérer. Donc des navigateurs ou des extensions bloque les cookies qui ne satisfait pas leur critères.
   4. `<script>document.getElementById('contenu').replaceChildren()</script>`
   5. Voir la fonction `sanitizeInput(input)` de [forum.js](js/forum.js)
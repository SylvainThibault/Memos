---


---

<h2 id="liste-des-commandes-git">Liste des commandes git</h2>
<p><strong>init</strong> : Crée un dossier git vide, ou (ré)initialise un dossier déjà existant</p>
<p><strong>status</strong> : Récupère l’état actuel du dossier git</p>
<p><strong>add</strong> : Ajoute le(s) élément(s) dans la liste des fichiers et dossiers à gérer par git</p>
<p><strong>commit</strong> : Enregistre et nomme (via -m “”) les changements effectués</p>
<p><strong>log</strong> : Affiche tous les changements enregistrés (les commit)</p>
<p><strong>remote add origin</strong>: Ajoute au dossier git un “repository” distant, et le lie a un dossier ‘origin’</p>
<p><strong>push</strong> : envoie sur le repo distant les modifications enregistrées dans le dernier commit.</p>
<p><strong>push -u origin master</strong>: -u permet de se rappeler, dans ce contexte d’utilisation, quels sont les paramètres de la fonction push : origin : l’élément à push (notre repo local) master : le nom de la ‘branch’ dans laquelle nous allons push notre élément</p>
<p><strong>pull</strong> : récupère les changements du repo distant sur notre repo local</p>
<p><strong>pull origin master</strong>: ‘pull’ dans origin ce qui vient de master</p>
<p><strong>diff</strong>: Montre les différences entre l’état actuel de notre repo local et un état ‘committé’</p>
<p><strong>diff HEAD</strong>: Précise que l’état auquel on veut comparer est le dernier commit</p>
<p><strong>diff --staged</strong>: ??</p>
<p><strong>reset</strong> : inverse de add sur un élément. Si c’est un élément qui a été ‘add’ au présent commit, il ne le sera plus.</p>
<p><strong>checkout</strong> : remet l’élément à l’état du précédent commit</p>
<p><strong>branch</strong> : crée une “branch” sur notre “arbre”. On crée ainsi un nouveau contexte, indépendant de la branch “master”, dans lequel nous allons travailler. on poura les merge éventuellement plus tard</p>
<p><strong>branch</strong>: Liste l’ensemble des branch actuellement disponibles.</p>
<p><strong>checkout</strong> : change de “branch” de travail, on travaille désormais sur la branch</p>
<p><strong>rm &lt;&gt;</strong>: remove -&gt; supprime de notre repo local le(s) élément(s) &lt;&gt;, et notifie git de cette suppression (ajout dans le journal)</p>
<p><strong>merge</strong> : fusionne la branch dans laquelle on travaille avec la branch</p>
<p><strong>branch -d</strong> : supprime la branch</p>


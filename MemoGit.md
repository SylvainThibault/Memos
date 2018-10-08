---


---

<h1 id="liste-des-commandes-git">Liste des commandes git</h1>
<h2 id="configuration-de-git">Configuration de git</h2>
<pre><code>git config
</code></pre>
<p>Permet de voir et modifier les variables configuration qui contrôlent tous les aspects de l’apparence et du comportement de Git. Ces variables peuvent être stockées dans trois endroits différents :</p>
<ul>
<li>Fichier <code>/etc/gitconfig</code> : Contient les valeurs pour tous les utilisateurs et tous les dépôts du système. Si vous passez l’option <code>--system</code> à <code>git config</code>, il lit et écrit ce fichier spécifiquement.</li>
<li>Fichier <code>~/.gitconfig</code> : Spécifique à votre utilisateur. Vous pouvez forcer Git à lire et écrire ce fichier en passant l’option <code>--global</code>.</li>
<li>Fichier <code>config</code> dans le répertoire Git (c’est-à-dire <code>.git/config</code>) du dépôt en cours d’utilisation : spécifique au seul dépôt en cours.</li>
</ul>
<p>Chaque niveau surcharge le niveau précédent, donc les valeurs dans <code>.git/config</code> surchargent celles de <code>/etc/gitconfig</code>.</p>
<h4 id="pour-configurer-son-nom-et-son-mail-">Pour configurer son nom et son mail :</h4>
<pre class=" language-console"><code class="prism  language-console">$ git config --global user.name "John Doe"
$ git config --global user.email johndoe@example.com
</code></pre>
<h4 id="vérifier-ses-paramètres-">Vérifier ses paramètres :</h4>
<pre class=" language-console"><code class="prism  language-console">$ git config --list
user.name=John Doe
user.email=johndoe@example.com
color.status=auto
color.branch=auto
color.interactive=auto
color.diff=auto
…
</code></pre>
<h4 id="vérifier-un-paramètre-particulier-en-utilisant-la-commande-git-config-parametre-">Vérifier un paramètre particulier en utilisant la commande <code>git config &lt;parametre&gt; :</code></h4>
<pre class=" language-console"><code class="prism  language-console">$ git config user.name
John Doe
</code></pre>
<h2 id="obtenir-de-laide">Obtenir de l’aide</h2>
<p>Si vous avez besoin d’aide pour utiliser Git, il y a trois moyens d’obtenir les pages de manuel pour toutes les commandes de Git :</p>
<pre class=" language-console"><code class="prism  language-console">$ git help &lt;commande&gt;
$ git &lt;commande&gt; --help
$ man git-&lt;commande&gt;
</code></pre>
<p>Par exemple, vous pouvez obtenir la page de manuel pour la commande config en lançant :</p>
<pre class=" language-console"><code class="prism  language-console">$ git help config
</code></pre>
<h1 id="démarrer-un-depôt-git">Démarrer un depôt Git</h1>
<h3 id="initialisation-d’un-dépôt-git-dans-un-répertoire-existant">Initialisation d’un dépôt Git dans un répertoire existant</h3>
<pre class=" language-console"><code class="prism  language-console">$ git init
</code></pre>
<h3 id="cloner-un-dépôt-existant">Cloner un dépôt existant</h3>
<pre class=" language-console"><code class="prism  language-console">$ git clone https://github.com/monprojet/monprojet
</code></pre>
<p>Crée un répertoire <code>monprojet</code> , initialise un répertoire .git à l’intérieur, récupère toutes les données de ce dépôt, et extrait une copie de travail de la dernière version.</p>
<pre class=" language-console"><code class="prism  language-console">$ git clone [url] monprojet
</code></pre>
<p>Crée un répertoire nommé <code>monprojet</code> initialise un répertoire <code>.git</code> à l’intérieur, récupère toutes les données de ce dépôt, et extrait une copie de travail de la dernière version.</p>
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


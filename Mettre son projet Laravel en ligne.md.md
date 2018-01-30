---


---

<h1 id="se-connecter-au-serveur">Se connecter au serveur</h1>
<p>Dans le Bash :</p>
<pre><code>ssh user@51.15.214.161 (adresse IP du server)
</code></pre>
<h1 id="cloner-son-projet-depuis-github">Cloner son projet depuis github</h1>
<pre><code>git clone https://github.com/SylvainThibault/PHP-Laravel.git
(= mon dépôt git)
</code></pre>
<h1 id="installer-les-dépendances">Installer les dépendances</h1>
<pre><code>composer install
</code></pre>
<h1 id="créer-et-mettre-à-jour-le-.env">Créer et mettre à jour le .env</h1>
<p>Dans le dossier Laravel :</p>
<pre><code>cp .env.example .env
nano .env
</code></pre>
<p>Puis mettre à jour les infos de connexion à la BDD…</p>
<h1 id="donner-la-propriété-du-dossier-storage-à-apache">Donner la propriété du dossier storage à Apache</h1>
<p>Pour voir les droits et propriétés des dossier et fichiers, dans le dossier Laravel :</p>
<pre><code>ls -la
total 940
drwxr-xr-x 12 root     root       4096 Jan 30 08:23 .
drwxr-xr-x  5 root     root       4096 Jan 29 15:27 ..
drwxr-xr-x  6 root     root       4096 Jan 29 15:30 app
...
</code></pre>
<p>On voit ici que c’est le <em>user</em> ‘root’ du groupe ‘root’ qui est propriétaire de tous les dossiers.<br>
le <em>d</em> en début de ligne signifie <em>directory</em>.<br>
le <em>user</em> a les droits <em>rwx</em> (read - write - execute).<br>
le <em>group</em> a les droits <em>r-x</em>.<br>
les <em>other</em> ont les droits <em>r-x</em>.</p>
<p>Pour changer le propriétaire d’un dossier (-R signifie récursif, cad que l’ordre va s’appliquer à tous les sous-dossiers ) :<br>
<code>chown [-R] user:group directory</code></p>
<p>Apache est le <em>user</em> ‘www-data’ du <em>group</em> ‘www-data’ , et on veut appliquer l’ordre à tous les dossiers enfants donc :</p>
<pre><code>chown -R www-data:www-data storage/
</code></pre>
<blockquote>
<p>!! Il faut laisser le droit d’exécution sur les dossiers sans quoi il devient impossible pour les utilisateurs de naviguer dedans !!</p>
</blockquote>


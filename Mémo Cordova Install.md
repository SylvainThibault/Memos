---


---

<h1 id="installation-de-lenvironnement-de-développement">Installation de l’environnement de développement</h1>
<h2 id="installer-android-studio">Installer Android Studio</h2>
<ul>
<li>Télécharger Android Studio : (<a href="https://developer.android.com/studio/index.html">https://developer.android.com/studio/index.html</a>)</li>
<li>Aide à l’installation :<br>
(<a href="https://developer.android.com/studio/install.html">https://developer.android.com/studio/install.html</a>)</li>
</ul>
<h2 id="installer-node.js">Installer Node.js</h2>
<ul>
<li>Télécharger Node.js : (<a href="https://nodejs.org/fr/">https://nodejs.org/fr/</a>)</li>
</ul>
<h2 id="installer-cordova">Installer Cordova</h2>
<p>Infos installation : (<a href="http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html">http://cordova.apache.org/docs/en/latest/guide/platforms/android/index.html</a>)</p>
<h3 id="installer-jdk-java-development-kit">Installer JDK (Java Development Kit)</h3>
<ul>
<li>Télécharger la V161 : (<a href="http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html">http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html</a>)</li>
</ul>
<h3 id="installer-cordova-1">Installer Cordova</h3>
<ul>
<li>Ouvrir un Bash, vérifier la présence de Node.js</li>
</ul>
<pre><code>node -v  
</code></pre>
<ul>
<li>Installer Cordova :</li>
</ul>
<pre><code>npm install -g cordova  
</code></pre>
<ul>
<li>Changer le PATH</li>
<li>Windows + Pause</li>
<li>Paramètres système avancés</li>
<li>Variables d’environnement</li>
<li>PATH</li>
<li>Récupérer le chemin de NPM : C:\Users\mon.nom\AppData\Roaming\npm</li>
<li>Nouveau : copier le chemin</li>
<li>Déplacer vers le haut dans la liste</li>
</ul>
<h1 id="projet-application">Projet Application</h1>
<p>Informations sur la création d’un projet : (<a href="http://cordova.apache.org/#getstarted">http://cordova.apache.org/#getstarted</a>)</p>
<h2 id="créer-un-projet">Créer un projet</h2>
<p>Ligne de commande permettant de créer le dossier complet pour l’App :</p>
<pre><code>cordova create NomApplication  
</code></pre>
<h2 id="ajouter-une-plateforme">Ajouter une plateforme</h2>
<p>Pour connaître toutes les plateformes, se positionner dans le dossier puis :</p>
<pre><code>cordova platform  
</code></pre>
<p>Ajouter une plateforme web :</p>
<pre><code>cordova platform add browser  
</code></pre>
<h2 id="faire-tourner-lapplication">Faire tourner l’application</h2>
<p>Ligne de commande :</p>
<pre><code>cordova run NomPlateforme  
</code></pre>
<p>Le projet est en ligne sur : localhost:8000<br>
Le projet est compilé.</p>
<h2 id="emuler-android">Emuler Android</h2>
<p>Pour que notre ordinateur puisse fonctionner comme un Android, il faut émuler un Android</p>
<ul>
<li>Redémarrer l’ordinateur et pendant le redémarrage appuyer 2 ou 3 fois sur “Echap”</li>
<li>Dans le menu qui s’ouvre aller dans BIOS SetUp en cliquant ou appuyer sur F10</li>
<li>Aller dans l’onglet “Advanced”</li>
<li>Choisir “Systems Options”</li>
<li>Cocher les cases “Virtualization”</li>
<li>Save (puis confirmer l’enregistrement)</li>
</ul>
<h2 id="faire-tourner-lapplication-sur-la-plateforme-android">Faire tourner l’application sur la plateforme Android</h2>
<h3 id="sélectionner-la-bonne-plateforme">Sélectionner la bonne plateforme</h3>
<p>Si la commande “cordova run android” donne une erreur et indique qu’il n’y a pas le “plateforme 26”, cela peut se régler dans Android Studio</p>
<ul>
<li>Ouvrir dans Android Studio : Configure / Settings / System Settings / Android SDK</li>
<li>Cocher la plateforme 26 (colonne “API Level”) et appliquer</li>
</ul>
<h3 id="tout-fonctionne-">Tout fonctionne ?</h3>
<p>Dans Android Studio, l’onglet “Tools” il doit y avoir “Android”</p>
<p>Paramétrer ensuite le téléphone souhaité pour la visualisation.</p>
<h1 id="mémo-cordova">Mémo Cordova</h1>
<h2 id="commandes-cordova">Commandes Cordova</h2>

<table>
<thead>
<tr>
<th align="center">Commande</th>
<th>Explication</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center"><code>cordova create NomApplication</code></td>
<td>Créer un nouveau projet (création de l’intégralité du dossier)</td>
</tr>
<tr>
<td align="center"><code>cordova platform add NomPlateforme</code></td>
<td>Ajouter une plateforme pour le projet (plusieurs plateformes peuvent être créées)</td>
</tr>
<tr>
<td align="center"><code>cordova plaform</code></td>
<td>Liste des plateformes</td>
</tr>
<tr>
<td align="center"><code>cordova run NomPlateforme</code></td>
<td>Lancer l’application sur la plateforme souhaitée</td>
</tr>
<tr>
<td align="center"><code>cordova plugin add NomPlugin</code></td>
<td>Ajouter un plugin</td>
</tr>
</tbody>
</table><h2 id="structure-dun-projet-cordova">Structure d’un projet Cordova</h2>

<table>
<thead>
<tr>
<th align="center">Dossier</th>
<th>Contenu</th>
</tr>
</thead>
<tbody>
<tr>
<td align="center">platforms</td>
<td>Contient les différentes plateformes ajoutées au projet</td>
</tr>
<tr>
<td align="center">plugins</td>
<td>Contient les différents plugins installés pour le projet</td>
</tr>
<tr>
<td align="center">www</td>
<td>Contient les fichiers de développement (index.html, css, img, js)</td>
</tr>
<tr>
<td align="center">package.json</td>
<td>Récapitulatif des plugins et autres fontionnalités installés pour le projet</td>
</tr>
<tr>
<td align="center">config.xml</td>
<td>Fichier de configuration de Cordova, reprend le nom du projet, les infos sur l’auteur, lien vers le fichier index.html, infos sur l’application, les plateformes, “content” : accès à toutes les fonctionnalités du support…</td>
</tr>
<tr>
<td align="center">www/index.html</td>
<td>Page d’accueil du projet</td>
</tr>
</tbody>
</table><h1 id="ide">IDE</h1>
<p>WebStorm : IDE pour JavaScript de JetBrains</p>
<p>Importer des librairies : File / Settings / Languages &amp; Frameworks / Javascript / Librairies puis “download” (ex : jquery, bootstrap)</p>


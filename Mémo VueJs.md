---


---

<h1 id="mémo-vuejs">Mémo VueJS</h1>
<h2 id="dans-le-js-">Dans le JS :</h2>
<pre><code>new Vue ({
	el: "#monId",
	data : {
		maVariable: "test",
		monAttribut : "www.exemple.com",
		monBooleen : true,
		items : ['item0','item1','item2']
	},
	methods: {
		maMethode: function(){
			this.monBooleen = false
		}
	}
});
</code></pre>
<h2 id="dans-le-html">Dans le HTML</h2>
<h4 id="afficher-une-variable---...-">Afficher une variable : <em>{{ … }}</em></h4>
<pre><code>&lt;div id="monId"&gt;
	{{ maVariable }}
&lt;/div&gt;
</code></pre>
<hr>
<h4 id="affecter-une-variable-à-un-attribut--v-bind">Affecter une variable à un attribut : <em>v-bind</em></h4>
<pre><code>&lt;a v-bind:href="monAttribut"&gt; Mon Lien &lt;/a&gt;
</code></pre>
<p>ou en raccourci :</p>
<pre><code>&lt;a :href="monAttribut"&gt; Mon Lien &lt;/a&gt;
</code></pre>
<hr>
<h4 id="afficher--masquer-un-bloc--v-show">Afficher / Masquer un bloc : <em>v-show</em></h4>
<pre><code>&lt;div v-show="monBooleen"&gt; Contenu &lt;/div&gt;
</code></pre>
<p>Si monBooleen est égal à <em>true</em> le bloc sera affiché.<br>
S’il est égal à <em>false</em>, le bloc sera en <code>display:none</code>.</p>
<hr>
<h4 id="afficher--masquer-un-bloc-avec-une-condition--v-if--v-else">Afficher / Masquer un bloc avec une condition : <em>v-if</em> / <em>v-else</em></h4>
<pre><code>&lt;div v-if="monBooleen"&gt; Contenu &lt;/div&gt;
&lt;div v-else&gt; Un autre contenu &lt;/div&gt;
</code></pre>
<p>Si monBooleen est égal à <em>true</em> le bloc sera affiché.<br>
S’il est égal à <em>false</em>, le bloc <strong>disparaît du code</strong>.<br>
( Il est remplacé par le bloc de même niveau contenant <em>v-else</em> le cas échéant )</p>
<hr>
<h4 id="boucler-dans-un-tableau--v-for">Boucler dans un tableau : <em>v-for</em></h4>
<pre><code>&lt;ul&gt;
	&lt;li v-for="item in items"&gt;{{ item }}&lt;/li&gt;
&lt;/ul&gt;
</code></pre>
<p>Crée une variable <em>item</em> pour chaque élément du tableau <em>items</em>.</p>
<hr>
<h4 id="lier-un-champ-à-une-variable--v-model">Lier un champ à une variable : <em>v-model</em></h4>
<pre><code>&lt;input type="text" v-model="maVariable" /&gt;
&lt;p&gt; {{ maVariable }} &lt;/p&gt;
</code></pre>
<h4 id="lier-une-checkbox-à-un-bloc--v-model">Lier une checkbox à un bloc : <em>v-model</em></h4>
<pre><code>&lt;input type="checkbox" v-model="monBooleen" /&gt;
&lt;div v-if="monBooleen"&gt; Bloc à Afficher / Masquer &lt;/div&gt;
</code></pre>
<p>La valeur de <em>monBooleen</em> passe de <em>true</em> à <em>false</em> en fonction de l’état de la checkbox.</p>
<h2 id="les-interactions">Les interactions</h2>
<h4 id="mettre-un-écouteur-sur-un-élément--v-on">Mettre un écouteur sur un élément : <em>v-on</em></h4>
<pre><code>&lt;div id="blocAfermer" v-if="monBooleen"&gt;
	&lt;span class="close-icon" v-on:click="maMethode"&gt; X &lt;/span&gt;
&lt;/div&gt;
</code></pre>
<p>ou en raccourci :</p>
<pre><code>&lt;span class="close-icon" @click="maMethode"&gt; X &lt;/span&gt;
</code></pre>
<hr>
<h2 id="les-principales-commandes">Les principales commandes</h2>
<p>Pour lancer un serveur en local :</p>
<pre><code>npm run dev


npm run build
</code></pre>
<hr>
<h2 id="structure-dun-projet-vue">Structure d’un projet VUE</h2>

<table>
<thead>
<tr>
<th>Dossier</th>
<th>Contenu</th>
</tr>
</thead>
<tbody>
<tr>
<td>build</td>
<td>Ce dossier contient la configuration pour le serveur de développement et de production. Théoriquement rien à modifier dans ce dossier.</td>
</tr>
<tr>
<td>config</td>
<td>C’est le dossier qui contient plusieurs fichiers de configurations important pour l’application.</td>
</tr>
<tr>
<td>node_modules</td>
<td>Dossier dans lequel sont installés les paquets/dépendances + les dépendances des dépendances</td>
</tr>
<tr>
<td>src</td>
<td>Dossier qui contient tous nos fichiers de travail</td>
</tr>
<tr>
<td>static</td>
<td>C’est ce dossier qui va contenir les “Assets”, c’est à dire les images, les fichiers js et css de l’application.</td>
</tr>
</tbody>
</table>

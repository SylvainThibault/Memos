---


---

<h1 id="mémo-vuejs">Mémo VueJS</h1>
<p>Dans le JS :</p>
<pre><code>new Vue ({
	el: "#monId",
	data : {
		maVariable: "test",
		monAttribut : "www.exemple.com",
		monBooleen : true,
		items : ['item0','item1','item2']
	}
});
</code></pre>
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


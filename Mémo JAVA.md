---


---

<h1 id="memo-java">Memo JAVA</h1>
<h2 id="types-de-variable">Types de variable</h2>
<h4 id="variables-de-type-numérique-">Variables de type numérique :</h4>
<ul>
<li><code>byte</code> : (1 octet) peut contenir les entiers entre -128 et +127</li>
<li><code>short</code> : (2 octets) contient les entiers compris entre -32768 et +32767</li>
<li><code>int</code> : (4 octets) va de -2*109 à 2*109</li>
<li><code>long</code> : (8 octets) peut aller de −9×1018−9×1018 à 9×10189×1018 (<strong>!! Afin d’informer la JVM que le type utilisé est long, il faut ajouter un “L” à la fin du nombre !!</strong>)</li>
<li><code>float</code> : (4 octets) est utilisé pour les nombres avec une virgule flottante. (<strong>!! Il faut écrire les nombres à virgule avec un point, ajouter un “l” à la fin du nombre, et écrire les nombres ronds avec un zéro après le point : “3.0l” !!</strong>)</li>
<li><code>double</code> : (8 octets) est identique à<code>float</code>, si ce n’est qu’il contient plus de chiffres derrière la virgule et qu’il n’a pas de suffixe.  (<strong>!! Il faut ajouter un “d” à la fin du nombre !!</strong>)</li>
</ul>
<h4 id="variables-stockant-un-caractère-">Variables stockant un caractère :</h4>
<ul>
<li><code>char</code>contient <em>un</em> caractère stocké entre apostrophes (« ’ ’ »)</li>
</ul>
<h4 id="variables-stockant-un-booléen-">Variables stockant un booléen :</h4>
<ul>
<li><code>boolean</code> ne peut contenir que les valeurs :<code>true</code> ou<code>false</code></li>
</ul>
<h4 id="variables-stockant-un-string-">Variables stockant un string :</h4>
<ul>
<li><code>String</code>permet de gérer les chaînes de caractères</li>
</ul>
<p>Il s’agit d’une variable de type <em>objet</em></p>
<pre><code>    //Première méthode de déclaration
    String phrase;
    phrase = "Titi et Grosminet";
    
    //Deuxième méthode de déclaration
    String str = new String();
    str = "Une autre chaîne de caractères";
    
    //Troisième méthode de déclaration
    String string = "Une autre chaîne";
    
    //Quatrième méthode de déclaration
    String chaine = new String("Et une de plus !");
</code></pre>
<p><strong>Attention</strong> :<code>String</code>commence par une majuscule ! Et lors de l’initialisation, on utilise des guillemets doubles (« <code>" "</code> »).</p>
<h2 id="les-opérateurs-arithmétiques">Les opérateurs arithmétiques</h2>
<ul>
<li>
<p>« + » : permet d’additionner deux variables numériques (mais aussi de concaténer des chaînes de caractères ; ne vous inquiétez pas, on aura l’occasion d’y revenir).</p>
</li>
<li>
<p>« - » : permet de soustraire deux variables numériques.</p>
</li>
<li>
<p>« * » : permet de multiplier deux variables numériques.</p>
</li>
<li>
<p>« / » : permet de diviser deux variables numériques (mais je crois que vous aviez deviné).</p>
</li>
<li>
<p>« % » : permet de renvoyer le reste de la division entière de deux variables de type numérique ; cet opérateur s’appelle le  <strong>modulo</strong>.</p>
</li>
</ul>


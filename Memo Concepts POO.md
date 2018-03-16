---


---

<h1 id="concepts-de-base-poo">Concepts de base POO</h1>
<h2 id="classes">Classes</h2>
<p>Une classe est une entité regroupant des variables et des fonctions. Chacune de ces fonctions aura accès aux variables de cette entité.  Les classes contiennent la définition des objets que l’on va créer par la suite.  Une classe est donc un regroupement logique de variables et fonctions que tout objet issu de cette classe possédera.<br>
Un objet créé à partir d’une classe s’appelle une <em>instance</em></p>
<h2 id="héritage">Héritage</h2>
<p>Une classe qui <em>extends</em> une autre est une classe enfant. Elle bénéficiera des méthodes et attributs de la classe parent.</p>
<h2 id="abstract--concrete">Abstract / concrete</h2>
<p>Une méthode est abstraite tant qu’elle n’est pas définie.<br>
Une classe abstract ne peut pas être instanciée.<br>
Une classe qui contient une ou des méthodes abstraites est abstraite.</p>
<h2 id="attributs--méthodes">Attributs &amp; méthodes</h2>
<p>Un <em>attribut (ou propriété)</em> désigne une variable et une <em>méthode</em> désigne une fonction.</p>
<h2 id="getters-et-setters">Getters et setters</h2>
<p>Les getters et les setters sont des méthodes qui servent à récupérer et définir les variables au sein d’une classe (pour protéger le code et éviter de manipuler les variables depuis l’extérieur de la classe).</p>
<h2 id="interface">Interface</h2>
<p>Une interface définit un comportement (d’une classe) qui doit être implémenté par une classe, sans implémenter ce comportement. C’est un ensemble de méthodes abstraites, et de constantes. Certaines interfaces ( <em>Cloneable</em>, <em>Serializable</em>, …) sont dites interfaces de «balisage» : elle n’imposent pas la définition d’une méthode, mais indiquent que les objets qui les implémentent ont certaines propriétés.<br>
Une interface est implémentée dans une classe avec le mot-clé <em>implements</em></p>
<h2 id="constructeur">Constructeur</h2>
<p>Le constructeur est une méthode écrite dans la classe. Il sert à initialiser les attributs d’un objet dès sa création, sans connaître les valeurs à l’avance.</p>


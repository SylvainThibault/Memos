---


---

<h1 id="memo-singleton-java">Memo-Singleton-Java</h1>
<h2 id="le-singleton">Le Singleton</h2>
<p>En <a href="https://fr.wikipedia.org/wiki/G%C3%A9nie_logiciel" title="Génie logiciel">génie logiciel</a>, le <strong>singleton</strong> est un <a href="https://fr.wikipedia.org/wiki/Patron_de_conception" title="Patron de conception">patron de conception</a>  <em>(design pattern)</em> dont l’objectif est de restreindre l’instanciation d’une classe à un seul objet (ou bien à quelques objets seulement). Il est utilisé lorsqu’on a besoin exactement d’un objet pour coordonner des opérations dans un système. Le modèle est parfois utilisé pour son efficacité, lorsque le système est plus rapide ou occupe moins de mémoire avec peu d’objets qu’avec beaucoup d’objets similaires.</p>
<p>On implémente le singleton en écrivant une classe contenant une méthode qui crée une instance uniquement s’il n’en existe pas encore. Sinon elle renvoie une référence vers l’objet qui existe déjà. Dans beaucoup de langages de type objet, il faudra veiller à ce que le constructeur de la classe soit  <em>privé</em>, afin de s’assurer que la classe ne puisse être instanciée autrement que par la méthode de création contrôlée.</p>
<p>Le singleton doit être implémenté avec précaution dans les applications  <a href="https://fr.wikipedia.org/wiki/Multi-thread" title="Multi-thread">multi-thread</a>. Si deux  <a href="https://fr.wikipedia.org/wiki/Processus_l%C3%A9ger" title="Processus léger">threads</a>  exécutent  <em>en même temps</em>  la méthode de création alors que l’objet unique n’existe pas encore, il faut absolument s’assurer qu’un seul créera l’objet, et que l’autre obtiendra une référence vers ce nouvel objet.</p>
<p>La solution classique à ce problème consiste à utiliser l’<a href="https://fr.wikipedia.org/wiki/Exclusion_mutuelle" title="Exclusion mutuelle">exclusion mutuelle</a>  pour indiquer que l’objet est en cours d’instanciation.</p>
<h2 id="le-singleton-en-java">Le Singleton en Java</h2>
<p>Voici une solution écrite en  <a href="https://fr.wikipedia.org/wiki/Java_(langage)" title="Java (langage)">Java</a>  (il faut écrire un code similaire pour chaque classe singleton) :</p>
<pre><code>// La classe est finale, car un singleton n'est pas censé avoir d'héritier.
 public final class Singleton {

     // L'utilisation du mot clé volatile, en Java version 5 et supérieure,
     // permet d'éviter le cas où "Singleton.instance" est non nul,
     // mais pas encore "réellement" instancié.
     // De Java version 1.2 à 1.4, il est possible d'utiliser la classe ThreadLocal.
     private static volatile Singleton instance = null;
 
     // D'autres attributs, classiques et non "static".
     private String xxx;
     private int zzz;

     /**
 * Constructeur de l'objet.
 */
     private Singleton() {
         // La présence d'un constructeur privé supprime le constructeur public par défaut.
         // De plus, seul le singleton peut s'instancier lui-même.
         super();
     }
     
     /**
 * Méthode permettant de renvoyer une instance de la classe Singleton
 * @return Retourne l'instance du singleton.
 */
     public final static Singleton getInstance() {
         //Le "Double-Checked Singleton"/"Singleton doublement vérifié" permet 
         //d'éviter un appel coûteux à synchronized, 
         //une fois que l'instanciation est faite.
         if (Singleton.instance == null) {
            // Le mot-clé synchronized sur ce bloc empêche toute instanciation
            // multiple même par différents "threads".
            // Il est TRES important.
            synchronized(Singleton.class) {
              if (Singleton.instance == null) {
                Singleton.instance = new Singleton();
              }
            }
         }
         return Singleton.instance;
     }

     // D'autres méthodes classiques et non "static".
     public void faireXxx(...) {
       ...
       this.xxx = "bonjour";
     }

     public void faireZzz(...) {
       ...
     }
    
 }
</code></pre>
<p>Pour plus d’information, sur ce patron : Cf  <a href="http://www.cs.umd.edu/~pugh/java/memoryModel/DoubleCheckedLocking.html">The “Double-Checked Locking is Broken” Declaration</a> [<a href="http://archive.wikiwix.com/cache/?url=http%3A%2F%2Fwww.cs.umd.edu%2F~pugh%2Fjava%2FmemoryModel%2FDoubleCheckedLocking.html" title="archive sur Wikiwix">archive</a>]<a href="https://fr.wikipedia.org/wiki/Singleton_(patron_de_conception)#cite_note-1">1</a>.</p>
<p><strong>Attention, l’usage du  <em>double checked locking</em>  est une mauvaise idée en Java. Ça ne fonctionne simplement pas dans un environnement multithread. Idem pour « volatile ».</strong></p>
<p>Exemple d’utilisation :</p>
<pre><code>public static void main(String[] args) {
   // Il ne faut pas copier un singleton dans une variable locale sauf dans les cas d'optimisations extrêmes.
   Singleton.getInstance().faireXxx(1,2,3);
   Singleton.getInstance().faireZzz(3,4,5);
 }
</code></pre>
<p>Il est à noter que l’usage du pattern singleton en Java n’est pas des plus approprié car l’instanciation tardive de la classe que l’on cherche à obtenir est en fait le comportement par défaut du Java et le pattern “standard” risque juste de générer des bugs et des complications. En effet le ClassLoader de la JVM va charger les classes à la première utilisation et donc :</p>
<ol>
<li>Le mutex (la variable du synchronized) quel qu’il soit est créé à ce moment et donc est très artificiel ;</li>
<li>La classe est nativement un singleton sur lequel il est naturel de s’appuyer.</li>
</ol>
<p>À partir de cette remarque plusieurs implémentations sont possibles :</p>
<p>1/ Initialisation directe de la variable instance.</p>
<p>public final class Singleton {<br>
private final static Singleton instance = new Singleton();<br>
public final static Singleton getInstance() { return instance; }<br>
private Singleton() {}<br>
}</p>
<p>2/ Initialisation dans un bloc “static”.</p>
<pre><code>public final class Singleton {
  private static Singleton instance = null;
  static {
    instance = new Singleton();
  }
  public final static Singleton getInstance() { return instance; }
  private Singleton() {}
}
</code></pre>
<p>3/  Utilisation d’un “enum” à la place d’une classe.</p>
<pre><code>public enum Singleton {
  SINGLETON;
}
</code></pre>
<p>L’utilisation se fait par appel de la seule valeur de l’enum :</p>
<pre><code>Singleton.SINGLETON;
</code></pre>
<p>Cette dernière forme est fortement recommandée depuis Java 1.5.<br>
À noter que l’unicité du singleton est dépendante de l’unicité du ClassLoader.</p>
<h2 id="les-enumérations">Les Enumérations</h2>
<p><em>Enum type</em> est un <em>data type</em> spécial qui permet à une variable d’être un <em>set</em> de constantes.<br>
Une énumération se déclare comme une classe, mais en remplaçant le mot-clé  <code>class</code>par  <code>enum</code>. Autre différence : les énumérations héritent de la classe  <code>java.lang.Enum</code>.</p>
<p>Voici à quoi ressemble une énumération :</p>
<pre><code>public enum Langage {
  JAVA,
  C,
  CPlus,
  PHP;	
}
</code></pre>
<p>C’est une structure de données qui encapsule des “objets” (ici <code>JAVA</code>, <code>C</code>, <code>CPlus</code> et <code>PHP</code>) partageant tous les mêmes méthodes issues de la classe <code>java.lang.Object</code> comme n’importe quel autre objet : <code>equals(), toString()</code>, etc…<br>
Il n’y a pas de déclaration de portée, ni de type : les énumérations s’utilisent comme des variables statiques déclarées <code>public</code> : on écrira par exemple <code>Langage.JAVA</code>.</p>
<p>De plus, on peut recourir à la méthode <code>values()</code> retournant la liste des déclarations de l’énumération :</p>
<pre><code>public class Main {
  public static void main(String args[]){
    for(Langage lang : Langage.values()){
      if(Langage.JAVA.equals(lang))
        System.out.println("J'aime le : " + lang);
      else
        System.out.println(lang);
    }
  }
}
</code></pre>
<p>Résultat :</p>
<blockquote>
<p>J’aime le: JAVA<br>
C<br>
PLUS<br>
PHP</p>
</blockquote>
<p>Il n’est pas nécessaire de déclarer de portée au constructeur. Il est toujours considéré comme <code>private</code> afin de préserver les valeurs définies dans l’<code>enum</code>. Les données formant l’énumération sont directement construites dans la classe :<br>
public enum Langage {</p>
<pre><code>  //Objets directement construits
  JAVA ("Langage JAVA"),
  C ("Langage C"),
  CPlus ("Langage C++"),
  PHP ("Langage PHP");
   
  private String name = "";
   
  //Constructeur
  Langage(String name){
    this.name = name;
  }
   
  public String toString(){
    return name;
  }
}
</code></pre>
<p>Résultat pour le même <code>Main</code> :</p>
<blockquote>
<p>J’aime le: Langage JAVA<br>
Langage C<br>
Langage PLUS<br>
Langage PHP</p>
</blockquote>
<p>Il est donc possible de créer des méthodes qui ne passerons en argument que l’une des constantes déclarées. C’est un mécanisme protégé : seuls des arguments valides peuvent être passés en paramètres de la méthode car la méthode est appelée sur la constante.</p>
<p>Un exemple plus complet :</p>
<pre><code>public enum Langage {
  //Objets directement construits
  JAVA("Langage JAVA", "Eclipse"),
  C ("Lanage C", "Code Block"),
  CPlus ("Langage C++", "Visual studio"),
  PHP ("Langage PHP", "PS Pad");

  private String name = "";
  private String editor = "";
   
  //Constructeur
  Langage(String name, String editor){
    this.name = name;
    this.editor = editor;
  }
   
  public void getEditor(){
    System.out.println("Editeur : " + editor);
  }
   
  public String toString(){
    return name;
  }
   
  public static void main(String args[]){
    Langage l1 = Langage.JAVA;
    Langage l2 = Langage.PHP;
      
    l1.getEditor();
    l2.getEditor();
  }
}
</code></pre>


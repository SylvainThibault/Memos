---


---

<p>##Human Talk du 13 Novembre 2018<br>
###Présentation de Victor Sabatier sur certaines des nouveautés React 16.6.1<br>
React est une alternative à la manipulation du DOM, grâce à des concepts avancés tels que le <strong>Virtual DOM</strong> ( une image du DOM modifiée servant de comparaison à l’état originel ) , le <strong>One Way Data Flow</strong> ( qui optimise le Data Flow et facillite le debug ), ou encore la <strong>Reconciliation</strong> ( le mécanisme qui met en oeuvre la comparaison entre le Virtual DOM et l’ancien DOM, afin de mettre l’état à jour en n’updatant que les parties différentes ).</p>
<p>Victor Sabatier nous a d’abord brillament expliqué la notion de <strong>Fragment</strong>. Elle permet d’injecter des fragments Html sans qu’ils soient wrappés dans une <code>&lt;div&gt;</code>, ce qui pourrait occasionner un Html invalide ( notamment dans le cas de balises imbriquées, comme dans un tableau par exemple ).</p>
<p>Victor Sabatier a ensuite introduit, dans un langage d’une précision technique effarante et néanmoins accessible au plus grand nombre, les <strong>dépréciations liées au <em>Lifecycle</em> de React</strong> ainsi que les méthodes paliatives à leur disparition.</p>
<p>Quelle ne fut pas la joie de l’auditoire lorsque Victor Sabatier nous a appris que la <strong>Context API</strong> venait de passer en mode <em>‘safe’</em>. Nous allons enfin pouvoir éviter le passage de props en chaîne d’un module à l’autre ( <em>‘props drilling’</em> ) et nous économiser l’utilisation de Redux en toute tranquillité d’esprit. Gloire à Victor Sabatier.</p>
<p>Enfin, parmi les toutes nouvelles fonctionnalités de React 16.6.1, Victor Sabatier a judicieusement sélectionné les deux suivantes : <strong>React.Memo</strong> qui permet d’optimiser les performances en donnant aux <em>Function Components</em> un comportement de <em>Pure Component</em> ( mémorisation de certains résultats de calcul afin d’économiser des appels à la fonction ) et <strong>React.Lazy</strong> qui permet de rendre un import dynamique à la manière d’un composant habituel, mais au moment où il est appelé.</p>
<p>Je me sens privilégié d’avoir assisté à ce <em>Human Talk</em> de Victor Sabatier. Les qualités d’orateur de ce beau jeune homme n’ont d’égal que ses compétences techniques. Merci Victor ( de bien vouloir valider ma dernière compétence :).</p>


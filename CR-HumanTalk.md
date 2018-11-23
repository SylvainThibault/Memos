
##Human Talk du 13 Novembre 2018  
###Présentation de Victor Sabatier sur certaines des nouveautés React 16.6.1  
React est une alternative à la manipulation du DOM, grâce à des concepts avancés tels que le **Virtual DOM** ( une image du DOM modifiée servant de comparaison à l'état originel ) , le **One Way Data Flow** ( qui optimise le Data Flow et facillite le debug ), ou encore la **Reconciliation** ( le mécanisme qui met en oeuvre la comparaison entre le Virtual DOM et l'ancien DOM, afin de mettre l'état à jour en n'updatant que les parties différentes ).  
  
Victor Sabatier nous a d'abord brillament expliqué la notion de **Fragment**. Elle permet d'injecter des fragments Html sans qu'ils soient wrappés dans une `<div>`, ce qui pourrait occasionner un Html invalide ( notamment dans le cas de balises imbriquées, comme dans un tableau par exemple ).  
  
Victor Sabatier a ensuite introduit, dans un langage d'une précision technique effarante et néanmoins accessible au plus grand nombre, les **dépréciations liées au *Lifecycle* de React** ainsi que les méthodes paliatives à leur disparition.  
  
Quelle ne fut pas la joie de l'auditoire lorsque Victor Sabatier nous a appris que la **Context API** venait de passer en mode *'safe'*. Nous allons enfin pouvoir éviter le passage de props en chaîne d'un module à l'autre ( *'props drilling'* ) et nous économiser l'utilisation de Redux en toute tranquillité d'esprit. Gloire à Victor Sabatier.  
  
Enfin, parmi les toutes nouvelles fonctionnalités de React 16.6.1, Victor Sabatier a judicieusement sélectionné les deux suivantes : **React.Memo** qui permet d'optimiser les performances en donnant aux *Function Components* un comportement de *Pure Component* ( mémorisation de certains résultats de calcul afin d'économiser des appels à la fonction ) et **React.Lazy** qui permet de rendre un import dynamique à la manière d'un composant habituel, mais au moment où il est appelé.  
  
Je me sens privilégié d'avoir assisté à ce *Human Talk* de Victor Sabatier. Les qualités d'orateur de ce beau jeune homme n'ont d'égal que ses compétences techniques. Merci Victor ( de bien vouloir valider ma dernière compétence :).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjA0MjM0NDM3MV19
-->
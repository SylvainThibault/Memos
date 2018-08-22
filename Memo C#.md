# Memo C#

C# est un langage de programmation simple, moderne, orienté objet et de type sécurisé. C# est un langage orienté objet, mais inclut de plus la prise en charge de la programmation **_orientée composant_**.
C# a un  **_système de type unifié_**.  Tous les types C#, y compris les types primitifs tels que  `int`  et  `double`, héritent d’un seul type  `object`  racine.

### Main Class
    class  Hello { 
	    static void Main() { 
		    Console.WriteLine("Hello, World"); 
		}
	}

Les fichiers sources C# ont généralement l’extension de fichier  `.cs`.  Si l’on suppose que le programme « Hello, World » est stocké dans le fichier  `hello.cs`, le programme peut être compilé en ligne de commande :
```
csc hello.cs
```
ce qui génère un assembly exécutable nommé hello.exe.

La ligne de commande :
```
csc /t:library hello.cs
```
compile l’exemple en tant que bibliothèque (code sans point d’entrée  `Main`) et produit un assembly nommé  `hello.dll`.

La ligne de commande :
```
csc /r:acme.dll hello.cs
```

Cela permet de créer un assembly exécutable nommé  `hello.exe`
### Structure du programme
Les concepts clés d’organisation en C# sont les  **_programmes_**,  **_espaces de noms_**,  **_types_**,  **_membres_**  et  **_assemblys_**.  Les programmes C++, comme les programmes C, se composent d'un ou plusieurs fichiers sources.  Les programmes déclarent des types qui contiennent des membres et peuvent être organisés en espaces de noms.  Les classes et les interfaces sont des exemples de types.  Les champs, méthodes, propriétés et événements sont des exemples de membres.  Lorsque les programmes C# sont compilés, ils sont physiquement empaquetés dans des assemblys.  Les assemblys ont généralement l’extension de fichier  `.exe`  ou  `.dll`, selon qu’elles implémentent des  **_applications_**  ou des  **_bibliothèques_**, respectivement.


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExMjA1NzYwOTMsMTE3ODMzMzkzOSwxMD
ExMDQ1MDk3XX0=
-->
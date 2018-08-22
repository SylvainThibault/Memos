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
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE3ODMzMzkzOSwxMDExMDQ1MDk3XX0=
-->
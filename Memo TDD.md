---


---

<h1 id="memo-tdd">Memo TDD</h1>
<h2 id="les-différents-types-de-test">Les différents types de test</h2>
<h3 id="les-tests-unitaires">Les tests unitaires</h3>
<p>Les tests unitaires consistent à tester individuellement les composants de l’application. On pourra ainsi valider la qualité du code et les performances d’un module.</p>
<h3 id="les-tests-dintégration">Les tests d’intégration</h3>
<p>Ces tests sont exécutées pour valider l’intégration des différents modules entre eux et dans leur environnement exploitation définitif.<br>
Ils permettront de mettre en évidence des problèmes d’interfaces entre différents programmes.</p>
<h3 id="les-tests-fonctionnels">Les tests fonctionnels</h3>
<p>Ces tests ont pour but de vérifier la conformité de l’application développée avec le cahier des charges initial. Ils sont donc basés sur les spécifications fonctionnelles et techniques.</p>
<h3 id="les-tests-de-non-régression">Les tests de non-régression</h3>
<p>Les tests de non-régression permettent de vérifier que des modifications n’ont pas altérées le fonctionnent de l’application.<br>
L’utilisation d’outils de tests, dans ce domaine, permet de facilité la mise en place de ce type de tests.</p>
<h3 id="les-tests-ihm">Les tests IHM</h3>
<p>Les tests IHM ont pour but de vérifier que  la charte graphique a été respectée tout au long du développement.<br>
Cela consiste à contrôler :</p>
<ol>
<li>la présentation visuelle : les menus, les paramètres d’affichages, les propriétés des fenêtres, les barres d’icônes, la résolution des écrans, les effets de bord,…</li>
<li>la navigation : les moyens de navigations, les raccourcis, le résultat d’un déplacement dans un écran…</li>
</ol>
<h3 id="les-tests-de-configuration">Les tests de configuration</h3>
<p>Une application doit pouvoir s’adapter au renouvellement de plus en plus fréquent des ordinateurs. Il s’avère donc indispensable d’étudier l’impact des environnements d’exploitation sur son fonctionnement.<br>
Voici quelques sources de problèmes qui peuvent surgir lorsque l’on migre une application vers un environnement différent :</p>
<ol>
<li>l’application développée en 16 bits migre sur un environnement 32 bits,</li>
<li>les DLL sont incompatibles,</li>
<li>les formats de fichiers sont différents,</li>
<li>les drivers de périphériques changent,</li>
<li>les interfaces ne sont pas gérées de la même manière…</li>
</ol>
<p>Ainsi, pour faire des tests efficaces dans ce contexte, il est nécessaire de fixer certains paramètres comme par exemple :</p>
<ol>
<li>la même résolution graphique,</li>
<li>le même nombre de couleurs à l’écran,</li>
<li>une imprimante identique,</li>
<li>les mêmes paramètres pour le réseau…</li>
</ol>
<h3 id="les-tests-de-performance">Les tests de performance</h3>
<p>Le but principal des tests de performance est de valider la capacité qu’ont les serveurs et les réseaux à supporter des charges d’accès importantes.<br>
On doit notamment vérifier que les temps de réponse restent raisonnable lorsqu’un nombre important d’utilisateurs sont simultanément connectés à la base de données de l’application.<br>
Pour cela, il faut d’abord relever les temps de réponse en utilisation normale, puis les comparer aux résultats obtenus dans des conditions extrêmes d’ utilisation.<br>
Une solution est de simuler un nombre important d’utilisateur en exécutant l’application à partir d’un même poste et en analysant le trafic généré.<br>
Le deuxième objectif de ces tests est de valider le comportement de l’application, toujours dans des conditions extrêmes. Ces tests doivent permettre de définir un environnement matériel minimum pour que l’application fonctionnement correctement.</p>
<h3 id="les-tests-dinstallation">Les tests d’installation</h3>
<p>Une fois l’application validée, il est nécessaire de contrôler les aspects liés à la documentation et à l’installation.<br>
Les procédures d’installation doivent être testées intégralement car elles garantissent la fiabilité de l’application dans la phase de démarrage.<br>
Bien sûr, il faudra aussi vérifier que les supports d’installation ne contiennent pas de virus.</p>
<h2 id="la-pyramide-des-tests">La “Pyramide des tests”</h2>
<p><img src="http://softmethods.fr/wp-content/uploads/2014/12/SoftMethods_pyramide_de_tests_s.png" alt="enter image description here"></p>


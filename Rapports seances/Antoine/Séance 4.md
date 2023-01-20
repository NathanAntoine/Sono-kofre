<h1>Quatrième séance</h1>

<p>Lors de la quatrième séance, j'ai tout d'abord réglé le problème du bruit émis par le servo-moteur. </p>
<p>En effet, le problème venait effectivement du servo-moteur lui-même, donc du composant. Ainsi, j'ai changé de servo-moteur et les mesures étaient prises comme prévues.</p> 

<p>Cependant, les mêmes probèmes ont été conservés entre les mesures du piezo et le code secret. En effet, même si les mesures étaient en adéquation avec les valeurs stipulées dans le code secret, le mécanisme ne s'enclenchait pas, et dans le terminal, il y avait écrit "Secret code failed". </p>
<p>Pour cela, j'ai tout d'abord, comme la semaine dernière, retiré deux fonctions qui me renvoyait false si le code secret n'était pas en adéquation. J'ai ensuite réalisé les mesures et le mécanisme s'est bel et bien enclenché. De plus, le servo-moteur ouvrait le coffre s'il recevait 3 coups (nombre de coups du code secret), puis se refermait aussi automatiquement avant de reprendre d'autres mesures.</p> 
<p>Ainsi, au lieu d'avoir comme la semaine dernière un circuit sans fin, cette fois-ci, le cycle ouvrait le mécanisme puis le refermait uniquement. </p>

<p>J'ai donc en suite décidé de retrouver un autre code avec le même mécanisme pour vérifier si le problème venait des composants ou du montage, ou bel et bien du code que j'avais modifié. </p>
<p>J'ai réussi à trouver ce site : <a href="https://embarque.developpez.com/tutoriels/arduino/systeme-fermeture/">Serrure sonore</a>, qui m'a permit de prendre un tout nouveau montage et un tout nouveau code.</p>
<p>Par la suite, j'ai demandé donc de nouveaux composants : un condensateur de 100 microF et 3 résistances de 220 ohm. </p>
<p>J'ai passé le reste de mon heure à coder le code tout en décryptant toutes les méthodes, variables et ce que l'on cherchait à faire. </p>
<p>Puis dès que le code fût terminé, je me suis mis à monter le circuit, qui est nettement plus conséquent que le précédent. </p>
<p>Je n'ai malheureusement pas eu le temps de terminer le montage, cependant, je me suis dit que je finirai le montage et que je testerai le programme chez moi, avec des tests plus précis, pour déterminer si le programme fonctionne bien.</p>
<p>Petite précision sur le circuit, l'idée du programme est d'afficher l'état de la porte du coffre à l'aide de LED verte (uvert), jaune (écoute un code) et rouge (fermé).</p>
<p>Le piezo va capter la fréquence du son et déterminer si la fréquence est en adéquation avec le code secret (comme le précédent montage). Puis le servo-moteur va tourner ou non en fonction de la véracité du code ou non.</p>
<p>Pour fermer la porte, il faudra pousser la porte puis appuyer sur un petit interrupteur. </p>

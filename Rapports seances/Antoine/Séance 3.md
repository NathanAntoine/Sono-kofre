<p>Lors de la troisième séance, je n'ai pas réussi à palier les problèmes survenus lors de la deuxième séance.</p>

<p>En effet, lors de la deuxième séance, il y avait un problème au niveau du piezo qui prenait des valeurs alors que l'on n'avait pas émis de son particulier.</p>
<p>Au cours de la troisième séance j'ai remarqué que le problème ne provenait pas du piezo.</p>
<p>Tout d'abord, j'ai demandé à monsieur Charlon de l'aide au niveau du piezo, il m'a alors passé plusieurs résistances de 750 kohm que j'ai alors par la suite branché en série afin de me rapprocher le plus possible des 10 Méga ohm initiaux de la vidéo.</p>
<p>J'ai remarqué que les valeurs mesurées variées entre 10 et 50, comme lorsque l'on n'avait uniquement la résistance de 1 kohm. Ainsi, le problème ne provenait pas non plus des résistances.</p>
<p>J'ai alors découvert par la suite que le problème venait de l'émission de son du servo moteur. EN effet, le servo moteur émettait un grésillement qui était alors capté par le piezo, et donc faussait les résultats obtenus.</p>
<p>Si l'on débranchait l'alimentation du servo moteur, le piezo ne captait alors plus les grésillement du servo moteur ce qui permettait d'obtenir des résultats au moment souhaité.</p>

<p>Cependant, j'ai rencontré un autre problème, même si les valeurs commençait au bon moment, et que le copde secret était adéquat aux valeurs mesurées, le terminal affichait : "Secret code failed".</p>
<p>Ainsi, j'ai essayé de déterminer d'où le problème provenait. Tout d'abord j'ai commencé par rajouter des lignes de code pour déterminer ce que nous renvoyait certaines variables.</p>
<p>J'ai remarqué que dans la fonction validate(), 2 endroits nous renvoyait false et provoquait une erreur. J'ai tenté de les mettre en comentaire pour voir si le problème persistait. J'ai remarqué que lorsque l'on affichait le terminal, le code cette fois fonctionnait et affichait "Door Unlocked" et "Door Locked", ce qui signifiait que le mécanisme s'ouvrait puis se fermait.</p>
<p>Cependant, 2 nouveaux poroblèmes sont apparus. Le premier, c'est que n'importe quel code à 3 bruits ouvrait et fermait le mécanisme, même lorsque les valeurs étaient supérieures à 100. La deuxième c'est que lorsque l'on rebranchait l'alimentation du servo-moteur, le mécanisme s'activait, mais le bruit du servo-moteur était capté par le piezo, renouvelant le problème du début de séance, et donc une boucle infini était créée.</p>

<p>Pour palier le problème du bruit du servo-moteur, 2 options s'offrent à nous. La première est d'isoler le servo-moteur à l'aide de mousse insonorisante afin que ce dernier n'émette plus de bruit capté par le piezo. La deuxième solution est d'enlver l'aimentation (fil bleu sur le montage) du servo-moteur lorsque le mécanisme s'ouvre, et le remettre lorsque le mécanisme se ferme.</p>

<p>C'est pourquoi, le prochain objectif de la séance est de corriger les parties non-fonctionnelles du code, notamment le traitement des valeurs mesurées. Afin de pouvoir activer le mécanisme correctement. Par la suite, il faudra s'appropier de la mousse après avoir testé le programme en enlevant l'alimentation du servo-moteur manuellement.</p>
 

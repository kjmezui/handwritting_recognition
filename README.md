# handwritting_recognition

La reconnaissance des chiffres manuscrits à l'aide de l'ensemble de données MNIST est un projet majeur réalisé à l'aide de Neural Network. Il détecte essentiellement les images numérisées des chiffres manuscrits. 

Nous allons par contre permettre à notre système de reconnaissance de chiffres manuscrits de détecter non seulement les images numérisées de chiffres manuscrits, mais également d'écrire des chiffres sur l'écran à l'aide d'une interface graphique intégrée pour la reconnaissance.

Approche: 

Nous aborderons ce projet en utilisant un réseau neuronal convolutionnel à trois couches. 

La couche d'entrée : Elle distribue les fonctionnalités de nos exemples à la couche suivante pour le calcul des activations de la couche suivante.
La couche cachée : Elle est constituée d'unités cachées appelées activations qui assurent des liaisons non linéaires pour le réseau. Le nombre de couches cachées peut varier en fonction de nos besoins.
La couche de sortie : les nœuds ici sont appelés unités de sortie. Elle nous fournit la prédiction finale du réseau neuronal sur la base de laquelle des prédictions finales peuvent être faites.
Un réseau neuronal est un modèle inspiré du fonctionnement du cerveau. Il est constitué de plusieurs couches comportant de nombreuses activations, ces activations ressemblant aux neurones de notre cerveau. Un réseau neuronal tente d'apprendre un ensemble de paramètres dans un ensemble de données qui pourraient aider à reconnaître les relations sous-jacentes. Les réseaux neuronaux peuvent s'adapter aux changements d'entrée ; le réseau génère donc le meilleur résultat possible sans avoir besoin de repenser les critères de sortie.

Méthodologie:

Nous avons mis en œuvre un réseau neuronal avec 1 couche cachée comportant 100 unités d'activation (hors unités de biais). Les données sont chargées à partir d'un fichier .mat , les caractéristiques (X) et les étiquettes (y) ont été extraites. Ensuite, les caractéristiques sont divisées par 255 pour les redimensionner dans une plage de [0,1] afin d'éviter un débordement pendant le calcul. Les données sont divisées en 60 000 exemples d'entraînement et 10 000 exemples de test. Une rétropropagation est effectuée avec l'ensemble d'entraînement pour calculer l'hypothèse, puis une rétropropagation est effectuée afin de réduire l'erreur entre les couches. Le paramètre de régularisation lambda est défini sur 0,1 pour résoudre le problème du surajustement. L'optimiseur est exécuté pendant 70 itérations pour trouver le modèle le mieux adapté. 

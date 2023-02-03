# Test de niveau sur Django Python (Note / 20 pts)

## Evaluation de niveau sur la compréhension du Framework 

### 1. Que sont Django-admin et manage.py et expliquez leurs commandes ? (1,5pt)

- "Django-admin" est l'utilitaire de ligne de commande de Django pour effectuer des tâches administratives. 
- manage.py est créé automatiquement dans chaque projet Django. Il exécute les mêmes fonctions que Django-admin, mais il modifie également la variable d'environnement DJANGO SETTINGS MODULE pour pointer vers le fichier settings.py de votre projet.

### 2. Expliquez l'utilisation de la session dans le cadre de Django. (1pt)

Django fournit une session qui permet à l'utilisateur de stocker et d'extraire des données en fonction de chaque visiteur du site. 
Django abstrait le processus d'envoi et de réception des cookies, en plaçant un cookie d'identification de session du côté client, et en stockant toutes les données connexes du côté serveur.

![Questions d'entretien sur Python](https://static.javatpoint.com/interview/images/python-interview-q58.png)

Ainsi, les données elles-mêmes ne sont pas stockées côté client. C'est une bonne chose du point de vue de la sécurité.

### 3. Dans le contexte de Django, quelle est la différence entre un projet et une application ? (1pt)

Le projet couvre l'ensemble de l'application, tandis qu'une application est un module ou une application au sein du projet qui traite d'une exigence spécifique. Ainsi, un projet est constitué de plusieurs applications, tandis qu'une application est présente dans plusieurs projets.

### 4. Discutez du cycle demande/réponse de Django. (1pt)

Au début du processus, le serveur Django reçoit une demande. Le serveur recherche alors une URL correspondante dans les modèles d'URL définis pour le projet. Si le serveur ne trouve pas d'URL correspondante, il produit un code d'état 404. Si l'URL correspond, il exécute le code correspondant dans le fichier de vue associé à l'URL et envoie une réponse.

### 5. Expliquer Django.shortcuts.render ? (1,5pt)

La fonction render est une fonction raccourcie qui permet au développeur de passer rapidement le dictionnaire de données avec le modèle. Le modèle est ensuite combiné au dictionnaire de données à l'aide du moteur de création de modèles dans cette fonction. 
Enfin, la fonction render() fournit une HttpResponse contenant le texte rendu, c'est-à-dire les données renvoyées par les modèles. Par conséquent, la fonction Django render() fait gagner du temps au développeur et lui permet d'utiliser plusieurs moteurs de modèles.

### 6. Qu'est-ce que le Django Rest Framework ? (1pt)

Le Django Rest Framework (DRF) est un cadre qui vous aide à créer rapidement des API RESTful. Elles sont idéales pour les applications Web en raison de la faible utilisation de la bande passante.

### 7. À quoi sert l'intergiciel dans Django ? (2pt)

Vous utilisez les intergiciels pour quatre fonctions différentes :
- Gzippage du contenu
- Protection contre la falsification des requêtes intersites
- Gestion des sessions
- Utilisation de l'authentification

### 8. Comment pouvez-vous voir les requêtes SQL brutes exécutées dans Django ? (1pt)

Pour commencer, assurez-vous que le paramètre DEBUG est défini sur True. Si le paramètre est bien défini, tapez les commandes suivantes :

- from Django.db import connection
- connexion.queries

### 9. Citez plusieurs stratégies de mise en cache prises en charge par Django (2pt)

Django prend en charge ces stratégies de mise en cache :
- Mise en cache de la base de données
- Mise en cache en mémoire
- Mise en cache du système de fichiers
- Mise en cache en mémoire

### 10. Qu'est-ce qu'un QuerySet dans le contexte de Django ? (1pt)

Un QuerySet est une collection de requêtes SQL. La commande print(b.query) vous montre la requête SQL créée à partir de l'appel au filtre Django.

### 11. Expliquer la différence entre Django OneToOneField et ForeignKey Field ? (1pt)

Ces deux types de champs sont parmi les plus fréquents dans Django. 
La seule différence entre ces deux champs est que le champ ForeignKey inclut une option on_delete en plus de la classe du modèle car il est utilisé pour les relations plusieurs à un, alors que le champ OneToOneField ne gère que les relations un à un et ne nécessite que la classe du modèle.

### 12. Comment combiner plusieurs QuerySets dans une vue ? (2pt)

Les QuerySets peuvent être combinés dans un autre QuerySet, et ils ne doivent pas nécessairement provenir du même modèle.
Pour fusionner des QuerySets provenant du même modèle, utilisez l'opérateur union de Python.
L'opérateur union peut être utilisé pour combiner deux ou plusieurs QuerySets avec la syntaxe suivante :
```python
    model_combination = model_set1 | model_set2 | model_set3
```
En outre, vous pouvez concaténer deux ou plusieurs ensembles de requêtes provenant d'autres modèles en utilisant la méthode chain() du paquet Itertools.
```python
    from itertools import chain
    model_combination = list(chain(model_set1, model_set2))
```
Comme alternative, vous pouvez fusionner deux ou plusieurs ensembles de requêtes provenant d'autres modèles en utilisant union(), en passant all=TRUE pour permettre la duplication.
```python
    model_combination = model_set1.union(model_set2, all=TRUE)
```

### 13. Différence entre select_related et prefetch_related ? (2pt)

Les fonctions select-related et prefetch-related de Django sont destinées à réduire le nombre de requêtes de base de données générées lors de l'accès à des objets connexes.

Lorsqu'une requête est exécutée, select related() " suit " les relations à clé étrangère et choisit des données supplémentaires sur les objets liés.

Prefetch related() effectue la "jonction" en Python en effectuant une recherche séparée pour chaque relation.

Pour choisir un seul objet, tel qu'un OneToOneField ou une ForeignKey, les utilisateurs utilisent la fonction select_related. Lorsqu'ils récupèrent un "ensemble" d'objets, tels que ManyToManyFields ou des ForeignKeys inversées, les utilisateurs utilisent la fonction prefetch_related.

### 14. Expliquer les objets Q dans l'ORM de Django (1pt)

Lors de l'écriture de requêtes complexes, les objets Q sont utilisés parce que les fonctions filter() ne vous permettent que de "AND" les conditions ; alors que les objets Q vous permettent de "OR" les conditions.

### 15. Qu'est ce qu'une exception de Django ? (1pt)

Une exception est un événement inhabituel qui entraîne l'échec d'un programme. Django dispose de classes d'exceptions pour faire face à cette situation, et prend également en charge toutes les exceptions Python fondamentales. 
Le module Django.core.exceptions définit les classes d'exceptions du noyau de Django.
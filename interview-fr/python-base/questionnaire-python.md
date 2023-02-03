# Test de niveau sur le langage Python (Note / 20 pts)

## 1. Python est-il un langage interprété ? Expliquez (0,5pt)

Python est un langage interprété. Le programme en langage Python s'exécute directement à partir du code source. Il convertit le code source en un code de langage intermédiaire, qui est à nouveau traduit en langage machine qui doit être exécuté.

Contrairement à Java ou C, Python ne nécessite pas de compilation avant exécution.

!Questions d'entretien sur Python](https://static.javatpoint.com/interview/images/python-interpreted-language.png)

## 2. Que sont les fonctions en Python ? Donnez un exemple et un résultat (0,5pt)

Une fonction est un bloc de code qui n'est exécuté que lorsqu'un appel est fait à la fonction. Le mot-clé **def** est utilisé pour définir une fonction particulière comme indiqué ci-dessous :

**Exemple:**
```python
    def function() :
        print("Hi, Welcome to Hairun Dud :)")
    function() ; # appel à la fonction
```
**Sortie:**
```console
    Bonjour, Bienvenue à Hairun Dud :)
```


## 3. Qu'est-ce que PYTHONPATH ? (1pt)

**PYTHONPATH** a un rôle similaire à celui de PATH. Cette variable indique à Python Interpreter où trouver les fichiers de modules importés dans un programme. Elle doit inclure le répertoire de la bibliothèque source Python et les répertoires contenant le code source Python. PYTHONPATH est parfois prédéfini par l'installateur de Python.

## 4. Citer 5 modules Python courants (1,25pt)

Les modules construits les plus utilisés sont listés ci-dessous:
-   os
-   sys
-   datatime
-   math
-   random

## 5. Qu'est-ce que self en Python ? (0,5pt)

Self est une instance ou un objet d'une classe. En Python, il est explicitement inclus comme premier paramètre. Cependant, ce n'est pas le cas en Java où il est optionnel. Il permet de différencier les méthodes et les attributs d'une classe avec des variables locales.

La variable locale dans la méthode init fait référence à l'objet nouvellement créé alors que dans les autres méthodes, elle fait référence à l'objet dont la méthode a été appelée.

## 6. Que fait la fonction len() ? (0,25pt)

len() est une fonction intégrée utilisée pour calculer la longueur de séquences comme une liste, une [chaîne python] (https://intellipaat.com/blog/tutorial/python-tutorial/python-strings/) et un tableau.

**Exemple:**
```python
    ma _liste=[1,2,3,4,5]
    len(ma_liste)
```
**Sortie:**
```console
    5
```

## 7. Quelles sont les différences entre Python 2.x et Python 3.x ? (1,5pt)

Python 2.x est une ancienne version de Python. Python 3.x est une version plus récente. Python 2.x est l'héritage actuel. Python 3.x est le présent et l'avenir de ce langage.

La différence la plus visible entre Python 2 et Python 3 est l'instruction print (fonction). 
- En Python 2, cela ressemble à print "Hello".
- En Python 3, c'est print ("Hello").

La chaîne de caractères dans Python2 est implicitement ASCII, et dans Python3 elle est Unicode.

La méthode xrange() a été supprimée de la version Python 3. Un nouveau mot-clé as est introduit dans Error handling.

## 8. Qu'est-ce qu'une fonction map en Python ? Donnez un exemple de son utilisation. (1pt)

La fonction map() en Python a deux paramètres, function et iterable. La fonction map() prend une fonction en argument, puis applique cette fonction à tous les éléments d'un itérable, qui lui est passé comme autre argument. Elle renvoie une liste d'objets de résultats.

**Exemple 1**
```python
    def addition(n) :
        return n + n
    # Nous doublons tous les nombres en utilisant map()
    nombres = (1, 2, 3, 4)
    résultat = map(addition, nombres)
    print(liste(résultat))
```
**Sortie:**
```console
    [2, 4, 6, 8]
```
**Exemple 2**
```python
    # Doublez tous les nombres en utilisant map et lambda
    nombres = (1, 2, 3, 4)
    résultat = map(lambda x : x + x, nombres)
    print(liste(résultat))
```
**Sortie:**
```console
    [2, 4, 6, 8]
```
**Exemple 3**
```python
    # Ajoutez deux listes en utilisant map et lambda
    nombres1 = [1, 2, 3]
    nombres2 = [4, 5, 6]
    result = map(lambda x, y : x + y, nombres1, nombres2)
    print(liste(résultat))
```
**Sortie:**
```console
    [5, 7, 9]
```

## 9. Quels sont les types de données intégrés courants en Python ? (2pt)

Python prend en charge les types de données intégrés suivants :

**Types de données immuables:**
-   Number
-   String
-   Tuple

**Types de données modifiables:**
-   List
-   Dictionary
-   set

## 10. Comment créer une chaîne Unicode en Python ? (1pt)

Dans Python 3, l'ancien type Unicode a été remplacé par le type "str", et la chaîne est traitée en Unicode par défaut. Nous pouvons rendre une chaîne en Unicode en utilisant la fonction art.title.encode("utf-8").

**Exemple:**
```python
    1. unicode_1 = ("\u0123", "\u2665", "\U0001f638", "\u265E", "\u265F", "\u2168")
    2. imprimer (unicode_1)

    1. unicode_1 = ("\u0123", "\u2665", "\U0001f638", "\u265E", "\u265F", "\u2168")
    2. imprimez (unicode_1)
```
**Sortie:**
```console
    unicode_1 : ('ģ', '♥', '😸', '♞', '♟', 'Ⅸ')
```

## 11. Qu'est-ce que le slicing en Python ? (0,5pt)

Le découpage en tranches est un mécanisme utilisé pour sélectionner une gamme d'éléments à partir d'une séquence de type liste, tuple et chaîne. Il est avantageux et facile d'obtenir des éléments d'une plage en utilisant la méthode de découpage. Elle nécessite un : (deux points) qui sépare l'indice de début et de fin du champ. Tous les types de collecte de données (liste ou tuple) nous permettent d'utiliser le découpage pour récupérer des éléments. Bien que nous puissions obtenir des éléments en spécifiant un index, nous n'obtenons qu'un seul élément alors qu'en utilisant le slicing nous pouvons obtenir un groupe d'éléments.

![Questions d'entretien sur Python](https://static.javatpoint.com/interview/images/slicing-in-python.png)

**Exemple:**
```python
    1.  Q = "JavaTpoint, Python Interview Questions !"
    2. print(Q[2:25])
```
**Sortie:**
```console
    vaTpoint, Python Interv
```

## 12. Que signifient *args et **kwargs ? (2pt)

- *args : Il est utilisé pour passer plusieurs arguments dans une fonction.
- **kwargs : Il est utilisé pour passer des arguments multiples avec des mots-clés dans une fonction en python.

## 13. Quelle est l'utilisation de la fonction enumerate() en Python ? (1pt)

La fonction enumerate() est utilisée pour itérer dans la séquence et récupérer la position de l'index et sa valeur correspondante en même temps.

**Exemple:**
```python
    1. list_1 = ["A", "B", "C"]
    2. s_1 = "Javatpoint"
    3.  # création d'objets d'énumération
    4. object_1 = enumerate(list_1)
    5. object_2 = enumerate(s_1)

    7. print ("Return type :",type(object_1))
    8. print (list(enumerate(list_1)))
    9. print (list(enumerate(s_1)))
```

**Sortie:**
```console
    Type de retour :
    [(0, 'A'), (1, 'B'), (2, 'C')]
    [(0, 'J'), (1, 'a'), (2, 'v'), (3, 'a'), (4, 't'), (5, 'p'), (6, 'o'), (7, 'i'), (8, 'n'), (9, 't')]
```

## 14. Que fait [::-1] ? (1,5pt)

[::-1] ,c'est un exemple de notation en tranches et permet d'inverser la séquence à l'aide de l'indexation.
**[Début, fin, nombre d'étapes]**.

**Exemple:**
```python
    import array as arr
    Array_d=arr.array('i',[1,2,3,4,5])
    Array_d[::-1] #inverse le tableau ou la séquence
```
**Sortie:** 
```Console
    5,4,3,2,1
```

## 15. Comment supprimer les éléments en double d'une liste ? (1pt)

Pour supprimer les éléments en double de la liste, nous utilisons la fonction set().

**Exemple:**
```python
    demo_list=[5,4,4,6,8,12,12,1,5]
    print(demo_list)
    unique_list = list(set(demo_list))
    print(unique_list)
```
**Sortie:**
```console
    [5,4,4,6,8,12,12,1,5]
    [1,5,6,8,12]
```

## 16. Qu'est-ce que la fonction lambda en Python ? (1,5pt)

Une fonction lambda est une fonction anonyme (une fonction qui n'a pas de nom) en Python. Pour définir des fonctions anonymes, nous utilisons le mot-clé 'lambda' au lieu du mot-clé 'def', d'où le nom de 'fonction lambda'. Les fonctions lambda peuvent avoir un nombre quelconque d'arguments mais une seule instruction.

**Exemple:**
```python
    a = lambda x,y : x*y
    print(a(5, 6))
```
**Sortie:**
```console
    30
```

## 17. Expliquez les méthodes split(), sub(), subn() du module "re" en Python (3pt)

Ces méthodes appartiennent au module [Python RegEx ou 're'] (https://intellipaat.com/blog/tutorial/python-tutorial/python-regex-regular-expressions/) et sont utilisées pour modifier les chaînes de caractères.

- split() : Cette méthode est utilisée pour diviser une chaîne de caractères donnée en une liste.
- sub() : Cette méthode est utilisée pour trouver une sous-chaîne où un motif regex correspond, puis elle remplace la sous-chaîne correspondante par une chaîne différente.
- subn() : Cette méthode est similaire à la méthode sub(), mais elle renvoie la nouvelle chaîne, ainsi que le nombre de remplacements.
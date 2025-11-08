# Chapitre 1 : Premiers pas avec Python

## Bienvenue dans le monde de la programmation !

Python est un langage de programmation simple et puissant, parfait pour débuter. Il est utilisé partout : sites web, intelligence artificielle, jeux vidéo, sciences, etc.

## Qu'est-ce qu'un programme ?

Un programme, c'est une série d'instructions que l'ordinateur va suivre à la lettre. Imaginez une recette de cuisine : vous donnez des étapes précises, et l'ordinateur les exécute.

## Notre premier programme : Hello World

Commençons par la tradition : afficher un message à l'écran.

```python
print("Bonjour le monde !")
```

**Explication :** La fonction `print()` affiche du texte à l'écran. Le texte doit être entre guillemets.

**Essayez :** Modifiez le message pour afficher votre prénom !

## Les variables : la mémoire de votre programme

Une variable, c'est comme une boîte avec une étiquette où on range une information.

```python
prenom = "Marie"
age = 25
print(prenom)
print(age)
```

**Règles importantes :**
- Pas d'espaces dans les noms de variables
- Pas de caractères spéciaux (sauf _ underscore)
- Python fait la différence entre majuscules et minuscules

**Exemples de noms valides :**
- `mon_prenom` ✓
- `age_utilisateur` ✓
- `nombre1` ✓

**Exemples invalides :**
- `mon prenom` ✗ (espace)
- `1nombre` ✗ (commence par un chiffre)
- `âge` ✗ (accent)

## Les types de données de base

Python travaille avec différents types d'informations :

### 1. Les chaînes de caractères (str)
Du texte entre guillemets simples ou doubles.

```python
message = "Ceci est du texte"
ville = 'Paris'
```

### 2. Les nombres entiers (int)
Des nombres sans virgule.

```python
nombre_eleves = 30
temperature = -5
```

### 3. Les nombres décimaux (float)
Des nombres avec virgule (on utilise le point en Python).

```python
prix = 19.99
taille = 1.75
```

### 4. Les booléens (bool)
Vrai ou Faux (True ou False).

```python
est_majeur = True
a_plu = False
```

## Afficher plusieurs informations

On peut combiner du texte et des variables :

```python
prenom = "Thomas"
age = 20

print("Je m'appelle", prenom, "et j'ai", age, "ans")
```

**Résultat :** `Je m'appelle Thomas et j'ai 20 ans`

Ou utiliser les f-strings (plus moderne) :

```python
print(f"Je m'appelle {prenom} et j'ai {age} ans")
```

## Exercices pratiques

### Exercice 1 : Carte de visite
Créez un programme qui affiche vos informations :

```python
# Complétez ce code
nom = "..."
prenom = "..."
age = ...
ville = "..."

print(f"Bonjour, je suis {prenom} {nom}")
print(f"J'ai {age} ans et j'habite à {ville}")
```

### Exercice 2 : Calcul simple
Créez des variables pour calculer l'aire d'un rectangle :

```python
longueur = 10
largeur = 5
aire = longueur * largeur
print(f"L'aire du rectangle est : {aire}")
```

### Exercice 3 : Modification de variable
Observez ce qui se passe :

```python
compteur = 0
print(compteur)

compteur = 5
print(compteur)

compteur = 10
print(compteur)
```

**Question :** Que remarquez-vous ? Une variable peut-elle changer de valeur ?

## Les commentaires

Les commentaires sont des notes pour vous ou d'autres programmeurs. Python les ignore.

```python
# Ceci est un commentaire sur une ligne

"""
Ceci est un commentaire
sur plusieurs lignes
"""

age = 25  # On peut aussi commenter en fin de ligne
```

## Conseils pour bien débuter

1. **Pratiquez régulièrement** : 15 minutes par jour valent mieux que 2 heures le dimanche
2. **Expérimentez** : Modifiez les exemples, cassez le code, voyez ce qui se passe
3. **Lisez vos erreurs** : Les messages d'erreur sont vos amis, ils vous disent quoi corriger
4. **Nommez bien vos variables** : `age_utilisateur` est mieux que `x`

## Résumé du chapitre

- `print()` affiche des informations à l'écran
- Les variables stockent des informations
- Il existe plusieurs types de données : texte, nombres, booléens
- Les commentaires aident à documenter le code
- Python est sensible aux majuscules et à l'indentation

## À venir dans le chapitre 2

Nous verrons comment faire des calculs, demander des informations à l'utilisateur, et prendre des décisions dans notre code !

---

**Bon courage et amusez-vous bien ! 🐍**

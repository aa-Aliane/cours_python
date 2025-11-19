# Cours Python - Chapitre 3

## Rappel des chapitres précédents

✓ **Chapitre 1** : `print()`, types, opérations, comparaisons  
✓ **Chapitre 2** : Variables, affectation, calculs avec variables

---

## 🎤 Demander des informations : `input()`

### Qu'est-ce que `input()` ?

**`input()`** permet de **demander** quelque chose à l'utilisateur.

Le programme s'arrête et attend que l'utilisateur tape quelque chose au clavier.

**Avant `input()` :**
- Le programme fait toujours la même chose
- Les valeurs sont fixées dans le code

**Avec `input()` :**
- Le programme devient **interactif**
- L'utilisateur peut choisir les valeurs

### Syntaxe de base
```python
input("Votre message ici")
```

### Premier exemple
```python
prenom = input("Quel est ton prénom ? ")
print("Bonjour", prenom)
```

**🖥️ Ce qui se passe à l'exécution :**

1. Python affiche : `Quel est ton prénom ?`
2. Le programme attend
3. L'utilisateur tape (par exemple) : `Marie`
4. Python met `"Marie"` dans la variable `prenom`
5. Python affiche : `Bonjour Marie`

⚠️ **TRÈS IMPORTANT :** `input()` donne **TOUJOURS du texte** (type `str`), même si l'utilisateur tape un nombre !

### Exemples simples
```python
# Demander le nom
nom = input("Quel est ton nom ? ")
print("Enchanté,", nom)

# Demander la ville
ville = input("Dans quelle ville habites-tu ? ")
print("Tu habites à", ville)

# Demander la couleur préférée
couleur = input("Quelle est ta couleur préférée ? ")
print("J'aime aussi le", couleur)
```

---

## 🔢 Le problème avec les nombres

### Exemple du problème
```python
age = input("Quel est ton âge ? ")
print(type(age))  # Affiche : <class 'str'>
```

Même si l'utilisateur tape `20`, Python le considère comme du **texte** `"20"` et pas comme le nombre `20`.

### Pourquoi c'est un problème ?
```python
age = input("Quel est ton âge ? ")  # L'utilisateur tape : 20
age = age + 1  # ❌ ERREUR ! On ne peut pas faire "20" + 1
```

**Message d'erreur :**
```
TypeError: can only concatenate str (not "int") to str
```
On ne peut pas additionner du texte et un nombre !

---

## ✅ La solution : convertir avec `int()`

Pour transformer du texte en nombre entier, on utilise `int()` :
```python
age = input("Quel est ton âge ? ")  # age est du texte
age = int(age)  # On convertit en nombre entier
print(type(age))  # Affiche : <class 'int'>
```

### Version courte (recommandée)

On peut faire la conversion directement :
```python
age = int(input("Quel est ton âge ? "))
# Maintenant age est un nombre entier
```

**Comment ça marche ?**

Python fait les choses **de l'intérieur vers l'extérieur** :

1. `input("Quel est ton âge ? ")` → donne du texte (ex: `"20"`)
2. `int("20")` → convertit en nombre `20`
3. `age = 20` → stocke le nombre dans la variable

### Maintenant on peut faire des calculs
```python
age = int(input("Quel est ton âge ? "))
age_futur = age + 10
print("Dans 10 ans, tu auras", age_futur, "ans")
```

---

## 🔢 Convertir en nombre décimal avec `float()`

Pour les nombres décimaux, on utilise `float()` :
```python
taille = float(input("Quelle est ta taille en mètres ? "))
print("Ta taille est", taille, "m")
print(type(taille))  # Affiche : <class 'float'>
```

**🖥️ Exemple d'exécution :**
```
Quelle est ta taille en mètres ? 1.75
Ta taille est 1.75 m
<class 'float'>
```

---

## 📊 Résumé des conversions

| Fonction | Conversion | Exemple |
|----------|-----------|---------|
| `int()` | Texte → Nombre entier | `int("20")` → `20` |
| `float()` | Texte → Nombre décimal | `float("3.14")` → `3.14` |
| `str()` | Nombre → Texte | `str(20)` → `"20"` |

---

## 💡 Exemples pratiques complets

### Exemple 1 : Calculer un âge futur
```python
nom = input("Quel est ton nom ? ")
age = int(input("Quel est ton âge ? "))

age_dans_5_ans = age + 5

print(nom + ", dans 5 ans tu auras", age_dans_5_ans, "ans")
```

### Exemple 2 : Calculer une surface
```python
longueur = float(input("Longueur du rectangle (en mètres) ? "))
largeur = float(input("Largeur du rectangle (en mètres) ? "))

surface = longueur * largeur

print("La surface est de", surface, "m²")
```

### Exemple 3 : Additionner deux nombres
```python
nombre1 = int(input("Premier nombre : "))
nombre2 = int(input("Deuxième nombre : "))

somme = nombre1 + nombre2

print("La somme est :", somme)
```

---

## 📊 Exercices pratiques

### Exercice 1 : Présentation

Demande à l'utilisateur :
- Son prénom
- Son âge
- Sa ville

Puis affiche : "Tu t'appelles [prénom], tu as [âge] ans et tu habites à [ville]"

**Solution :**
```python
prenom = input("Quel est ton prénom ? ")
age = input("Quel est ton âge ? ")
ville = input("Dans quelle ville habites-tu ? ")

print("Tu t'appelles", prenom, ", tu as", age, "ans et tu habites à", ville)
```

### Exercice 2 : Calculer un double

Demande un nombre à l'utilisateur et affiche son double.

**Solution :**
```python
nombre = int(input("Entre un nombre : "))
double = nombre * 2
print("Le double de", nombre, "est", double)
```

### Exercice 3 : Conversion en années

Demande l'âge d'une personne en mois, et affiche son âge en années (divise par 12).

**Solution :**
```python
age_mois = int(input("Ton âge en mois : "))
age_annees = age_mois / 12
print("Tu as", age_annees, "ans")
```

### Exercice 4 : Prix total

Demande le prix d'un article et la quantité. Calcule et affiche le prix total.

**Solution :**
```python
prix = float(input("Prix de l'article : "))
quantite = int(input("Quantité : "))
total = prix * quantite
print("Prix total :", total, "€")
```

### Exercice 5 : Moyenne de deux notes

Demande deux notes à l'utilisateur et affiche leur moyenne.

**Solution :**
```python
note1 = float(input("Première note : "))
note2 = float(input("Deuxième note : "))
moyenne = (note1 + note2) / 2
print("Ta moyenne est :", moyenne)
```

---

## 🎯 Points importants à retenir

✓ `input()` permet de **demander** des informations à l'utilisateur  
✓ `input()` renvoie **TOUJOURS du texte** (type `str`)  
✓ Pour faire des calculs, il faut convertir avec `int()` ou `float()`  
✓ `int()` pour les nombres entiers  
✓ `float()` pour les nombres décimaux  
✓ On peut écrire : `age = int(input("Age ? "))`

---

## ⚠️ Erreurs fréquentes

### Erreur 1 : Oublier de convertir pour faire des calculs

❌ **Ne fonctionne pas :**
```python
age = input("Ton âge ? ")  # age est du texte
age = age + 5  # ❌ Erreur !
```

✅ **Fonctionne :**
```python
age = int(input("Ton âge ? "))  # age est un nombre
age = age + 5  # ✓ Bon !
```

### Erreur 2 : L'utilisateur tape du texte au lieu d'un nombre

**Problème :**
```python
age = int(input("Ton âge ? "))
# Si l'utilisateur tape "vingt" au lieu de "20"
# ❌ Erreur : ValueError
```

**Note :** Pour l'instant, on suppose que l'utilisateur tape correctement. Plus tard, on apprendra à gérer les erreurs avec `try/except`.

### Erreur 3 : Oublier les parenthèses de `input()`

❌ **Ne fonctionne pas :**
```python
nom = input  # Oubli des parenthèses ()
```

✅ **Fonctionne :**
```python
nom = input("Ton nom ? ")  # Avec les parenthèses
```

---

## 🔄 Schéma récapitulatif

### Le cycle d'un programme interactif

1. **DEMANDER** → `input()`
2. **CONVERTIR (si besoin)** → `int()` ou `float()`
3. **STOCKER** → `variable = ...`
4. **TRAITER** → Calculs, comparaisons...
5. **AFFICHER** → `print()`

---

**Prochaine étape :** Dans le Chapitre 4, on verra les **conditions** (`if/else`) pour que le programme prenne des **décisions** en fonction des réponses de l'utilisateur !

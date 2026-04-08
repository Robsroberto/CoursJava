---
marp: false
size: 4:3
style: |
  h2, h3, p {
    font-size: 20px;
  }
  li {
    font-size:20px
  }
headingDivider: 1
header: 
paginate: 
footer: Licence 2 Informatique &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ISI (Institut Supérieur D'Informatique) &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; RD
---

<img src="../isi.png" alt="ISI" width="100px">

# Série 1 Exercice Java Base
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <img src="java.webp" alt="ISI" width="50px">


### **Exercice 1 – Classification par tranche d'âge**

Écrire un programme qui demande à l’utilisateur de saisir son âge, puis affiche dans quelle catégorie il se trouve : "enfant" (moins de 12 ans), "adolescent" (12 à 17 ans), "jeune adulte" (18 à 25 ans), "adulte" (26 à 59 ans) ou "senior" (60 ans et plus).

---

### **Exercice 2 – Analyse d’un entier (positif, pair, multiple)**

Demander à l’utilisateur de saisir un entier, puis afficher successivement s’il est positif ou négatif, pair ou impair, et s’il est multiple de 3, de 5 ou des deux. 

---

### **Exercice 3 – Nom du mois à partir de son numéro**

Écrire un programme qui demande à l’utilisateur de saisir un numéro de mois (1 à 12) et affiche le nom du mois correspondant. Afficher un message d’erreur si le numéro est invalide.

---

### **Exercice 4 – Conversion de jours de la semaine**

Demander à l’utilisateur de saisir le **nom d’un jour de la semaine** (ex: "lundi", "mercredi", etc.) en lettres minuscules, puis afficher à quel **rang** il correspond (1 pour lundi, 7 pour dimanche). 

---

### **Exercice 5 – Affichage conditionnel d’un bulletin scolaire**

Écrire un programme qui demande une note sur 20 et affiche le bulletin suivant : "Très bien" si la note est ≥ 16, "Bien" entre 14 et 15, "Assez bien" entre 12 et 13, "Passable" entre 10 et 11, "Insuffisant" sinon. 

---

### **Exercice 6 – Mini-calculatrice intelligente**

Demander deux entiers à l’utilisateur, puis une opération à choisir parmi `+`, `-`, `*`, `/`. Selon l’opérateur saisi, effectuer l’opération et afficher le résultat. En cas de division par 0, afficher un message d’erreur. 

---

### **Exercice 7 – Interprétation numérique en lettres**

Écrire un programme qui demande à l’utilisateur un chiffre entre 0 et 9 et affiche la **représentation littérale** correspondante (ex: "zéro", "un", "deux", etc.).  Mettez un message spécifique si la saisie est hors plage.

---

### **Exercice 8 – Validation d’un mot de passe**

Écrire un programme qui demande à l’utilisateur de saisir un mot de passe et vérifie s’il correspond à la valeur `"Java2025"`. Afficher un message de succès ou d’échec selon le cas. La vérification doit être sensible à la casse (`equals()` en Java).

---

### **Exercice 9 – Permutation de deux variables**

Demander deux entiers à l’utilisateur, puis permuter leur contenu sans utiliser une troisième variable temporaire. Afficher les valeurs avant et après la permutation. Cet exercice fait appel à une logique algébrique discrète et à la maîtrise des opérations arithmétiques.

---

### **Exercice 10 – Analyse de température**

Demander à l’utilisateur une température et afficher un message différent selon la valeur : "Très froid" (moins de 5), "Frais" (5 à 15), "Tempéré" (16 à 25), "Chaud" (26 à 35), "Canicule" (plus de 35). 


### **Exercice 11 – Vérification de triangle valide**

Écrire un programme qui demande trois longueurs à l’utilisateur et vérifie si ces longueurs peuvent former un triangle. Rappel : un triangle est valide si la somme de deux côtés est toujours supérieure au troisième. Afficher un message approprié dans chaque cas.

---

### **Exercice 12 – Triangle équilatéral, isocèle ou scalène**

À partir des longueurs des 3 côtés d’un triangle (supposés valides), indiquer si le triangle est :

* équilatéral (3 côtés égaux),
* isocèle (2 côtés égaux),
* ou scalène (aucun côté égal).

---

### **Exercice 13 – Calcul du maximum et du minimum (3 entiers)**

Écrire un programme qui demande trois entiers à l’utilisateur et affiche le plus grand et le plus petit. Ne pas utiliser de `Math.max()` ni `Math.min()`, mais uniquement des `if...else`.

---

### **Exercice 14 – Année bissextile**

Demander une année à l’utilisateur et déterminer si elle est bissextile ou non. Rappel : une année est bissextile si elle est divisible par 4, sauf si elle est divisible par 100, sauf si elle est aussi divisible par 400.

---

### **Exercice 15 – Validité d’un identifiant**

Demander à l’utilisateur de saisir un identifiant, et vérifier qu’il est valide selon les règles suivantes :

* doit contenir au moins 6 caractères,
* ne doit pas commencer par un chiffre,
* ne doit pas contenir d’espace.

Afficher un message clair indiquant s’il est valide ou non.

---

### **Exercice 16 – Calcul de la moyenne pondérée**

Demander 3 notes et leurs coefficients respectifs, calculer et afficher la moyenne pondérée. Afficher également la mention associée selon la note finale (selon le barème de l’exercice 5).

---

### **Exercice 17 – Vérification de date (jour, mois, année)**

Demander à l’utilisateur de saisir un jour, un mois et une année. Vérifier si la date est **valide** (ex : pas de 31 février, mois entre 1 et 12, jours corrects selon le mois et si année bissextile). N’utilisez pas de librairie externe (pas de `LocalDate`).

---

### **Exercice 18 – Système de menu avec switch**

Créer un menu interactif avec `switch`, où l’utilisateur choisit une option :

1. Afficher "Bonjour"
2. Calculer la somme de deux nombres
3. Quitter le programme

Chaque action doit être bien gérée avec un `switch` propre. Le programme se termine après le choix 3.

---

### **Exercice 19 – Racines d’une équation du second degré**

Demander à l’utilisateur les coefficients `a`, `b`, `c` d’une équation du second degré `ax² + bx + c = 0`. Calculer et afficher la ou les racines en fonction du discriminant (`Δ = b² - 4ac`), avec gestion :

* Pas de racine (Δ < 0),
* Une racine (Δ = 0),
* Deux racines (Δ > 0).

---

### **Exercice 20 – Deviner un nombre mystère (jeu simple)**

Écrire un programme dans lequel un **nombre mystère** est défini (par exemple 27), et l’utilisateur doit le deviner. Le programme lui indique "Trop petit", "Trop grand", ou "Bravo" selon la réponse. Il doit continuer tant qu’il ne trouve pas.



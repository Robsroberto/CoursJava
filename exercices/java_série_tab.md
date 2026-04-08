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

#  **SÉRIE D'EXERCICES – TABLEAUX ET MATRICES EN JAVA**
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <img src="java.webp" alt="ISI" width="50px">



---

# **PARTIE I – TABLEAUX (1 dimension)**

### **Exercice 1 – Lecture et affichage d’un tableau**

Écrire un programme qui demande à l’utilisateur de saisir `N` valeurs entières puis de les stocker dans un tableau. Le programme affichera ensuite toutes les valeurs sous la forme :
`T[i] = valeur`.

---

### **Exercice 2 – Somme et moyenne d’un tableau**

À partir d’un tableau d’entiers saisi par l’utilisateur, calculer et afficher :

* la somme des éléments,
* la moyenne arithmétique.

---

### **Exercice 3 – Recherche d’un élément dans un tableau**

Écrire un programme qui recherche une valeur dans un tableau d’entiers et affiche :

* sa position si elle est trouvée,
* un message indiquant qu’elle n’existe pas sinon.

---

### **Exercice 4 – Plus grand et plus petit élément**

À partir d’un tableau, déterminer :

* le maximum,
* le minimum,
* la différence entre les deux.

---

### **Exercice 5 – Compter les occurrences**

Écrire un programme qui compte le nombre de fois qu’une valeur donnée apparaît dans un tableau.

---

### **Exercice 6 – Inversion d’un tableau**

Écrire un programme qui inverse l’ordre des éléments d’un tableau (ex : `[1 2 3 4] → [4 3 2 1]`).

---

### **Exercice 7 – Trouver les valeurs paires et impaires**

À partir d’un tableau d’entiers, afficher séparément :

* les valeurs paires,
* les valeurs impaires,
* leur nombre respectif.

---

### **Exercice 8 – Fusion de deux tableaux**

Écrire un programme qui fusionne deux tableaux de même taille en un tableau de taille double.

---

### **Exercice 9 – Suppression d’un élément**

Écrire un programme qui supprime la première occurrence d’une valeur donnée dans un tableau.
Le tableau final doit être réorganisé sans "trous".

---

### **Exercice 10 – Tri d’un tableau (méthode simple)**

Écrire un programme qui trie les éléments d’un tableau dans l’ordre croissant **sans utiliser l’API Java** (`Arrays.sort()` interdit).

---

---

# **PARTIE II – MATRICES (tableaux à 2 dimensions)**

### **Exercice 11 – Lecture d’une matrice**

Écrire un programme qui demande à l’utilisateur de saisir les valeurs d’une matrice `m × n`.
Afficher immédiatement la matrice sous forme de tableau.

---

### **Exercice 12 – Somme des éléments**

Calculer la somme de tous les éléments d’une matrice d’entiers.

---

### **Exercice 13 – Somme d’une ligne et d’une colonne**

À partir d’une matrice, afficher :

* la somme de la ligne `L`,
* la somme de la colonne `C`,
  où `L` et `C` sont saisis par l’utilisateur.

---

### **Exercice 14 – Diagonale principale et secondaire**

Pour une matrice carrée :

* afficher les éléments de la diagonale principale,
* afficher ceux de la diagonale secondaire,
* calculer leur somme respective.

---

### **Exercice 15 – Matrice transposée**

Écrire un programme qui calcule la **transposée** d’une matrice (lignes ↔ colonnes).

---

### **Exercice 16 – Produit d’une matrice par un scalaire**

Multiplier chaque élément d’une matrice par un nombre donné `k`.

---

### **Exercice 17 – Addition de deux matrices**

Écrire un programme qui effectue la somme élément par élément de deux matrices de même dimension.

---

### **Exercice 18 – Produit matriciel (A × B)**

Écrire un programme qui calcule la matrice produit `C = A × B`.
Rappel : les matrices sont multipliables seulement si le nombre de colonnes de `A` = nombre de lignes de `B`.

---

### **Exercice 19 – Vérification matrice symétrique**

Écrire un programme qui vérifie si une matrice carrée est **symétrique**, c’est-à-dire :
`M[i][j] == M[j][i]`.

---

### **Exercice 20 – Comptage avancé dans une matrice**

À partir d’une matrice d’entiers, déterminer :

* le nombre de valeurs positives,
* le nombre de valeurs négatives,
* le nombre de valeurs nulles,
* la valeur la plus grande et la plus petite de la matrice.

---

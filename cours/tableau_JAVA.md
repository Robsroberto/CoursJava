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

# Chapitre 4 : Les Tableaux en Java
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <img src="java.webp" alt="ISI" width="50px">

---

## 4.1. Introduction aux Tableaux

En programmation, un **tableau** est une structure de données qui permet de stocker plusieurs valeurs de **même type** dans une seule variable.
Au lieu de déclarer plusieurs variables séparées (par exemple `note1`, `note2`, `note3`), on utilise un tableau qui regroupe toutes les valeurs.

**Caractéristiques :**

* Les éléments d’un tableau sont **indexés** à partir de 0.
* Tous les éléments doivent être du même type (int, double, String, etc.).
* La taille d’un tableau est **fixe** une fois déclarée.

---

## 4.2. Déclaration et Initialisation

### 4.2.1. Déclaration

```java
int[] notes;       // déclaration d'un tableau d'entiers
double[] prix;     // déclaration d'un tableau de réels
String[] noms;     // déclaration d'un tableau de chaînes de caractères
```

### 4.2.2. Allocation (taille fixe)

```java
notes = new int[5];  // tableau de 5 entiers (cases de 0 à 4)
```

### 4.2.3. Déclaration + Allocation en une ligne

```java
int[] notes = new int[5];
```

### 4.2.4. Initialisation directe avec des valeurs

```java
int[] nombres = {10, 20, 30, 40, 50};
String[] jours = {"Lundi", "Mardi", "Mercredi"};
```

---

## 4.3. Accès aux Éléments d’un Tableau

* Les indices commencent à `0`.
* Pour un tableau de taille `n`, le dernier élément est à l’indice `n-1`.

```java
int[] notes = {12, 15, 17, 10, 14};
System.out.println(notes[0]); // affiche 12
System.out.println(notes[4]); // affiche 14
```

---

## 4.4. Parcours d’un Tableau

### 4.4.1. Avec une boucle `for`

```java
int[] notes = {12, 15, 17, 10, 14};
for (int i = 0; i < notes.length; i++) {
    System.out.println("Note " + i + " = " + notes[i]);
}
```

Explication :

* `notes.length` retourne la taille du tableau.
* `i` varie de `0` à `notes.length - 1`.

### 4.4.2. Avec une boucle `for-each`

```java
for (int note : notes) {
    System.out.println(note);
}
```

Le `for-each` parcourt directement les éléments sans manipuler les indices.

---

## 4.5. Tableaux Multidimensionnels

Un **tableau à deux dimensions** (2D) est utilisé pour représenter des **matrices** ou des **tableaux de tableaux**.

### 4.5.1. Déclaration

```java
int[][] matrice = new int[3][4]; // 3 lignes et 4 colonnes
```

### 4.5.2. Initialisation

```java
int[][] matrice = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

### 4.5.3. Parcours avec deux boucles imbriquées

```java
for (int i = 0; i < matrice.length; i++) {
    for (int j = 0; j < matrice[i].length; j++) {
        System.out.print(matrice[i][j] + " ");
    }
    System.out.println();
}
```

---

## 4.6. Erreurs Courantes à Éviter

1. **Indice en dehors des limites**

   ```java
   int[] tab = {1, 2, 3};
   System.out.println(tab[3]); // Erreur ! Indice hors limite
   ```

   → Indices possibles : 0, 1, 2.

2. **Ne pas oublier d’allouer la mémoire**

   ```java
   int[] tab;
   tab[0] = 5; // Erreur ! Tableau non initialisé
   ```

3. **Confusion entre taille et dernier indice**

   * Taille = `tab.length`
   * Dernier indice = `tab.length - 1`

---

## 4.7. Exemples Pratiques

### Exemple 1 : Somme des éléments d’un tableau

```java
int[] nombres = {5, 8, 12, 20};
int somme = 0;

for (int i = 0; i < nombres.length; i++) {
    somme += nombres[i];
}

System.out.println("Somme = " + somme);
```

### Exemple 2 : Trouver le maximum

```java
int[] nombres = {12, 7, 25, 18, 30};
int max = nombres[0];

for (int i = 1; i < nombres.length; i++) {
    if (nombres[i] > max) {
        max = nombres[i];
    }
}

System.out.println("Maximum = " + max);
```

---

## 4.8. Exercices

1. Déclarer un tableau de 10 entiers et l’initialiser avec des valeurs saisies par l’utilisateur.
2. Calculer la **somme et la moyenne** des éléments d’un tableau.
3. Trouver le **minimum et le maximum** dans un tableau d’entiers.
4. Compter le nombre d’éléments **pairs** et **impairs** dans un tableau.
5. Vérifier si un tableau contient une valeur donnée (recherche).
6. Inverser les éléments d’un tableau (exemple : `{1,2,3}` → `{3,2,1}`).
7. Trier un tableau en ordre croissant (méthode du tri à bulles).
8. Multiplier deux matrices 2D de dimensions compatibles.
9. Créer un programme qui lit une **matrice carrée** et affiche sa **diagonale principale**.
10. Écrire un programme qui affiche la **somme des éléments d’une ligne donnée** d’une matrice.

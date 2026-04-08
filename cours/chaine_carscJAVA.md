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

# Chapitre 5 : Les Chaînes de Caractères en Java
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <img src="java.webp" alt="ISI" width="50px">

---
## 1. Introduction aux chaînes de caractères

Une **chaîne de caractères** (ou *string*) est une suite de caractères utilisée pour représenter du texte.
En Java, les chaînes sont représentées par la classe **`String`** qui fait partie du package de base `java.lang`.

Contrairement à d’autres langages où les chaînes sont des tableaux de caractères terminés par `\0` (comme en C), en Java les objets de type `String` sont **immuables** :

> Une fois créées, leur contenu ne peut pas être modifié.

Cela signifie que chaque opération de modification d’une chaîne produit **une nouvelle chaîne en mémoire**.

---

## 2. Déclaration et initialisation

On peut déclarer une chaîne de plusieurs manières :

```java
public class ExempleString {
    public static void main(String[] args) {
        String s1 = "Bonjour"; // Déclaration simple
        String s2 = new String("Salut"); // Utilisation du constructeur (rarement nécessaire)
        
        System.out.println(s1); 
        System.out.println(s2);
    }
}
```

---

## 3. Quelques méthodes utiles de la classe `String`

### a) Longueur d’une chaîne

```java
String texte = "Programmation";
System.out.println("Longueur : " + texte.length());
```

`length()` retourne le nombre de caractères.

---

### b) Accéder à un caractère

```java
String mot = "Java";
System.out.println("Premier caractère : " + mot.charAt(0));
System.out.println("Dernier caractère : " + mot.charAt(mot.length() - 1));
```

`charAt(i)` donne le caractère à l’indice `i`.

---

### c) Concaténation

```java
String prenom = "Ali";
String nom = "Diop";
String nomComplet = prenom + " " + nom;
System.out.println("Nom complet : " + nomComplet);
```

On peut utiliser `+` ou `concat()`.

---

### d) Comparaison de chaînes

```java
String a = "Java";
String b = "java";

System.out.println(a.equals(b));      // false (sensible à la casse)
System.out.println(a.equalsIgnoreCase(b)); // true (insensible à la casse)
```

`equals()` compare le contenu, contrairement à `==` qui compare les références mémoire.

---

### e) Transformation

```java
String phrase = "Bonjour le monde";
System.out.println(phrase.toUpperCase()); // MAJUSCULES
System.out.println(phrase.toLowerCase()); // minuscules
System.out.println(phrase.trim());        // supprime espaces au début et à la fin
```

---

### f) Recherche et sous-chaîne

```java
String texte = "Programmation Java";
System.out.println(texte.contains("Java"));  // true
System.out.println(texte.indexOf("Java"));   // 14
System.out.println(texte.substring(0, 7));   // "Program"
```

---

## 4. Tableaux de caractères (`char[]`) vs String

En Java, une chaîne peut être convertie en tableau de caractères :

```java
String mot = "Bonjour";
char[] lettres = mot.toCharArray();

for (char c : lettres) {
    System.out.print(c + " ");
}
```

Inversement, un tableau de caractères peut être transformé en chaîne :

```java
char[] tab = {'J','a','v','a'};
String mot2 = new String(tab);
System.out.println(mot2); // Java
```

---

## 5. Erreurs fréquentes à éviter

1. **Confondre `==` et `equals()`**

   * `==` compare les adresses mémoire
   * `equals()` compare le contenu

2. **Oublier que les `String` sont immuables**
   Exemple :

   ```java
   String s = "Hello";
   s.concat(" World");
   System.out.println(s); // Affiche "Hello" et non "Hello World"
   ```

   Solution :

   ```java
   s = s.concat(" World");
   ```

3. **Confusion entre `length` (tableaux) et `length()` (chaînes)**

   * Tableau : `tab.length`
   * Chaîne : `chaine.length()`

---

## 6. Exemples d’application

### Exemple 1 : Compter le nombre de voyelles dans une chaîne

```java
public class Voyelles {
    public static void main(String[] args) {
        String texte = "Informatique";
        int compteur = 0;

        for (int i = 0; i < texte.length(); i++) {
            char c = Character.toLowerCase(texte.charAt(i));
            if ("aeiouy".indexOf(c) != -1) {
                compteur++;
            }
        }
        System.out.println("Nombre de voyelles : " + compteur);
    }
}
```

---

### Exemple 2 : Vérifier si une chaîne est un palindrome

```java
public class Palindrome {
    public static void main(String[] args) {
        String mot = "radar";
        String inverse = "";

        for (int i = mot.length() - 1; i >= 0; i--) {
            inverse += mot.charAt(i);
        }

        if (mot.equals(inverse)) {
            System.out.println(mot + " est un palindrome");
        } else {
            System.out.println(mot + " n'est pas un palindrome");
        }
    }
}
```

---

## 7. Exercices pratiques

### Exercice 1 :

Écrire un programme qui lit une chaîne et compte le nombre d’espaces.

### Exercice 2 :

Écrire un programme qui demande une phrase et affiche le nombre de mots.

### Exercice 3 :

Écrire un programme qui demande une chaîne et affiche sa version inversée.

### Exercice 4 :

Écrire un programme qui vérifie si une chaîne donnée contient seulement des chiffres.

### Exercice 5 :

Écrire un programme qui demande deux chaînes et teste si elles sont des anagrammes.


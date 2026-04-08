## Exercices Java procédural

### Exercice Niveau basic 

### Exercice 1: Somme de deux nombres

Écrivez un programme qui demande à l'utilisateur deux nombres, puis affiche leur somme.


### Exercice 2: Vérification de la parité

Écrivez un programme qui demande à l'utilisateur un nombre et indique s'il est pair ou impair.


### Exercice 3: Calcul du factoriel

Écrivez un programme qui calcule le factoriel d'un nombre.

### Exercice 4: Vérification de nombre premier

Écrivez un programme qui vérifie si un nombre est premier.
<!-- 
### Exercice 5: Inversion d'un nombre

Écrivez un programme qui inverse les chiffres d'un nombre (par exemple, 12345 devrait devenir 54321). -->

### Exercice 5: Génération de nombres de Fibonacci

Écrivez un programme qui génère les n premiers nombres de la séquence de Fibonacci.
les premiers termes de la suite de Fibonacci sont généralement :

0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
<!-- 
La formule récurrente pour calculer les termes de la suite de Fibonacci est la suivante :

\[ F(n) = F(n-1) + F(n-2) \] -->



### Exercice 6: Palindrome

Écrivez un programme qui vérifie si un mot est un palindrome.
Voici un exemple de mot palindrome :

"radar"

Lorsque vous lisez le mot "radar" de gauche à droite ou de droite à gauche, il reste le même. Les palindromes sont intéressants en raison de leur symétrie.



### Exercice 7: Conversion de température

Écrivez un programme qui convertit une température en Celsius en Fahrenheit et vice versa.

La conversion entre Celsius (°C) et Fahrenheit (°F) peut être effectuée à l'aide des formules suivantes :

1. De Celsius à Fahrenheit :
\[ F = 9/5 C + 32 \]

2. De Fahrenheit à Celsius :
\[ C = 5/9F - 32 \]

Exemples :

1. Conversion de 25°C en Fahrenheit :
\[ F = 9/5 * 25 + 32 = 77°F \]

2. Conversion de 98.6°F en Celsius :
\[ C = 5/9 * (98.6 - 32) = 37°C \]


### Exercice 8: Calculatrice simple

Écrivez un programme qui fonctionne comme une calculatrice simple, permettant à l'utilisateur d'effectuer des opérations de base (+, -, *, /). Le programme demande d'entrer le premier nombre, puis l'operateur et enfin le deuxieme nombre et fait l'operation.



<!-- ### Exercice 9: Calcul de la somme des chiffres

Écrivez un programme qui calcule la somme des chiffres d'un nombre.

### Solution 10:
```java
import java.util.Scanner;

public class SommeChiffres {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre : ");
        int nombre = scanner.nextInt();

        int somme = 0;

        while (nombre != 0) {
            somme += nombre % 10;
            nombre /= 10;
        }

        System.out.println("La somme des chiffres est : " + somme);

        scanner.close();
    }
}
``` -->

<!-- Ces exercices couvrent divers aspects de la programmation procédurale en Java, des concepts de base aux défis un peu plus avancés. N'hésitez pas à les implémenter et à les expérimenter pour renforcer votre compréhension du langage Java. Si vous avez des questions spécifiques sur l'un des exercices, n'hésitez pas à demander ! -->


## Niveau Intermédiare

### Exercice 1: Calcul de Moyenne

**Objectif :** Écrire une fonction qui calcule la moyenne de plusieurs nombres.


**Explications :** La fonction `calculerMoyenne` prend un tableau d'entiers en entrée, somme ces nombres, puis divise la somme par la taille du tableau pour obtenir la moyenne.

---

### Exercice 2: Recherche Binaire

**Objectif :** Implémenter l'algorithme de recherche binaire pour trouver un élément dans un tableau trié.



**Explications :** La fonction `rechercheBinaire` divise de manière récursive le tableau en deux parties, puis compare l'élément avec la valeur au milieu du tableau pour déterminer dans quelle moitié la recherche doit continuer.

---

### Exercice 3: Tri à Bulles

**Objectif :** Implémenter l'algorithme de tri à bulles pour trier un tableau d'entiers.

**Explications :** La fonction `triBulles` effectue des comparaisons adjacentes et échange les éléments s'ils sont dans le mauvais ordre, itérant sur le tableau jusqu'à ce qu'il soit trié.

---

### Exercice 4: Gestion des Chaînes de Caractères

**Objectif :** Écrire une fonction qui compte le nombre de voyelles dans une chaîne de caractères.


**Explications :** La fonction `compterVoyelles` itère sur chaque caractère de la chaîne, le convertit en minuscule, puis incrémente

 un compteur si le caractère est une voyelle.

---

### Exercice 5: Manipulation de Fichiers

**Objectif :** Écrire un programme qui copie le contenu d'un fichier source dans un fichier destination.


**Explications :** La fonction `copierFichier` utilise les classes `BufferedReader` et `BufferedWriter` pour lire et écrire le contenu du fichier source dans le fichier destination.

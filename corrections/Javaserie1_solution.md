# Solutions – Série Java 
```java
import java.util.Scanner;

public class Serie1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // EXERCICE 1
        System.out.println("=== Exercice 1 ===");
        System.out.print("Entrez le premier nombre : ");
        int a = sc.nextInt();
        System.out.print("Entrez le deuxième nombre : ");
        int b = sc.nextInt();
        System.out.println("Somme = " + (a + b));
        System.out.println("Différence = " + (a - b));
        System.out.println("Produit = " + (a * b));
        if (b != 0) {
            System.out.println("Quotient = " + (a / b));
        } else {
            System.out.println("Division impossible (b = 0)");
        }v

        // EXERCICE 2
        System.out.println("\n=== Exercice 2 ===");
        final double PI = 3.14159; // constante
        System.out.print("Entrez le rayon du cercle : ");
        double r = sc.nextDouble();
        System.out.println("Périmètre = " + (2 * PI * r));
        System.out.println("Aire = " + (PI * r * r));

        // EXERCICE 3
        System.out.println("\n=== Exercice 3 ===");
        System.out.print("Entrez trois nombres : ");
        int n1 = sc.nextInt();
        int n2 = sc.nextInt();
        int n3 = sc.nextInt();
        int max = n1;
        if (n2 > max) max = n2;
        if (n3 > max) max = n3;
        System.out.println("Le plus grand est : " + max);

        // EXERCICE 4
        System.out.println("\n=== Exercice 4 ===");
        System.out.print("Entrez une note (0-20) : ");
        int note = sc.nextInt();
        if (note >= 16) System.out.println("Très bien");
        else if (note >= 14) System.out.println("Bien");
        else if (note >= 12) System.out.println("Assez bien");
        else if (note >= 10) System.out.println("Passable");
        else System.out.println("Échec");

        // EXERCICE 5
        System.out.println("\n=== Exercice 5 ===");
        System.out.print("Entrez un entier : ");
        int x = sc.nextInt();
        if (x % 2 == 0) System.out.println("Pair");
        else System.out.println("Impair");
        if (x >= 0) System.out.println("Positif");
        else System.out.println("Négatif");

        // EXERCICE 6
        System.out.println("\n=== Exercice 6 ===");
        System.out.print("Entrez un jour (1-7) : ");
        int jour = sc.nextInt();
        switch (jour) {
            case 1 -> System.out.println("Lundi");
            case 2 -> System.out.println("Mardi");
            case 3 -> System.out.println("Mercredi");
            case 4 -> System.out.println("Jeudi");
            case 5 -> System.out.println("Vendredi");
            case 6 -> System.out.println("Samedi");
            case 7 -> System.out.println("Dimanche");
            default -> System.out.println("Jour invalide");
        }

        // EXERCICE 7
        System.out.println("\n=== Exercice 7 ===");
        System.out.print("Entrez un mois (1-12) : ");
        int mois = sc.nextInt();
        switch (mois) {
            case 1, 3, 5, 7, 8, 10, 12 -> System.out.println("31 jours");
            case 4, 6, 9, 11 -> System.out.println("30 jours");
            case 2 -> System.out.println("28 ou 29 jours");
            default -> System.out.println("Mois invalide");
        }

        // EXERCICE 8
        System.out.println("\n=== Exercice 8 ===");
        sc.nextLine(); // vider le buffer
        System.out.print("Entrez un mot de passe : ");
        String mdp = sc.nextLine();
        if (mdp.equals("Java2025")) System.out.println("Accès autorisé");
        else System.out.println("Accès refusé");

        // EXERCICE 9
        System.out.println("\n=== Exercice 9 ===");
        System.out.print("Entrez un nombre positif : ");
        int n = sc.nextInt();
        for (int i = 1; i <= n; i++) {
            System.out.print(i + " ");
        }
        System.out.println();

        // EXERCICE 10
        System.out.println("\n=== Exercice 10 ===");
        System.out.print("Entrez un nombre : ");
        int m = sc.nextInt();
        for (int i = 2; i <= m; i += 2) {
            System.out.print(i + " ");
        }
        System.out.println();

        sc.close();
    }
}
```

---

## Notions importantes à remarquer

* **Division par zéro** : toujours vérifier avant de diviser (exercice 1).
* **Constante en Java** : mot-clé `final` (exercice 2).
* **Maximum de 3 valeurs** : on compare pas à pas (exercice 3).
* **Chaînage de conditions (`if...else if`)** : pratique pour des intervalles (exercice 4).
* **Modulo `%`** : permet de tester la parité (exercice 5).
* **Switch-case** : utilisé pour éviter des `if` répétés (exercice 6 et 7).
* **Comparaison de chaînes** : `equals()` et non `==` (exercice 8).
* **Boucles `for`** : incrémentation classique et avec pas de 2 pour les pairs (exercice 9 et 10).

---
(Exercices 11 à 20)

```java
import java.util.Scanner;

public class Serie2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // EXERCICE 11
        System.out.println("=== Exercice 11 ===");
        System.out.print("Entrez un entier N : ");
        int N = sc.nextInt();
        int somme = 0;
        for (int i = 1; i <= N; i++) {
            somme += i;
        }
        System.out.println("Somme de 1 à " + N + " = " + somme);

        // EXERCICE 12
        System.out.println("\n=== Exercice 12 ===");
        System.out.print("Entrez un entier N : ");
        int Nfact = sc.nextInt();
        long fact = 1;
        for (int i = 1; i <= Nfact; i++) {
            fact *= i;
        }
        System.out.println("Factorielle de " + Nfact + " = " + fact);

        // EXERCICE 13
        System.out.println("\n=== Exercice 13 ===");
        int total = 0, val;
        do {
            System.out.print("Entrez un nombre (0 pour arrêter) : ");
            val = sc.nextInt();
            total += val;
        } while (val != 0);
        System.out.println("Somme = " + total);

        // EXERCICE 14
        System.out.println("\n=== Exercice 14 ===");
        System.out.print("Entrez un nombre : ");
        int num = sc.nextInt();
        System.out.println("Diviseurs de " + num + " : ");
        for (int i = 1; i <= num; i++) {
            if (num % i == 0) {
                System.out.print(i + " ");
            }
        }
        System.out.println();

        // EXERCICE 15
        System.out.println("\n=== Exercice 15 ===");
        int entier;
        do {
            System.out.print("Entrez un entier inférieur à 100 : ");
            entier = sc.nextInt();
        } while (entier >= 100);
        System.out.println("Vous avez entré : " + entier);

        // EXERCICE 16
        System.out.println("\n=== Exercice 16 ===");
        System.out.print("Entrez un nombre : ");
        int nb = sc.nextInt();
        for (int i = 1; i <= 10; i++) {
            System.out.println(nb + " x " + i + " = " + (nb * i));
        }

        // EXERCICE 17
        System.out.println("\n=== Exercice 17 ===");
        System.out.print("Entrez un entier N : ");
        int Nc = sc.nextInt();
        for (int i = 1; i <= Nc; i++) {
            System.out.println("Carré de " + i + " = " + (i * i));
        }

        // EXERCICE 18
        System.out.println("\n=== Exercice 18 ===");
        System.out.print("Entrez un nombre : ");
        int nimp = sc.nextInt();
        for (int i = 1; i <= nimp; i += 2) {
            System.out.print(i + " ");
        }
        System.out.println();

        // EXERCICE 19
        System.out.println("\n=== Exercice 19 ===");
        int nb19;
        while (true) {
            System.out.print("Entrez un nombre : ");
            nb19 = sc.nextInt();
            if (nb19 > 50) break;
            System.out.println("Vous avez entré : " + nb19);
        }
        System.out.println("Saisie arrêtée car le nombre > 50");

        // EXERCICE 20
        System.out.println("\n=== Exercice 20 ===");
        int max = Integer.MIN_VALUE;
        int min = Integer.MAX_VALUE;
        int somme20 = 0;
        for (int i = 1; i <= 5; i++) {
            System.out.print("Entrez le nombre " + i + " : ");
            int val20 = sc.nextInt();
            if (val20 > max) max = val20;
            if (val20 < min) min = val20;
            somme20 += val20;
        }
        double moyenne = somme20 / 5.0;
        System.out.println("Maximum = " + max);
        System.out.println("Minimum = " + min);
        System.out.println("Moyenne = " + moyenne);

        sc.close();
    }
}
```

---

## Notions importantes à remarquer

* **Somme d’une série (Ex11)** → on initialise `somme = 0` puis on additionne dans une boucle.
* **Factorielle (Ex12)** → produit des entiers de 1 à N, attention aux grands N (`long`).
* **Boucle avec condition d’arrêt utilisateur (Ex13)** → `do...while` pratique pour répéter au moins une fois.
* **Diviseurs (Ex14)** → on teste avec `%` pour savoir si un nombre est divisible.
* **Validation de saisie (Ex15)** → boucle `do...while` jusqu’à ce que la condition soit respectée.
* **Table de multiplication (Ex16)** → boucle `for` classique.
* **Carrés (Ex17)** → calcul direct dans la boucle.
* **Nombres impairs (Ex18)** → incrément `i += 2`.
* **Arrêt conditionnel (Ex19)** → `break` utilisé dans une boucle infinie.
* **Min, Max, Moyenne (Ex20)** → utilisation de `Integer.MIN_VALUE` et `Integer.MAX_VALUE` comme bornes initiales.

---
(Exercices 21 à 30)

```java
import java.util.Scanner;

public class Serie3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // EXERCICE 21 : nombre premier
        System.out.println("=== Exercice 21 ===");
        System.out.print("Entrez un nombre : ");
        int n21 = sc.nextInt();
        boolean estPremier = true;
        if (n21 < 2) estPremier = false;
        else {
            for (int i = 2; i <= Math.sqrt(n21); i++) {
                if (n21 % i == 0) {
                    estPremier = false;
                    break;
                }
            }
        }
        if (estPremier) System.out.println(n21 + " est un nombre premier");
        else System.out.println(n21 + " n'est pas un nombre premier");

        // EXERCICE 22 : longueur et caractères
        System.out.println("\n=== Exercice 22 ===");
        System.out.print("Entrez un mot : ");
        sc.nextLine(); // vider le buffer
        String mot = sc.nextLine();
        System.out.println("Longueur du mot : " + mot.length());
        for (int i = 0; i < mot.length(); i++) {
            System.out.println("Caractère " + (i+1) + " : " + mot.charAt(i));
        }

        // EXERCICE 23 : Fibonacci
        System.out.println("\n=== Exercice 23 ===");
        System.out.print("Entrez un nombre N : ");
        int N23 = sc.nextInt();
        int a = 0, b = 1;
        System.out.print("Fibonacci : ");
        for (int i = 1; i <= N23; i++) {
            System.out.print(a + " ");
            int temp = a + b;
            a = b;
            b = temp;
        }
        System.out.println();

        // EXERCICE 24 : nombres parfaits
        System.out.println("\n=== Exercice 24 ===");
        System.out.print("Entrez N : ");
        int N24 = sc.nextInt();
        System.out.println("Nombres parfaits <= " + N24 + " :");
        for (int num = 2; num <= N24; num++) {
            int sommeDiv = 0;
            for (int i = 1; i <= num/2; i++) {
                if (num % i == 0) sommeDiv += i;
            }
            if (sommeDiv == num) System.out.println(num);
        }

        // EXERCICE 25 : min et max sans connaître la taille
        System.out.println("\n=== Exercice 25 ===");
        int max = Integer.MIN_VALUE, min = Integer.MAX_VALUE, val25, somme25 = 0, count = 0;
        do {
            System.out.print("Entrez un nombre (0 pour arrêter) : ");
            val25 = sc.nextInt();
            if (val25 != 0) {
                if (val25 > max) max = val25;
                if (val25 < min) min = val25;
                somme25 += val25;
                count++;
            }
        } while (val25 != 0);
        if (count > 0) {
            System.out.println("Max = " + max + ", Min = " + min);
        } else {
            System.out.println("Aucun nombre entré !");
        }

        // EXERCICE 26 : moyenne des notes
        System.out.println("\n=== Exercice 26 ===");
        int sup10 = 0, somme26 = 0;
        for (int i = 1; i <= 10; i++) {
            System.out.print("Entrez la note " + i + " : ");
            int note = sc.nextInt();
            somme26 += note;
            if (note >= 10) sup10++;
        }
        double moyenne26 = somme26 / 10.0;
        System.out.println("Moyenne = " + moyenne26);
        System.out.println("Nombre de notes >= 10 : " + sup10);

        // EXERCICE 27 : table interrompue
        System.out.println("\n=== Exercice 27 ===");
        System.out.print("Entrez un nombre : ");
        int nb27 = sc.nextInt();
        for (int i = 1; i <= 10; i++) {
            int produit = nb27 * i;
            if (produit > 50) break;
            System.out.println(nb27 + " x " + i + " = " + produit);
        }

        // EXERCICE 28 : somme des pairs
        System.out.println("\n=== Exercice 28 ===");
        System.out.print("Entrez un entier N : ");
        int N28 = sc.nextInt();
        int sommePairs = 0;
        for (int i = 2; i <= N28; i += 2) {
            sommePairs += i;
        }
        System.out.println("Somme des pairs = " + sommePairs);

        // EXERCICE 29 : positifs, négatifs, nuls
        System.out.println("\n=== Exercice 29 ===");
        int pos = 0, neg = 0, nul = 0;
        for (int i = 1; i <= 5; i++) {
            System.out.print("Entrez le nombre " + i + " : ");
            int nb29 = sc.nextInt();
            if (nb29 > 0) pos++;
            else if (nb29 < 0) neg++;
            else nul++;
        }
        System.out.println("Positifs = " + pos + ", Négatifs = " + neg + ", Nuls = " + nul);

        // EXERCICE 30 : diviseurs pairs
        System.out.println("\n=== Exercice 30 ===");
        System.out.print("Entrez un nombre : ");
        int nb30 = sc.nextInt();
        System.out.println("Diviseurs pairs de " + nb30 + " : ");
        for (int i = 1; i <= nb30; i++) {
            if (nb30 % i == 0 && i % 2 == 0) {
                System.out.print(i + " ");
            }
        }
        System.out.println();

        sc.close();
    }
}
```

---

## Points importants (Ex21 → Ex30)

* **Nombre premier (Ex21)** → tester jusqu’à `sqrt(n)` optimise la recherche.
* **Chaînes (Ex22)** → `nextLine()` après un `nextInt()` → il faut vider le buffer (`sc.nextLine()`).
* **Fibonacci (Ex23)** → progression par somme des deux précédents.
* **Nombres parfaits (Ex24)** → somme des diviseurs propres. Exemple : 6 = 1 + 2 + 3.
* **Lecture illimitée (Ex25)** → condition d’arrêt avec `0`, utile pour flux de données inconnues.
* **Moyenne des notes (Ex26)** → attention au `double` pour éviter division entière.
* **Table interrompue (Ex27)** → usage de `break` dans une boucle.
* **Somme des pairs (Ex28)** → boucle par pas de `2`.
* **Comptage (Ex29)** → classification avec `if / else if / else`.
* **Diviseurs pairs (Ex30)** → combinaison de deux conditions avec `&&`.



Parfait, voici donc la **correction complète et détaillée** des **10 exercices Java** que tu as partagés, en respectant ton style pédagogique (code clair, explication simple, notion bien posée). Ces corrections respectent les chapitres 1 à 3 : variables, conditions, et boucles.

---

## ✅ Correction et explication des exercices

---

### **Exercice 1 – Classification par tranche d'âge**

```java
import java.util.Scanner;

public class Exo1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Entrez votre âge : ");
        int age = sc.nextInt();

        if (age < 12)
            System.out.println("Enfant");
        else if (age <= 17)
            System.out.println("Adolescent");
        else if (age <= 25)
            System.out.println("Jeune adulte");
        else if (age <= 59)
            System.out.println("Adulte");
        else
            System.out.println("Senior");

        sc.close();
    }
}
```

🧠 **Explication** :

* L'enchaînement `if...else if` permet de tester les tranches.
* `<=` permet d'inclure les bornes (par exemple 17 inclus dans "Adolescent").
* Structure classique et claire à présenter en cours.

---

### **Exercice 2 – Analyse d’un entier**

```java
import java.util.Scanner;

public class Exo2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez un entier : ");
        int n = sc.nextInt();

        // Signe
        if (n >= 0) System.out.println("Positif");
        else System.out.println("Négatif");

        // Parité
        if (n % 2 == 0) System.out.println("Pair");
        else System.out.println("Impair");

        // Multiples
        if (n % 3 == 0 && n % 5 == 0)
            System.out.println("Multiple de 3 et 5");
        else if (n % 3 == 0)
            System.out.println("Multiple de 3");
        else if (n % 5 == 0)
            System.out.println("Multiple de 5");
        else
            System.out.println("Pas multiple de 3 ni 5");

        sc.close();
    }
}
```

💡 **Notions** :

* `%` est l’opérateur modulo (reste de la division).
* `&&` pour tester les deux en même temps.

---

### **Exercice 3 – Nom du mois à partir du numéro**

```java
import java.util.Scanner;

public class Exo3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez un numéro de mois (1-12) : ");
        int mois = sc.nextInt();

        switch (mois) {
            case 1: System.out.println("Janvier"); break;
            case 2: System.out.println("Février"); break;
            case 3: System.out.println("Mars"); break;
            case 4: System.out.println("Avril"); break;
            case 5: System.out.println("Mai"); break;
            case 6: System.out.println("Juin"); break;
            case 7: System.out.println("Juillet"); break;
            case 8: System.out.println("Août"); break;
            case 9: System.out.println("Septembre"); break;
            case 10: System.out.println("Octobre"); break;
            case 11: System.out.println("Novembre"); break;
            case 12: System.out.println("Décembre"); break;
            default: System.out.println("Numéro invalide !");
        }

        sc.close();
    }
}
```

📌 **Remarques** :

* Le `switch` ne prend que des `int`, `char`, `enum`, `String` en Java (à partir de Java 7).
* Le `default` est indispensable pour gérer les erreurs.

---

### **Exercice 4 – Jour de la semaine**

```java
import java.util.Scanner;

public class Exo4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez un jour (en minuscule) : ");
        String jour = sc.nextLine();

        switch (jour) {
            case "lundi": System.out.println("Jour 1"); break;
            case "mardi": System.out.println("Jour 2"); break;
            case "mercredi": System.out.println("Jour 3"); break;
            case "jeudi": System.out.println("Jour 4"); break;
            case "vendredi": System.out.println("Jour 5"); break;
            case "samedi": System.out.println("Jour 6"); break;
            case "dimanche": System.out.println("Jour 7"); break;
            default: System.out.println("Jour inconnu !");
        }

        sc.close();
    }
}
```

🎯 **Points clés** :

* On travaille ici avec des `String` → switch possible avec Java ≥ 7.
* Important de rappeler que Java est sensible à la casse (`lundi` ≠ `Lundi`).

---

### **Exercice 5 – Bulletin scolaire**

```java
import java.util.Scanner;

public class Exo5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez votre note (sur 20) : ");
        float note = sc.nextFloat();

        if (note >= 16)
            System.out.println("Très bien");
        else if (note >= 14)
            System.out.println("Bien");
        else if (note >= 12)
            System.out.println("Assez bien");
        else if (note >= 10)
            System.out.println("Passable");
        else
            System.out.println("Insuffisant");

        sc.close();
    }
}
```

🧠 **Notions** :

* Priorité du `if` du plus grand vers le plus petit.
* Utilisation du type `float` permet les notes décimales (12.5, etc.).

---

### **Exercice 6 – Mini-calculatrice**

```java
import java.util.Scanner;

public class Exo6 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez le 1er nombre : ");
        int a = sc.nextInt();
        System.out.print("Entrez le 2e nombre : ");
        int b = sc.nextInt();
        System.out.print("Opération (+, -, *, /) : ");
        char op = sc.next().charAt(0);

        switch (op) {
            case '+': System.out.println("Résultat = " + (a + b)); break;
            case '-': System.out.println("Résultat = " + (a - b)); break;
            case '*': System.out.println("Résultat = " + (a * b)); break;
            case '/':
                if (b != 0)
                    System.out.println("Résultat = " + (a / b));
                else
                    System.out.println("Erreur : division par zéro !");
                break;
            default: System.out.println("Opérateur inconnu !");
        }

        sc.close();
    }
}
```

📌 **Concepts** :

* Lecture de caractère avec `next().charAt(0)`
* Test d’erreur `if (b != 0)` avant de diviser.

---

### **Exercice 7 – Nombre en lettres**

```java
import java.util.Scanner;

public class Exo7 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Entrez un chiffre (0 à 9) : ");
        int n = sc.nextInt();

        switch (n) {
            case 0: System.out.println("zéro"); break;
            case 1: System.out.println("un"); break;
            case 2: System.out.println("deux"); break;
            case 3: System.out.println("trois"); break;
            case 4: System.out.println("quatre"); break;
            case 5: System.out.println("cinq"); break;
            case 6: System.out.println("six"); break;
            case 7: System.out.println("sept"); break;
            case 8: System.out.println("huit"); break;
            case 9: System.out.println("neuf"); break;
            default: System.out.println("Chiffre invalide !");
        }

        sc.close();
    }
}
```

---

### **Exercice 8 – Vérification de mot de passe**

```java
import java.util.Scanner;

public class Exo8 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Saisir le mot de passe : ");
        String mdp = sc.nextLine();

        if (mdp.equals("Java2025"))
            System.out.println("Mot de passe correct !");
        else
            System.out.println("Mot de passe incorrect.");

        sc.close();
    }
}
```

🔐 **À retenir** :

* Comparaison de chaînes avec `equals()`.
* `==` ne fonctionne pas pour tester deux chaînes en Java.

---

### **Exercice 9 – Permutation sans variable temporaire**

```java
import java.util.Scanner;

public class Exo9 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("a = ");
        int a = sc.nextInt();
        System.out.print("b = ");
        int b = sc.nextInt();

        System.out.println("Avant permutation : a=" + a + ", b=" + b);

        a = a + b;
        b = a - b;
        a = a - b;

        System.out.println("Après permutation : a=" + a + ", b=" + b);
        sc.close();
    }
}
```

🧠 **Technique** :

* Utilise l’algèbre (sans 3e variable).
* Alternative : XOR (plus complexe à ce stade).

---

### **Exercice 10 – Analyse de température**

```java
import java.util.Scanner;

public class Exo10 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Température : ");
        float t = sc.nextFloat();

        if (t < 5)
            System.out.println("Très froid");
        else if (t <= 15)
            System.out.println("Frais");
        else if (t <= 25)
            System.out.println("Tempéré");
        else if (t <= 35)
            System.out.println("Chaud");
        else
            System.out.println("Canicule");

        sc.close();
    }
}
```

🌡️ **À retenir** :

* Lecture d’un `float` avec `nextFloat()`.
* Valeurs numériques utilisées comme bornes d’intervalles.

Parfait, voici les **corrections détaillées** des exercices **11 à 20**, avec :

* Code Java clair et exécutable ;
* Utilisation du **Scanner** ;
* Explications simples et pédagogiques juste après chaque solution ;
* Difficulté progressive respectée.

---

# ✅ **CORRECTIONS – Série 2 (Exercices 11 à 20)**

> **Important :**
> On suppose que chaque programme est dans un fichier séparé (Exo11.java, Exo12.java, etc.).
> Pour éviter de fermer le `Scanner` à chaque fois, on le ferme **seulement à la fin du programme**.

---

### **Exercice 11 – Vérification de triangle valide**

```java
import java.util.Scanner;

public class Exo11 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Longueur a : ");
        double a = sc.nextDouble();
        System.out.print("Longueur b : ");
        double b = sc.nextDouble();
        System.out.print("Longueur c : ");
        double c = sc.nextDouble();

        if (a + b > c && a + c > b && b + c > a) {
            System.out.println("Ces longueurs forment un triangle valide.");
        } else {
            System.out.println("Ces longueurs NE forment PAS un triangle.");
        }

        sc.close();
    }
}
```

🧠 **Explication**
Un triangle est valide si **chaque côté est inférieur à la somme des deux autres**.
On teste donc les 3 combinaisons avec `&&`.

---

### **Exercice 12 – Type de triangle**

```java
import java.util.Scanner;

public class Exo12 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("a : ");
        double a = sc.nextDouble();
        System.out.print("b : ");
        double b = sc.nextDouble();
        System.out.print("c : ");
        double c = sc.nextDouble();

        if (a == b && b == c) {
            System.out.println("Triangle équilatéral");
        } else if (a == b || a == c || b == c) {
            System.out.println("Triangle isocèle");
        } else {
            System.out.println("Triangle scalène");
        }

        sc.close();
    }
}
```

🧠 **Explication**

* Tous égaux → équilatéral
* Deux égaux → isocèle
* Aucun égal → scalène

---

### **Exercice 13 – Max et Min parmi 3 valeurs**

```java
import java.util.Scanner;

public class Exo13 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Entrez trois entiers : ");
        int x = sc.nextInt();
        int y = sc.nextInt();
        int z = sc.nextInt();

        int max = x;
        if (y > max) max = y;
        if (z > max) max = z;

        int min = x;
        if (y < min) min = y;
        if (z < min) min = z;

        System.out.println("Max = " + max);
        System.out.println("Min = " + min);

        sc.close();
    }
}
```

🧠 **Explication**
On part du premier élément comme référence, puis on compare successivement.

---

### **Exercice 14 – Année bissextile**

```java
import java.util.Scanner;

public class Exo14 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Entrez une année : ");
        int an = sc.nextInt();

        if ((an % 4 == 0 && an % 100 != 0) || an % 400 == 0)
            System.out.println("Année bissextile");
        else
            System.out.println("Année non bissextile");

        sc.close();
    }
}
```

🧠 **Explication**
La règle bissextile est **conditionnelle** : divisible par 4 mais pas par 100, sauf si divisible par 400.

---

### **Exercice 15 – Validité d’identifiant**

```java
import java.util.Scanner;

public class Exo15 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Entrez un identifiant : ");
        String id = sc.nextLine();

        if (id.length() >= 6 && !Character.isDigit(id.charAt(0)) && !id.contains(" ")) {
            System.out.println("Identifiant valide.");
        } else {
            System.out.println("Identifiant invalide.");
        }

        sc.close();
    }
}
```

🧠 **Explication**

* `length()` vérifie la taille
* `charAt(0)` donne le **premier caractère**
* `Character.isDigit()` teste si c’est un chiffre
* `contains(" ")` détecte les espaces

---

### **Exercice 16 – Moyenne pondérée**

```java
import java.util.Scanner;

public class Exo16 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Note 1, coef 1 : ");
        double n1 = sc.nextDouble();
        double c1 = sc.nextDouble();

        System.out.print("Note 2, coef 2 : ");
        double n2 = sc.nextDouble();
        double c2 = sc.nextDouble();

        System.out.print("Note 3, coef 3 : ");
        double n3 = sc.nextDouble();
        double c3 = sc.nextDouble();

        double moy = (n1*c1 + n2*c2 + n3*c3) / (c1 + c2 + c3);
        System.out.println("Moyenne pondérée = " + moy);

        sc.close();
    }
}
```

🧠 **Explication**
La moyenne pondérée est :
[
\frac{n_1c_1 + n_2c_2 + n_3c_3}{c_1 + c_2 + c_3}
]

---

### **Exercice 17 – Vérification de date**

```java
import java.util.Scanner;

public class Exo17 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Jour : ");
        int j = sc.nextInt();
        System.out.print("Mois : ");
        int m = sc.nextInt();
        System.out.print("Année : ");
        int a = sc.nextInt();

        boolean bissextile = (a % 4 == 0 && a % 100 != 0) || a % 400 == 0;
        int nbJours;

        switch (m) {
            case 4, 6, 9, 11 -> nbJours = 30;
            case 2 -> nbJours = bissextile ? 29 : 28;
            case 1,3,5,7,8,10,12 -> nbJours = 31;
            default -> nbJours = -1;
        }

        if (nbJours != -1 && j >= 1 && j <= nbJours)
            System.out.println("Date valide.");
        else
            System.out.println("Date invalide.");

        sc.close();
    }
}
```

🧠 **Explication**
On détermine d’abord le nombre de jours du mois, puis on vérifie que le jour appartient à l’intervalle correct.

---

### **Exercice 18 – Menu avec switch**

```java
import java.util.Scanner;

public class Exo18 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("1) Bonjour");
        System.out.println("2) Somme de deux nombres");
        System.out.println("3) Quitter");
        System.out.print("Votre choix : ");
        int ch = sc.nextInt();

        switch (ch) {
            case 1 -> System.out.println("Bonjour !");
            case 2 -> {
                System.out.print("a : ");
                int a = sc.nextInt();
                System.out.print("b : ");
                int b = sc.nextInt();
                System.out.println("Somme = " + (a + b));
            }
            case 3 -> System.out.println("Fin du programme.");
            default -> System.out.println("Choix invalide.");
        }

        sc.close();
    }
}
```

---

### **Exercice 19 – Racines d’une équation**

```java
import java.util.Scanner;

public class Exo19 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("a : ");
        double a = sc.nextDouble();
        System.out.print("b : ");
        double b = sc.nextDouble();
        System.out.print("c : ");
        double c = sc.nextDouble();

        double d = b*b - 4*a*c;

        if (d < 0)
            System.out.println("Pas de solution réelle.");
        else if (d == 0)
            System.out.println("Une solution : x = " + (-b/(2*a)));
        else
            System.out.println("Deux solutions : x1 = " + ((-b+Math.sqrt(d))/(2*a)) +
                               ", x2 = " + ((-b-Math.sqrt(d))/(2*a)));

        sc.close();
    }
}
```

🧠 **Explication**

* Calcul du discriminant Δ = b² - 4ac
* `Math.sqrt()` pour la racine carrée

---

### **Exercice 20 – Jeu du nombre mystère**

```java
import java.util.Scanner;

public class Exo20 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int mystere = 27;
        int n;

        do {
            System.out.print("Devinez le nombre : ");
            n = sc.nextInt();

            if (n < mystere)
                System.out.println("Trop petit !");
            else if (n > mystere)
                System.out.println("Trop grand !");
            else
                System.out.println("Bravo !");
        } while (n != mystere);

        sc.close();
    }
}
```

🧠 **Explication**
Une boucle `do...while` est idéale car **on veut demander au moins une fois**.

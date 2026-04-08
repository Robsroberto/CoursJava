
## Solution java procédural exercice 


### Exercice1
```java
import java.util.Scanner;

public class SommeDeuxNombres {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez le premier nombre : ");
        int nombre1 = scanner.nextInt();

        System.out.print("Entrez le deuxième nombre : ");
        int nombre2 = scanner.nextInt();

        int somme = nombre1 + nombre2;
        System.out.println("La somme est : " + somme);

        scanner.close();
    }
}
```

### Exercice2
```java
import java.util.Scanner;

public class PariteNombre {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre : ");
        int nombre = scanner.nextInt();

        if (nombre % 2 == 0) {
            System.out.println("Le nombre est pair.");
        } else {
            System.out.println("Le nombre est impair.");
        }

        scanner.close();
    }
}
```

### Exercice 3

```java
import java.util.Scanner;

public class FactorielleNombre {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre : ");
        int nombre = scanner.nextInt();

        long factorielle = 1;

        for (int i = 1; i <= nombre; i++) {
            factorielle *= i;
        }

        System.out.println("La factorielle de " + nombre + " est : " + factorielle);

        scanner.close();
    }
}
```

### Exercice 4

```java
import java.util.Scanner;

public class NombrePremier {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre : ");
        int nombre = scanner.nextInt();

        boolean estPremier = true;

        for (int i = 2; i <= nombre / 2; i++) {
            if (nombre % i == 0) {
                estPremier = false;
                break;
            }
        }

        if (estPremier) {
            System.out.println("Le nombre est premier.");
        } else {
            System.out.println("Le nombre n'est pas premier.");
        }

        scanner.close();
    }
}
```

### Exercice 5
<!-- 
```java
import java.util.Scanner;

public class InversionNombre {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un nombre : ");
        int nombre = scanner.nextInt();

        int nombreInverse = 0;

        while (nombre != 0) {
            int chiffre = nombre % 10;
            nombreInverse = nombreInverse * 10 + chiffre;
            nombre /= 10;
        }

        System.out.println("Le nombre inversé est : " + nombreInverse);

        scanner.close();
    }
}
``` -->

```java
import java.util.Scanner;

public class Fibonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez le nombre de termes de la séquence de Fibonacci : ");
        int n = scanner.nextInt();

        int premierTerme = 0, deuxiemeTerme = 1;

        System.out.println("Séquence de Fibonacci :");

        for (int i = 1; i <= n; i++) {
            System.out.print(premierTerme + " ");

            int somme = premierTerme + deuxiemeTerme;
            premierTerme = deuxiemeTerme;
            deuxiemeTerme = somme;
        }

        scanner.close();
    }
}
```
### Exercice 6
```java
import java.util.Scanner;

public class Palindrome {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez un mot : ");
        String mot = scanner.nextLine();

        String motInverse = "";

        for (int i = mot.length() - 1; i >= 0; i--) {
            motInverse += mot.charAt(i);
        }

        if (mot.equalsIgnoreCase(motInverse)) {
            System.out.println("Le mot est un palindrome.");
        } else {
            System.out.println("Le mot n'est pas un palindrome.");
        }

        scanner.close();
    }
}
```

### Exercice 7
```java
import java.util.Scanner;

public class ConversionTemperature {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez une température : ");
        double temperature = scanner.nextDouble();

        System.out.print("Choisissez l'unité (C pour Celsius, F pour Fahrenheit) : ");
        char unite = scanner.next().charAt(0);

        double resultat;

        if (unite == 'C' || unite == 'c') {
            resultat = (temperature * 9/5) + 32;
            System.out.println("La température en Fahrenheit est : " + resultat);
        } else if (unite == 'F' || unite == 'f') {
            resultat = (temperature - 32) * 5/9;
            System.out.println("La température en Celsius est : " + resultat);
        } else {
            System.out.println("Unité non valide.");
        }

        scanner.close();
    }
}
```

### Exercice 8
### Solution 9:
```java
import java.util.Scanner;

public class CalculatriceSimple {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Entrez le premier nombre : ");
        double nombre1 = scanner.nextDouble();

        System.out.print("Entrez l'opérateur (+, -, *, /) : ");
        char operateur = scanner.next().charAt(0);

        System.out.print("Entrez le deuxième nombre : ");
        double nombre2 = scanner.nextDouble();

        double resultat;

        switch (operateur) {
            case '+':
                resultat = nombre1 + nombre2;
                break;
            case '-':
                resultat = nombre1 - nombre2;
                break;
            case '*':
                resultat = nombre1 * nombre2;
                break;
            case '/':
                resultat = nombre1 / nombre2;
                break;
            default:
                System.out.println("Opérateur non valide.");
                return;
        }

        System.out.println("Le résultat est : " + resultat);

        scanner.close();
    }
}
```

### Exercice 11

```java
public class CalculMoyenne {
    public static void main(String[] args) {
        int[] nombres = {75, 92, 88, 120, 61};
        double moyenne = calculerMoyenne(nombres);
        System.out.println("La moyenne est : " + moyenne);
    }

    public static double calculerMoyenne(int[] tableau) {
        int somme = 0;
        for (int nombre : tableau) {
            somme += nombre;
        }
        return (double) somme / tableau.length;
    }
}
```

### Exercice 12 

```java
public class RechercheBinaire {
    public static void main(String[] args) {
        int[] tableau = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};
        int elementRecherche = 7;
        int position = rechercheBinaire(tableau, elementRecherche);
        System.out.println("L'élément " + elementRecherche + " est à la position : " + position);
    }

    public static int rechercheBinaire(int[] tableau, int element) {
        int debut = 0;
        int fin = tableau.length - 1;

        while (debut <= fin) {
            int milieu = (debut + fin) / 2;

            if (tableau[milieu] == element)
                return milieu;
            else if (tableau[milieu] < element)
                debut = milieu + 1;
            else
                fin = milieu - 1;
        }

        return -1; // Élément non trouvé
    }
}
```

### Exercice 13 

```java
public class TriBulles {
    public static void main(String[] args) {
        int[] tableau = {5, 2, 9, 1, 5, 6};
        triBulles(tableau);
        System.out.println("Tableau trié : " + Arrays.toString(tableau));
    }

    public static void triBulles(int[] tableau) {
        int n = tableau.length;
        for (int i = 0; i < n-1; i++) {
            for (int j = 0; j < n-i-1; j++) {
                if (tableau[j] > tableau[j+1]) {
                    // Échange des éléments
                    int temp = tableau[j];
                    tableau[j] = tableau[j+1];
                    tableau[j+1] = temp;
                }
            }
        }
    }
}
```

### Exercice 14 


```java
public class CompteurVoyelles {
    public static void main(String[] args) {
        String phrase = "Programmation en Java";
        int nombreVoyelles = compterVoyelles(phrase);
        System.out.println("Le nombre de voyelles dans la phrase est : " + nombreVoyelles);
    }

    public static int compterVoyelles(String chaine) {
        int compteur = 0;
        chaine = chaine.toLowerCase(); // Pour traiter les majuscules et minuscules de la même manière

        for (int i = 0; i < chaine.length(); i++) {
            char caractere = chaine.charAt(i);
            if (caractere == 'a' || caractere == 'e' || caractere == 'i' || caractere == 'o' || caractere == 'u') {
                compteur++;
            }
        }

        return compteur;
    }
}
```

### Exercice 15
```java
import java.io.*;

public class CopieFichier {
    public static void main(String[] args) {
        copierFichier("source.txt", "destination.txt");
        System.out.println("Copie terminée avec succès.");
    }

    public static void copierFichier(String fichierSource, String fichierDestination) {
        try (BufferedReader lecteur = new BufferedReader(new FileReader(fichierSource));
             BufferedWriter ecrivain = new BufferedWriter(new FileWriter(fichierDestination))) {

            String ligne;
            while ((ligne = lecteur.readLine()) != null) {
                ecrivain.write(ligne);
                ecrivain.newLine();
            }

        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```

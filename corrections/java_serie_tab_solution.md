
## PARTIE I – TABLEAUX (1D)

### Exercice 1 – Lecture et affichage d’un tableau

```java
import java.util.Scanner;

public class Exo1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Donner la taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        System.out.println("Contenu du tableau :");
        for (int i = 0; i < n; i++) {
            System.out.println("T[" + i + "] = " + T[i]);
        }

        sc.close();
    }
}
```

Explication : on lit la taille, on crée un tableau de cette taille, on remplit avec une boucle, puis on affiche le contenu avec une autre boucle.

---

### Exercice 2 – Somme et moyenne d’un tableau

```java
import java.util.Scanner;

public class Exo2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        int somme = 0;
        for (int i = 0; i < n; i++) {
            somme += T[i];
        }
        double moyenne = (n > 0) ? (double) somme / n : 0;

        System.out.println("Somme = " + somme);
        System.out.println("Moyenne = " + moyenne);

        sc.close();
    }
}
```

Explication : on calcule la somme en parcourant le tableau, puis on divise par `n` pour la moyenne. On caste en `double` pour éviter la division entière.

---

### Exercice 3 – Recherche d’un élément

```java
import java.util.Scanner;

public class Exo3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        System.out.print("Valeur à rechercher : ");
        int val = sc.nextInt();

        int position = -1;
        for (int i = 0; i < n; i++) {
            if (T[i] == val) {
                position = i;
                break;
            }
        }

        if (position == -1)
            System.out.println("Valeur non trouvée.");
        else
            System.out.println("Valeur trouvée en position : " + position);

        sc.close();
    }
}
```

Explication : on parcourt le tableau, si on trouve la valeur on mémorise l’indice et on arrête la boucle. Si `position` reste à -1, on sait que la valeur n’existe pas.

---

### Exercice 4 – Max et min

```java
import java.util.Scanner;

public class Exo4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        if (n == 0) {
            System.out.println("Tableau vide.");
        } else {
            int max = T[0];
            int min = T[0];

            for (int i = 1; i < n; i++) {
                if (T[i] > max) max = T[i];
                if (T[i] < min) min = T[i];
            }

            System.out.println("Max = " + max);
            System.out.println("Min = " + min);
            System.out.println("Différence (max - min) = " + (max - min));
        }

        sc.close();
    }
}
```

Explication : on initialise max et min avec le premier élément, puis on compare les autres pour mettre à jour.

---

### Exercice 5 – Compter les occurrences

```java
import java.util.Scanner;

public class Exo5 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        System.out.print("Valeur à compter : ");
        int val = sc.nextInt();

        int cpt = 0;
        for (int i = 0; i < n; i++) {
            if (T[i] == val) cpt++;
        }

        System.out.println("Nombre d'occurrences de " + val + " = " + cpt);

        sc.close();
    }
}
```

Explication : on parcourt tout le tableau et on incrémente un compteur dès que la valeur cherchée apparaît.

---

### Exercice 6 – Inversion d’un tableau

```java
import java.util.Scanner;

public class Exo6 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        // inversion en place
        int i = 0, j = n - 1;
        while (i < j) {
            int tmp = T[i];
            T[i] = T[j];
            T[j] = tmp;
            i++;
            j--;
        }

        System.out.println("Tableau inversé :");
        for (int k = 0; k < n; k++) {
            System.out.println("T[" + k + "] = " + T[k]);
        }

        sc.close();
    }
}
```

Explication : on échange le premier avec le dernier, le deuxième avec l’avant-dernier, etc., jusqu’à ce que les indices se croisent.

---

### Exercice 7 – Séparer pairs et impairs

```java
import java.util.Scanner;

public class Exo7 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        System.out.println("Nombres pairs :");
        int cptPairs = 0, cptImpairs = 0;
        for (int i = 0; i < n; i++) {
            if (T[i] % 2 == 0) {
                System.out.print(T[i] + " ");
                cptPairs++;
            }
        }

        System.out.println("\nNombres impairs :");
        for (int i = 0; i < n; i++) {
            if (T[i] % 2 != 0) {
                System.out.print(T[i] + " ");
                cptImpairs++;
            }
        }

        System.out.println("\nNombre de pairs = " + cptPairs);
        System.out.println("Nombre d'impairs = " + cptImpairs);

        sc.close();
    }
}
```

Explication : on fait deux parcours (ou un seul avec deux actions), on teste la parité avec `% 2`.

---

### Exercice 8 – Fusion de deux tableaux

```java
import java.util.Scanner;

public class Exo8 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille des tableaux : ");
        int n = sc.nextInt();

        int[] A = new int[n];
        int[] B = new int[n];

        System.out.println("Saisie du tableau A :");
        for (int i = 0; i < n; i++) {
            System.out.print("A[" + i + "] = ");
            A[i] = sc.nextInt();
        }

        System.out.println("Saisie du tableau B :");
        for (int i = 0; i < n; i++) {
            System.out.print("B[" + i + "] = ");
            B[i] = sc.nextInt();
        }

        int[] C = new int[2 * n];
        for (int i = 0; i < n; i++) {
            C[i] = A[i];
        }
        for (int i = 0; i < n; i++) {
            C[n + i] = B[i];
        }

        System.out.println("Tableau fusionné C :");
        for (int i = 0; i < 2 * n; i++) {
            System.out.println("C[" + i + "] = " + C[i]);
        }

        sc.close();
    }
}
```

Explication : on recopie d’abord tous les éléments de A dans C, puis ceux de B à partir de l’indice `n`.

---

### Exercice 9 – Suppression d’un élément

```java
import java.util.Scanner;

public class Exo9 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        System.out.print("Valeur à supprimer : ");
        int val = sc.nextInt();

        int pos = -1;
        for (int i = 0; i < n; i++) {
            if (T[i] == val) {
                pos = i;
                break;
            }
        }

        if (pos == -1) {
            System.out.println("Valeur non trouvée, rien à supprimer.");
        } else {
            for (int i = pos; i < n - 1; i++) {
                T[i] = T[i + 1];
            }
            n--; // nouvelle taille logique

            System.out.println("Nouveau tableau :");
            for (int i = 0; i < n; i++) {
                System.out.println("T[" + i + "] = " + T[i]);
            }
        }

        sc.close();
    }
}
```

Explication : on cherche la première position de la valeur, puis on décale tous les éléments suivants vers la gauche et on réduit la taille logique de 1.

---

### Exercice 10 – Tri simple (croissant)

```java
import java.util.Scanner;

public class Exo10 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille du tableau : ");
        int n = sc.nextInt();
        int[] T = new int[n];

        for (int i = 0; i < n; i++) {
            System.out.print("T[" + i + "] = ");
            T[i] = sc.nextInt();
        }

        // tri par sélection (simple)
        for (int i = 0; i < n - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < n; j++) {
                if (T[j] < T[minIndex]) {
                    minIndex = j;
                }
            }
            int tmp = T[i];
            T[i] = T[minIndex];
            T[minIndex] = tmp;
        }

        System.out.println("Tableau trié :");
        for (int i = 0; i < n; i++) {
            System.out.println("T[" + i + "] = " + T[i]);
        }

        sc.close();
    }
}
```

Explication : on cherche à chaque étape le plus petit élément dans la partie non triée, puis on l’échange avec la position courante.

---

## PARTIE II – MATRICES (2D)

Pour les matrices, j’utilise des `int[][]` et des boucles imbriquées.

---

### Exercice 11 – Lecture d’une matrice

```java
import java.util.Scanner;

public class Exo11Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Nombre de lignes : ");
        int m = sc.nextInt();
        System.out.print("Nombre de colonnes : ");
        int n = sc.nextInt();

        int[][] M = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        System.out.println("Matrice saisie :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(M[i][j] + "\t");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

Explication : deux boucles pour saisir et deux boucles pour afficher, une pour les lignes, une pour les colonnes.

---

### Exercice 12 – Somme des éléments d’une matrice

```java
import java.util.Scanner;

public class Exo12Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("m = ");
        int m = sc.nextInt();
        System.out.print("n = ");
        int n = sc.nextInt();

        int[][] M = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        int somme = 0;
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                somme += M[i][j];
            }
        }

        System.out.println("Somme des éléments = " + somme);

        sc.close();
    }
}
```

Explication : même structure d’itération, mais on accumule tous les éléments dans une variable `somme`.

---

### Exercice 13 – Somme d’une ligne et d’une colonne

```java
import java.util.Scanner;

public class Exo13Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("m = ");
        int m = sc.nextInt();
        System.out.print("n = ");
        int n = sc.nextInt();

        int[][] M = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        System.out.print("Numéro de ligne (0 à " + (m - 1) + ") : ");
        int L = sc.nextInt();
        System.out.print("Numéro de colonne (0 à " + (n - 1) + ") : ");
        int C = sc.nextInt();

        int sommeL = 0;
        for (int j = 0; j < n; j++) {
            sommeL += M[L][j];
        }

        int sommeC = 0;
        for (int i = 0; i < m; i++) {
            sommeC += M[i][C];
        }

        System.out.println("Somme de la ligne " + L + " = " + sommeL);
        System.out.println("Somme de la colonne " + C + " = " + sommeC);

        sc.close();
    }
}
```

Explication : pour la ligne, on fixe `L` et on parcourt les colonnes ; pour la colonne, on fixe `C` et on parcourt les lignes.

---

### Exercice 14 – Diagonales d’une matrice carrée

```java
import java.util.Scanner;

public class Exo14Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille de la matrice carrée n = ");
        int n = sc.nextInt();

        int[][] M = new int[n][n];

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        int sommeDiagPrinc = 0;
        int sommeDiagSec = 0;

        System.out.println("Diagonale principale :");
        for (int i = 0; i < n; i++) {
            System.out.print(M[i][i] + " ");
            sommeDiagPrinc += M[i][i];
        }

        System.out.println("\nDiagonale secondaire :");
        for (int i = 0; i < n; i++) {
            int j = n - 1 - i;
            System.out.print(M[i][j] + " ");
            sommeDiagSec += M[i][j];
        }

        System.out.println("\nSomme diagonale principale = " + sommeDiagPrinc);
        System.out.println("Somme diagonale secondaire = " + sommeDiagSec);

        sc.close();
    }
}
```

Explication : sur la diagonale principale, les indices sont égaux (`i == j`). Sur la secondaire, `i + j = n - 1`, donc `j = n - 1 - i`.

---

### Exercice 15 – Transposée d’une matrice

```java
import java.util.Scanner;

public class Exo15Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("m = ");
        int m = sc.nextInt();
        System.out.print("n = ");
        int n = sc.nextInt();

        int[][] M = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        int[][] T = new int[n][m];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                T[j][i] = M[i][j];
            }
        }

        System.out.println("Transposée :");
        for (int i = 0; i < n; i++) {
            for (int j = 0; j < m; j++) {
                System.out.print(T[i][j] + "\t");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

Explication : la transposée échange les lignes et colonnes, donc l’élément `(i, j)` devient `(j, i)`.

---

### Exercice 16 – Produit par un scalaire

```java
import java.util.Scanner;

public class Exo16Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("m = ");
        int m = sc.nextInt();
        System.out.print("n = ");
        int n = sc.nextInt();

        int[][] M = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        System.out.print("Scalaire k = ");
        int k = sc.nextInt();

        System.out.println("Matrice après multiplication :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print((M[i][j] * k) + "\t");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

Explication : on ne change que la façon d’afficher, on multiplie chaque élément par `k` au moment de l’afficher (ou on peut modifier M si on veut).

---

### Exercice 17 – Addition de deux matrices

```java
import java.util.Scanner;

public class Exo17Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("m = ");
        int m = sc.nextInt();
        System.out.print("n = ");
        int n = sc.nextInt();

        int[][] A = new int[m][n];
        int[][] B = new int[m][n];

        System.out.println("Saisie de A :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("A[" + i + "][" + j + "] = ");
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("Saisie de B :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("B[" + i + "][" + j + "] = ");
                B[i][j] = sc.nextInt();
            }
        }

        int[][] C = new int[m][n];
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                C[i][j] = A[i][j] + B[i][j];
            }
        }

        System.out.println("Matrice C = A + B :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(C[i][j] + "\t");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

Explication : même dimension, on additionne élément par élément en position `(i, j)`.

---

### Exercice 18 – Produit matriciel A × B

```java
import java.util.Scanner;

public class Exo18Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Nombre de lignes de A : ");
        int m = sc.nextInt();
        System.out.print("Nombre de colonnes de A (et lignes de B) : ");
        int p = sc.nextInt();
        System.out.print("Nombre de colonnes de B : ");
        int n = sc.nextInt();

        int[][] A = new int[m][p];
        int[][] B = new int[p][n];

        System.out.println("Saisie de A :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < p; j++) {
                System.out.print("A[" + i + "][" + j + "] = ");
                A[i][j] = sc.nextInt();
            }
        }

        System.out.println("Saisie de B :");
        for (int i = 0; i < p; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("B[" + i + "][" + j + "] = ");
                B[i][j] = sc.nextInt();
            }
        }

        int[][] C = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                int somme = 0;
                for (int k = 0; k < p; k++) {
                    somme += A[i][k] * B[k][j];
                }
                C[i][j] = somme;
            }
        }

        System.out.println("Matrice C = A x B :");
        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print(C[i][j] + "\t");
            }
            System.out.println();
        }

        sc.close();
    }
}
```

Explication : le produit matriciel nécessite trois boucles : lignes de A, colonnes de B et somme sur k. C’est un bon exercice algorithmique.

---

### Exercice 19 – Matrice symétrique

```java
import java.util.Scanner;

public class Exo19Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Taille de la matrice carrée n = ");
        int n = sc.nextInt();

        int[][] M = new int[n][n];

        for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        boolean sym = true;
        for (int i = 0; i < n && sym; i++) {
            for (int j = 0; j < n; j++) {
                if (M[i][j] != M[j][i]) {
                    sym = false;
                    break;
                }
            }
        }

        if (sym)
            System.out.println("La matrice est symétrique.");
        else
            System.out.println("La matrice n'est pas symétrique.");

        sc.close();
    }
}
```

Explication : une matrice est symétrique si chaque élément `(i, j)` est égal à `(j, i)`. On teste cette propriété avec une double boucle.

---

### Exercice 20 – Comptage dans une matrice

```java
import java.util.Scanner;

public class Exo20Mat {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("m = ");
        int m = sc.nextInt();
        System.out.print("n = ");
        int n = sc.nextInt();

        int[][] M = new int[m][n];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                System.out.print("M[" + i + "][" + j + "] = ");
                M[i][j] = sc.nextInt();
            }
        }

        int pos = 0, neg = 0, nul = 0;
        int max = M[0][0];
        int min = M[0][0];

        for (int i = 0; i < m; i++) {
            for (int j = 0; j < n; j++) {
                int v = M[i][j];
                if (v > 0) pos++;
                else if (v < 0) neg++;
                else nul++;

                if (v > max) max = v;
                if (v < min) min = v;
            }
        }

        System.out.println("Nombre de positifs = " + pos);
        System.out.println("Nombre de négatifs = " + neg);
        System.out.println("Nombre de zéros = " + nul);
        System.out.println("Max = " + max);
        System.out.println("Min = " + min);

        sc.close();
    }
}
```

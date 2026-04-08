### 1. Création de Classes :

**Exercice :**
Créez une classe `Personne` avec des propriétés telles que le nom, le prénom et l'âge. Ajoutez une méthode pour afficher les détails de la personne.

**Solution :**
```java
public class Personne {
    private String nom;
    private String prenom;
    private int age;

    public Personne(String nom, String prenom, int age) {
        this.nom = nom;
        this.prenom = prenom;
        this.age = age;
    }

    public void afficherDetails() {
        System.out.println("Nom: " + nom + ", Prénom: " + prenom + ", Âge: " + age);
    }
}
```

### 2. Encapsulation :

**Exercice :**
Modifiez la classe `Personne` pour rendre ses propriétés privées et utilisez des méthodes d'accès (getters et setters) pour y accéder depuis l'extérieur de la classe.

**Solution :**
```java
public class Personne {
    private String nom;
    private String prenom;
    private int age;

    public Personne(String nom, String prenom, int age) {
        this.nom = nom;
        this.prenom = prenom;
        this.age = age;
    }

    public String getNom() {
        return nom;
    }

    public void setNom(String nom) {
        this.nom = nom;
    }

    public String getPrenom() {
        return prenom;
    }

    public void setPrenom(String prenom) {
        this.prenom = prenom;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public void afficherDetails() {
        System.out.println("Nom: " + nom + ", Prénom: " + prenom + ", Âge: " + age);
    }
}
```

### 3. Héritage :

**Exercice :**
Créez une classe `Etudiant` qui hérite de la classe `Personne` et ajoutez une propriété spécifique telle que la spécialité.

**Solution :**
```java
public class Etudiant extends Personne {
    private String specialite;

    public Etudiant(String nom, String prenom, int age, String specialite) {
        super(nom, prenom, age);
        this.specialite = specialite;
    }

    public String getSpecialite() {
        return specialite;
    }

    public void setSpecialite(String specialite) {
        this.specialite = specialite;
    }

    @Override
    public void afficherDetails() {
        super.afficherDetails();
        System.out.println("Spécialité: " + specialite);
    }
}
```

### 4. Polymorphisme :

**Exercice :**
Créez une interface `Calculable` avec une méthode `calculer()`. Implémentez cette interface dans les classes `Addition` et `Multiplication`. Appelez la méthode `calculer()` sur des objets de type `Calculable` sans connaître leur type réel.

**Solution :**
```java
public interface Calculable {
    int calculer();
}

public class Addition implements Calculable {
    private int a;
    private int b;

    public Addition(int a, int b) {
        this.a = a;
        this.b = b;
    }

    @Override
    public int calculer() {
        return a + b;
    }
}

public class Multiplication implements Calculable {
    private int a;
    private int b;

    public Multiplication(int a, int b) {
        this.a = a;
        this.b = b;
    }

    @Override
    public int calculer() {
        return a * b;
    }
}
```

### Explications :

1. **Classes et Objets :**
   - *Explication :* En Java, une classe est un modèle pour créer des objets. Les objets sont des instances de classes. Une classe définit les propriétés (champs) et les comportements (méthodes) des objets.
   
2. **Encapsulation :**
   - *Explication :* L'encapsulation consiste à regrouper les données (champs) et les méthodes qui manipulent ces données dans une unité, c'est-à-dire une classe. L'accès aux données se fait via des méthodes d'accès (getters et setters).
   
3. **Héritage :**
   - *Explication :* L'héritage permet à une classe (sous-classe) d'utiliser les propriétés et les comportements d'une autre classe (super-classe). Cela favorise la réutilisation du code et l'établissement de hiérarchies de classes.
   
4. **Polymorphisme :**
   - *Explication :* Le polymorphisme permet à des objets d'être traités comme des objets de leur classe de base plutôt que comme des objets de leur type réel. Cela se réalise à travers l'héritage et l'implémentation d'interfaces.

### Exercices :

1. **Création de Classes :**
   - Créez une classe `Vehicule` avec des propriétés telles que la marque, le modèle et l'année de fabrication. Ajoutez une méthode pour afficher les détails du véhicule.

2. **Encapsulation :**
   - Modifiez la classe `Vehicule` pour rendre ses propriétés privées et utilisez des méthodes d'accès (getters et setters) pour y accéder depuis l'extérieur de la classe.

3. **Héritage :**
   - Créez une classe `Voiture` qui hérite de la classe `Vehicule`. Ajoutez des propriétés spécifiques à une voiture, comme le nombre de portes. Surchargez la méthode d'affichage pour inclure les détails spécifiques à une voiture.

4. **Polymorphisme :**
   - Créez une interface `Mouvement` avec une méthode `deplacer()`. Implémentez cette interface dans les classes `Vehicule` et `Voiture`. Appelez la méthode `deplacer()` sur des objets de type `Mouvement` sans connaître leur type réel.

5. **Abstraction :**
   - Créez une classe abstraite `Forme` avec une méthode abstraite `calculerSurface()`. Implémentez cette classe dans des classes concrètes telles que `Cercle` et `Rectangle`. Appelez la méthode `calculerSurface()` sur des objets de type `Forme` sans connaître leur type réel.

6. **Composition :**
   - Créez une classe `Moteur` avec une méthode `demarrer()`. Ajoutez une propriété de type `Moteur` à la classe `Voiture` pour représenter le moteur de la voiture. Appelez la méthode `demarrer()` sur une voiture pour démarrer son moteur.

7. **Surcharge de Méthode :**
   - Ajoutez une méthode `afficherDetails(String couleur)` à la classe `Voiture` qui surcharge la méthode d'affichage. Utilisez cette nouvelle méthode pour afficher les détails d'une voiture avec sa couleur.

8. **Utilisation de Super :**
   - Dans la classe `Voiture`, utilisez le mot-clé `super` pour appeler la méthode d'affichage de la classe `Vehicule` tout en ajoutant des informations spécifiques à une voiture.

Bien sûr, voici les solutions et explications pour chacun des exercices proposés :

### 1. Création de Classes :

```java
public class Vehicule {
    private String marque;
    private String modele;
    private int anneeFabrication;

    public Vehicule(String marque, String modele, int anneeFabrication) {
        this.marque = marque;
        this.modele = modele;
        this.anneeFabrication = anneeFabrication;
    }

    public void afficherDetails() {
        System.out.println("Marque: " + marque + ", Modèle: " + modele + ", Année de fabrication: " + anneeFabrication);
    }
}
```

**Explication :** La classe `Vehicule` a trois propriétés (marque, modèle, année de fabrication) et un constructeur pour initialiser ces propriétés. La méthode `afficherDetails()` permet d'afficher les détails du véhicule.

### 2. Encapsulation :

```java
public class Vehicule {
    private String marque;
    private String modele;
    private int anneeFabrication;

    public Vehicule(String marque, String modele, int anneeFabrication) {
        this.marque = marque;
        this.modele = modele;
        this.anneeFabrication = anneeFabrication;
    }

    public String getMarque() {
        return marque;
    }

    public void setMarque(String marque) {
        this.marque = marque;
    }

    public String getModele() {
        return modele;
    }

    public void setModele(String modele) {
        this.modele = modele;
    }

    public int getAnneeFabrication() {
        return anneeFabrication;
    }

    public void setAnneeFabrication(int anneeFabrication) {
        this.anneeFabrication = anneeFabrication;
    }

    public void afficherDetails() {
        System.out.println("Marque: " + marque + ", Modèle: " + modele + ", Année de fabrication: " + anneeFabrication);
    }
}
```

**Explication :** Les propriétés de la classe `Vehicule` sont maintenant privées, et des méthodes d'accès (getters et setters) sont utilisées pour y accéder depuis l'extérieur de la classe.

### 3. Héritage :

```java
public class Voiture extends Vehicule {
    private int nombrePortes;

    public Voiture(String marque, String modele, int anneeFabrication, int nombrePortes) {
        super(marque, modele, anneeFabrication);
        this.nombrePortes = nombrePortes;
    }

    @Override
    public void afficherDetails() {
        super.afficherDetails();
        System.out.println("Nombre de portes: " + nombrePortes);
    }
}
```

**Explication :** La classe `Voiture` hérite de la classe `Vehicule` et ajoute une propriété spécifique (`nombrePortes`). La méthode `afficherDetails()` est surchargée pour inclure les détails spécifiques à une voiture.

### 4. Polymorphisme :

```java
public interface Mouvement {
    void deplacer();
}

public class Vehicule implements Mouvement {
    // ... autres propriétés et méthodes

    @Override
    public void deplacer() {
        System.out.println("Le véhicule se déplace.");
    }
}

public class Voiture extends Vehicule {
    // ... autres propriétés et méthodes

    @Override
    public void deplacer() {
        System.out.println("La voiture se déplace.");
    }
}
```

**Explication :** L'interface `Mouvement` est implémentée dans les classes `Vehicule` et `Voiture`. Vous pouvez maintenant appeler la méthode `deplacer()` sur des objets de type `Mouvement` sans connaître leur type réel.

### 5. Abstraction :

```java
public abstract class Forme {
    public abstract double calculerSurface();
}

public class Cercle extends Forme {
    private double rayon;

    public Cercle(double rayon) {
        this.rayon = rayon;
    }

    @Override
    public double calculerSurface() {
        return Math.PI * Math.pow(rayon, 2);
    }
}

public class Rectangle extends Forme {
    private double longueur;
    private double largeur;

    public Rectangle(double longueur, double largeur) {
        this.longueur = longueur;
        this.largeur = largeur;
    }

    @Override
    public double calculerSurface() {
        return longueur * largeur;
    }
}
```

**Explication :** La classe `Forme` est abstraite avec une méthode abstraite `calculerSurface()`. Les classes concrètes `Cercle` et `Rectangle` implémentent cette méthode.

### 6. Composition :

```java
public class Moteur {
    public void demarrer() {
        System.out.println("Le moteur démarre.");
    }
}

public class Voiture extends Vehicule {
    private Moteur moteur;

    public Voiture(String marque, String modele, int anneeFabrication, int nombrePortes) {
        super(marque, modele, anneeFabrication);
        this.moteur = new Moteur();
    }

    public void demarrerVoiture() {
        moteur.demarrer();
    }
}
```

**Explication :** La classe `Voiture` utilise la composition en ayant une propriété de type `Moteur`. La méthode `demarrerVoiture()` utilise le moteur pour démarrer la voiture.

### 7. Surcharge de Méthode :

```java
public class Voiture extends Vehicule {
    private int nombrePortes;
    private String couleur;

    public Voiture(String marque, String modele, int anneeFabrication, int nombrePortes, String couleur) {
        super(marque, modele, anneeFabric

ation);
        this.nombrePortes = nombrePortes;
        this.couleur = couleur;
    }

    @Override
    public void afficherDetails() {
        super.afficherDetails();
        System.out.println("Nombre de portes: " + nombrePortes);
        System.out.println("Couleur: " + couleur);
    }

    public void afficherDetails(String couleur) {
        System.out.println("Nombre de portes: " + nombrePortes);
        System.out.println("Couleur: " + couleur);
    }
}
```

**Explication :** Une méthode `afficherDetails()` est surchargée pour prendre en compte la couleur. L'utilisation de `super` est illustrée pour appeler la méthode d'affichage de la classe `Vehicule`.

### 8. Utilisation de Super :

```java
public class Voiture extends Vehicule {
    private int nombrePortes;

    public Voiture(String marque, String modele, int anneeFabrication, int nombrePortes) {
        super(marque, modele, anneeFabrication);
        this.nombrePortes = nombrePortes;
    }

    @Override
    public void afficherDetails() {
        super.afficherDetails();
        System.out.println("Nombre de portes: " + nombrePortes);
    }

    public void afficherDetailsAvecMarque() {
        System.out.println("Marque: " + super.getMarque());
        afficherDetails();
    }
}
```

**Explication :** La méthode `afficherDetailsAvecMarque()` utilise le mot-clé `super` pour appeler la méthode `getMarque()` de la classe `Vehicule` tout en ajoutant les détails spécifiques à une voiture.


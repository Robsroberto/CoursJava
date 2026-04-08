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

# Chapitre 1 : Introduction à Java et Installation de l’Environnement
---
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 

## Par Robert DIASSÉ &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
 <img src="java.webp" alt="ISI" width="50px">

---

## 1.1 Présentation du langage Java

Java est un langage de programmation :

* **Orienté objet** (même si dans ce cours nous commençons en mode procédural).
* **Portable** : un programme écrit en Java peut s’exécuter sur n’importe quelle machine équipée de la JVM (Java Virtual Machine).
* **Sécurisé et robuste** : utilisé dans des applications critiques (banques, télécoms, mobile).
* **Très répandu** : présent dans le développement mobile (Android), desktop, web et big data.

Java est compilé en **bytecode** que la JVM interprète.
Ainsi, il est indépendant du système d’exploitation (Windows, Linux, MacOS).

---

## 1.2 Installation et configuration de l’environnement

### Étapes d’installation

1. **Installer le JDK (Java Development Kit)**

   * Télécharger la dernière version du JDK depuis : [https://www.oracle.com/java/technologies/javase-downloads.html](https://www.oracle.com/java/technologies/javase-downloads.html)
   * Vérifier l’installation :

     ```bash
     java -version
     javac -version
     ```

     Si les commandes affichent la version, Java est correctement installé.

2. **Choisir un éditeur de code**

   * **Terminal (classique)** : pour exécuter directement.
   * **IntelliJ IDEA** : IDE puissant recommandé pour le développement.
   * **Visual Studio Code (VS Code)** : plus léger, nécessite l’extension Java.

---

## 1.3 Premier programme Java : Hello World

Voici un premier programme simple :

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Bonjour, bienvenue en Java !");
    }
}
```

### Explications

* `public class HelloWorld { ... }` : définit une classe publique appelée `HelloWorld`.
* `public static void main(String[] args)` : point d’entrée du programme, c’est la première méthode exécutée.
* `System.out.println("...");` : affiche du texte dans la console.

---

## 1.4 Exécution du programme

### Méthode 1 : Exécution via le Terminal

1. Créer un fichier `HelloWorld.java`.
2. Compiler avec :

   ```bash
   javac HelloWorld.java
   ```

   Cela génère un fichier `HelloWorld.class`.
3. Exécuter avec :

   ```bash
   java HelloWorld
   ```

   **Sortie attendue :**

   ```
   Bonjour, bienvenue en Java !
   ```

---

### Méthode 2 : Exécution avec IntelliJ IDEA

1. Créer un nouveau projet Java.
2. Ajouter un fichier `HelloWorld.java` avec le code ci-dessus.
3. Clic droit → `Run HelloWorld.main()`.
4. La sortie s’affiche dans la console intégrée.

**Sortie attendue :**

```
Bonjour, bienvenue en Java !
```

---

### Méthode 3 : Exécution avec VS Code

1. Installer l’extension **Extension Pack for Java**.
2. Créer un fichier `HelloWorld.java`.
3. Cliquer sur le bouton **Run** en haut à droite ou utiliser :

   ```
   Ctrl + F5
   ```
4. La sortie s’affiche dans le terminal intégré.

**Sortie attendue :**

```
Bonjour, bienvenue en Java !
```

---

## 1.5 Un autre exemple : Calcul simple

```java
public class Addition {
    public static void main(String[] args) {
        int a = 5;
        int b = 7;
        int somme = a + b;
        System.out.println("La somme est : " + somme);
    }
}
```

### Explications

* On déclare deux entiers `a` et `b`.
* On calcule leur somme dans une nouvelle variable `somme`.
* On affiche le résultat avec `System.out.println`.

**Sortie attendue :**

```
La somme est : 12
```

---

## 1.6 Points clés du chapitre

* Java est un langage portable grâce à la JVM.
* Le JDK est nécessaire pour compiler et exécuter.
* Un programme Java commence toujours par une classe et une méthode `main`.
* Trois façons d’exécuter un programme : Terminal, IntelliJ IDEA, VS Code.

---


1. **Programmation Orientée Objet (POO) :**
   ```java
   class Personne {
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

       public int anneeDeNaissance() {
           return 2023 - age;
       }
   }

   class Employe extends Personne {
       private double salaire;
       private String poste;

       public Employe(String nom, String prenom, int age, double salaire, String poste) {
           super(nom, prenom, age);
           this.salaire = salaire;
           this.poste = poste;
       }
   }
   ```

2. **Collections :**
   ```java
   import java.util.ArrayList;
   import java.util.List;

   public class ToDoList {
       private List<String> tasks;

       public ToDoList() {
           this.tasks = new ArrayList<>();
       }

       public void addTask(String task) {
           tasks.add(task);
       }

       public void removeTask(String task) {
           tasks.remove(task);
       }

       public void displayTasks() {
           for (String task : tasks) {
               System.out.println(task);
           }
       }
   }
   ```

3. **Manipulation des Chaînes de Caractères :**
   ```java
   import java.util.Scanner;

   public class StringUtil {
       public static void main(String[] args) {
           Scanner scanner = new Scanner(System.in);
           System.out.print("Entrez une phrase : ");
           String phrase = scanner.nextLine();

           // Compter le nombre de mots
           String[] mots = phrase.split("\\s+");
           System.out.println("Nombre de mots : " + mots.length);

           // Inverser un mot
           System.out.print("Entrez un mot : ");
           String mot = scanner.next();
           String motInverse = new StringBuilder(mot).reverse().toString();
           System.out.println("Mot inversé : " + motInverse);
       }
   }
   ```

4. **Gestion de la Mémoire et Exceptions :**
   ```java
   import java.io.IOException;

   public class DatabaseConnection {
       public static void main(String[] args) {
           try (DatabaseConnection dbConnection = new DatabaseConnection()) {
               dbConnection.connect();
           } catch (ConnectionException e) {
               e.printStackTrace();
           }
       }

       public void connect() throws ConnectionException {
           // Simuler une connexion à la base de données
           System.out.println("Connexion réussie");
           // Simuler une exception pour illustrer la gestion des erreurs
           throw new ConnectionException("Erreur de connexion");
       }
   }

   class ConnectionException extends IOException {
       public ConnectionException(String message) {
           super(message);
       }
   }
   ```

5. **Entrées/Sorties (E/S) :**
   ```java
   import java.io.BufferedReader;
   import java.io.FileReader;
   import java.io.FileWriter;
   import java.io.IOException;

   public class FileCopy {
       public static void main(String[] args) {
           try (BufferedReader reader = new BufferedReader(new FileReader("source.txt"));
                FileWriter writer = new FileWriter("destination.txt")) {

               String line = reader.readLine();
               while (line != null) {
                   writer.write(line + "\n");
                   line = reader.readLine();
               }

               System.out.println("Copie terminée.");
           } catch (IOException e) {
               e.printStackTrace();
           }
       }
   }
   ```

6. **Threads et Multithreading :**
   ```java
   public class ThreadExample {
       public static void main(String[] args) {
           Thread thread1 = new Thread(() -> {
               for (int i = 0; i < 5; i++) {
                   System.out.println("Thread 1: " + i);
               }
           });

           Thread thread2 = new Thread(() -> {
               for (int i = 0; i < 5; i++) {
                   System.out.println("Thread 2: " + i);
               }
           });

           thread1.start();
           thread2.start();
       }
   }
   ```

7. **Collections avancées et Streams :**
   ```java
   import java.util.List;
   import java.util.stream.Collectors;

   public class Product {
       private String name;
       private double price;

       public Product(String name, double price) {
           this.name = name;
           this.price = price;
       }

       public static void main(String[] args) {
           List<Product> products = List.of(
                   new Product("Laptop", 1200.0),
                   new Product("Phone", 800.0),
                   new Product("Tablet", 400.0)
           );

           // Filtrer les produits dont le prix est supérieur à 1000
           List<Product> expensiveProducts = products.stream()
                   .filter(product -> product.getPrice() > 1000)
                   .collect(Collectors.toList());

           // Afficher les noms des produits filtrés
           expensiveProducts.forEach(product -> System.out.println(product.getName()));
       }

       public String getName() {
           return name;
       }

       public double getPrice() {
           return price;
       }
   }
   ```

8. **Manipulation des Dates et Heures :**
   ```java
   import java.time.LocalDate;
   import java.time.Period;

   public class DateExample {
       public static void main(String[] args) {
           LocalDate today = LocalDate.now();
           LocalDate birthdate = LocalDate.of(1990, 1, 1);

           // Calcul de la différence en jours entre aujourd'hui et la date de naissance
           long daysDifference = Period.between(birthdate, today).getDays();
           System.out.println("Différence en jours : " + daysDifference);
       }
   }
   ```

9. **Programmation Réseau :**
   ```java
   import java.io.IOException;
   import java.io.PrintWriter;
   import java.net.ServerSocket;
   import java.net.Socket;
   import java.util.Scanner;

   public class SimpleServer {
       public static void main(String[] args) {
           try (ServerSocket serverSocket = new ServerSocket(8080)) {
               System.out.println("Attente de connexion...");
               Socket clientSocket = serverSocket.accept();
               System.out.println("Connexion établie.");

               // Flux de sortie vers le client
               PrintWriter out = new PrintWriter(clientSocket.getOutputStream(), true);
               out.println("Bienvenue sur le serveur!");

               // Flux d'entrée depuis le client
               Scanner scanner = new Scanner(clientSocket.getInputStream());
               String clientMessage = scanner.nextLine();
               System.out.println("Message du client : " + clientMessage);

           } catch (IOException e) {
               e.printStackTrace();
           }
       }
   }
   ```

10. **Spring Boot (Bonus)
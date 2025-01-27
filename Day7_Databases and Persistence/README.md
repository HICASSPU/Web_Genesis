# Web Genesis: Day 7 - Databases and Persistence

**Welcome back to Web Genesis!** Today we delve into the world of databases, a crucial component of any robust backend application. We'll explore how to interact with databases using Spring Boot and learn about Object-Relational Mapping (ORM) with JPA and Hibernate.

**1. Introduction to SQL and Relational Databases**

* **Relational Databases:** 
    * Understand the concept of relational databases, where data is organized into tables with rows and columns.
    * Learn about key concepts like tables, columns, rows, primary keys, foreign keys, and relationships between tables.

* **SQL (Structured Query Language):**
    * Learn the basics of SQL, the standard language for interacting with relational databases. 
    * Explore common SQL commands:
        * **`SELECT`:** Retrieve data from one or more tables.
        * **`INSERT`:** Insert new data into a table.
        * **`UPDATE`:** Modify existing data in a table.
        * **`DELETE`:** Remove data from a table.
        * **`CREATE TABLE`:** Create a new table in the database.
        * **`ALTER TABLE`:** Modify the structure of a table (e.g., add or remove columns).

    * **Example:**

      ```sql
      -- Select all columns from the 'users' table
      SELECT * FROM users;

      -- Insert a new user
      INSERT INTO users (name, email) VALUES ('John Doe', '[email address removed]'); 
      ```

**2. Integrating MySQL with Spring Boot**

* **Setting up MySQL:** 
    * Learn how to install and configure MySQL, a popular open-source relational database.
    * Create a database and user for your Spring Boot application.

* **Spring Data JPA:** 
    * Explore Spring Data JPA, a powerful abstraction layer that simplifies database interactions.
    * Learn how to create JPA entities (Java objects that represent database tables) using annotations like `@Entity`, `@Id`, `@GeneratedValue`, `@Column`, etc.

    * **Example (User Entity):**

      ```java
      @Entity
      public class User {

          @Id
          @GeneratedValue(strategy = GenerationType.IDENTITY)
          private Long id;

          @Column(nullable = false)
          private String name;

          @Column(nullable = false, unique = true)
          private String email;

          // Getters and Setters (omitted for brevity)
      }
      ```

* **Spring Data JPA Repositories:** 
    * Learn how to create JPA repositories to interact with your database entities.
    * Utilize Spring Data JPA's built-in methods (e.g., `findAll()`, `findById()`, `save()`) to perform CRUD operations.

    * **Example (UserRepository):**

      ```java
      public interface UserRepository extends JpaRepository<User, Long> {
          // Custom query methods (optional)
          // e.g., findUserByEmail(String email); 
      }
      ```

**3. Object-Relational Mapping (ORM) with Hibernate**

* **ORM Overview:** 
    * Understand the concept of Object-Relational Mapping (ORM), which allows you to work with objects in your Java code instead of directly interacting with database tables.
    * Learn how Hibernate, the default ORM implementation in Spring Boot, maps Java objects to database tables.

* **Key Hibernate Concepts:** 
    * Explore key Hibernate concepts like sessions, transactions, and lazy loading.

**Mini-Project: Build a Backend Service for Managing User Data**

Today's challenge: Build a simple backend service for managing user data using Spring Boot, JPA, and an in-memory or external database.

* **Features:**
    * Create a `User` entity with fields like `id`, `name`, `email`, `password`.
    * Implement endpoints for:
        * Creating new users (POST)
        * Retrieving a list of users (GET)
        * Retrieving a specific user by ID (GET)
        * Updating user information (PUT)
        * Deleting a user (DELETE)
    * Consider implementing basic user authentication (e.g., username/password).

* **Technical Requirements:**
    * Use Spring Boot, JPA, and Hibernate to interact with the database.
    * Implement RESTful endpoints using Spring MVC.
    * Test your API using tools like Postman or cURL.

**Resources:**

* **Spring Boot Documentation:** [https://spring.io/projects/spring-boot/](https://spring.io/projects/spring-boot/) - Official documentation for Spring Boot.
* **Spring Data JPA Documentation:** [https://docs.spring.io/spring-data/jpa/docs/current/reference/html/](https://docs.spring.io/spring-data/jpa/docs/current/reference/html/index.html) - Official documentation for Spring Data JPA.
* **Hibernate Documentation:** [https://hibernate.org/](https://hibernate.org/) - Official documentation for Hibernate.

**Let's get coding!**

This enhanced README provides a comprehensive guide for Day 7 of Web Genesis, covering key database and persistence concepts with code examples and detailed explanations. Remember to refer to the official documentation, experiment with the code examples, and build your own Spring Boot applications to solidify your understanding.

**Bonus Tip:** Explore advanced JPA features like custom queries, projections, and caching to optimize your database interactions.


## *Created by:*

*Atharva Wakodikar*

---

## *Contributing*

Feel free to contribute by suggesting edits, adding more resources, or sharing your learning experiences.
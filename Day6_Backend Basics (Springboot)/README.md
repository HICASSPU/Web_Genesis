# Web Genesis: Day 6 - Backend Basics (Spring Boot)

**Welcome back to Web Genesis!** Today we'll embark on a journey into the world of backend development, starting with the powerful Spring Boot framework.

**1. Introduction to Backend Development and REST APIs**

* **Backend Development:** 
    * The backend is the "brains" of a web application, responsible for handling data, business logic, and server-side operations. It acts as the invisible engine behind the scenes, powering the user interface and ensuring seamless data flow. 
    * Key responsibilities include:
        * **Data Storage and Retrieval:** Interacting with databases (like relational databases, NoSQL databases, or cloud-based data stores) to store, retrieve, and manage application data.
        * **Business Logic Implementation:** Handling complex calculations, data validation, and decision-making processes within the application.
        * **User Authentication and Authorization:** Implementing secure user login, session management, and access control mechanisms to protect sensitive data and resources.
        * **Server-Side Operations:** Managing server resources, handling requests from clients, and ensuring the smooth functioning of the application.

* **REST APIs:** 
    * Representational State Transfer (REST) is a widely adopted architectural style for designing web services. It provides a standardized way for different software applications to communicate with each other over the internet. 
    * RESTful APIs use standard HTTP methods (GET, POST, PUT, DELETE) to interact with resources (e.g., users, products, orders). 
    * Key characteristics of REST APIs:
        * **Statelessness:** Each request from a client must contain all the necessary information for the server to understand and process it. 
        * **Client-Server Architecture:** Clear separation of concerns between the client (e.g., web browser, mobile app) and the server.
        * **Cacheability:** Responses from the server can be cached by clients or intermediate servers to improve performance and reduce server load.
        * **Uniform Interface:** REST APIs adhere to a uniform interface, making them easier to understand and use.

**2. Setting Up a Spring Boot Application**

* **Spring Boot Overview:** 
    * Spring Boot is a powerful Java framework that simplifies the development of Spring-based applications. 
    * It provides a streamlined setup process, auto-configuration, and a convention-over-configuration approach, reducing the amount of boilerplate code and allowing developers to focus on core application logic.
    * Key features include:
        * **Auto-configuration:** Spring Boot automatically configures many aspects of your application based on the dependencies you include, eliminating the need for extensive manual configuration.
        * **Embedded Server:** Easily embed a web server like Tomcat or Jetty within your application, making deployment simpler.
        * **Dependency Injection:** Simplifies managing dependencies between different parts of your application, making your code more modular and maintainable.

* **Creating a Spring Boot Project:** 
    * Learn how to create a new Spring Boot project using tools like Spring Initializr (a web-based tool that helps you generate a project with the necessary dependencies and configurations).
    * Understand the basic project structure, including the `src/main/java` and `src/test/java` directories, and the role of key files like `pom.xml` (Project Object Model) and `Application.java`.
    * Explore the role of key annotations like `@SpringBootApplication`, `@RestController`, and `@RequestMapping`, which are used to define the structure and behavior of your Spring Boot application.

**3. CRUD Operations with Spring Boot and H2**

* **CRUD Operations:** 
    * Learn about the fundamental CRUD operations:
        * **Create:** Create new records in the database (e.g., create a new user account).
        * **Read:** Retrieve existing records from the database (e.g., get a list of users, get a specific user by ID).
        * **Update:** Modify existing records in the database (e.g., update user information).
        * **Delete:** Remove records from the database (e.g., delete a user account).

* **In-Memory Database (H2):** 
    * Learn about in-memory databases like H2, which are lightweight and ideal for development and testing purposes. 
    * Explore how to integrate H2 Database with your Spring Boot application.

* **Building a REST API:** 
    * Learn how to create RESTful endpoints using Spring Boot's `@RestController` and `@RequestMapping` annotations. 
    * Implement methods for handling HTTP requests:
        * **`@GetMapping`:** Handle GET requests (e.g., retrieve a list of tasks, get a single task by ID).

          ```java
          @GetMapping("/tasks")
          public List<Task> getAllTasks() { 
              return taskService.getAllTasks(); 
          }

          @GetMapping("/tasks/{id}")
          public Task getTaskById(@PathVariable Long id) { 
              return taskService.getTaskById(id); 
          }
          ```

        * **`@PostMapping`:** Handle POST requests (e.g., create a new task).

          ```java
          @PostMapping("/tasks")
          public Task createTask(@RequestBody Task task) { 
              return taskService.createTask(task); 
          }
          ```

        * **`@PutMapping`:** Handle PUT requests (e.g., update an existing task).

          ```java
          @PutMapping("/tasks/{id}")
          public Task updateTask(@PathVariable Long id, @RequestBody Task task) { 
              return taskService.updateTask(id, task); 
          }
          ```

        * **`@DeleteMapping`:** Handle DELETE requests (e.g., delete a task).

          ```java
          @DeleteMapping("/tasks/{id}")
          public void deleteTask(@PathVariable Long id) { 
              taskService.deleteTask(id); 
          }
          ```

    * Learn how to handle request parameters, create and return JSON responses, and handle HTTP status codes (e.g., 200 OK, 404 Not Found, 500 Internal Server Error) to provide meaningful feedback to the client.

**Mini-Project: Create a Basic REST API for Managing Tasks**

Today's challenge: Build a simple REST API for managing tasks using Spring Boot.

* **Features:**
    * Create a `Task` entity (e.g., with fields like `id`, `title`, `description`, `status`, `dueDate`).
    * Implement endpoints for:
        * Creating new tasks (POST)
        * Retrieving a list of tasks (GET)
        * Retrieving a single task by ID (GET)
        * Updating an existing task (PUT)
        * Deleting a task (DELETE)

* **Technical Requirements:**
    * Use Spring Boot and JPA (Java Persistence API) to interact with the database.
    * Utilize Spring MVC for handling HTTP requests and responses.
    * Test your API using tools like Postman or cURL to verify that it is functioning as expected.

**Resources:**

* **Spring Boot Documentation:** [https://spring.io/projects/spring-boot/](https://spring.io/projects/spring-boot/) - Official documentation for Spring Boot.
* **Spring Framework Documentation:** [https://spring.io/](https://spring.io/) - Comprehensive documentation for the Spring Framework.
* **H2 Database Documentation:** [https://www.h2database.com/](https://www.h2database.com/) - Documentation for the H2 in-memory database.

**Let's get coding!**

This enhanced README provides a more comprehensive overview of backend development with Spring Boot, covering key concepts, best practices, and code examples. Remember to refer to the official documentation, experiment with the code examples, and build your own Spring Boot applications to solidify your understanding.

**Bonus Tip:** Explore advanced Spring Boot features like security (using Spring Security), caching, asynchronous processing, and cloud integration to further enhance your backend development skills.


## *Created by:*

*Atharva Wakodikar*

---

## *Contributing*

Feel free to contribute by suggesting edits, adding more resources, or sharing your learning experiences.
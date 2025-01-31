# Web Genesis: Day 8 - Authentication and Security

**Welcome back to Web Genesis!** Today we delve into the critical aspects of building secure and reliable backend applications: authentication and authorization.

**1. Authentication with Spring Security and JWT**

* **Authentication:** Understand the core concepts of authentication, the process of verifying a user's identity. 
* **Spring Security:** Learn how to integrate Spring Security into your Spring Boot application to handle user authentication. Spring Security is a powerful and flexible framework that provides a comprehensive set of features for securing your application.
* **JSON Web Tokens (JWT):** Explore JWT, a standard for creating secure and compact JSON-based tokens that represent user claims (e.g., username, roles, permissions). JWTs are a popular choice for authentication in modern applications due to their stateless nature and ease of use.
* **Implementing JWT Authentication:** 
    * **Generate and issue JWTs:**
        * After successful user login (e.g., username/password), generate a JWT containing user information (e.g., username, user ID, roles).
        * Include the JWT in the response (e.g., in the `Authorization` header) to the client.

    * **Example (Simplified):**

      ```java
      @RestController
      @RequestMapping("/api/auth")
      public class AuthController {

          @PostMapping("/login")
          public ResponseEntity<?> login(@RequestBody LoginRequest loginRequest) {
              // Authenticate user (e.g., check credentials against database) 
              // ...
              if (authenticationSuccessful) {
                  String jwt = jwtTokenProvider.generateToken(user); 
                  return ResponseEntity.ok(new AuthResponse(jwt)); 
              } else {
                  return ResponseEntity.status(HttpStatus.UNAUTHORIZED).body("Invalid credentials");
              }
          }
      }
      ```

    * **Validate JWTs in subsequent requests:** 
        * In subsequent requests, the client includes the JWT in the `Authorization` header (e.g., `Authorization: Bearer <token>`).
        * Spring Security can be configured to intercept requests, extract the JWT from the header, and validate its authenticity and integrity.

    * **Example (Security Configuration):**

      ```java
      @Configuration
      @EnableWebSecurity
      public class SecurityConfig extends WebSecurityConfigurerAdapter {

          @Autowired
          private JwtTokenProvider jwtTokenProvider; 

          @Override
          protected void configure(HttpSecurity http) throws Exception {
              http
                  .httpBasic().disable() 
                  .csrf().disable() 
                  .sessionManagement().sessionCreationPolicy(SessionCreationPolicy.STATELESS) 
                  .and()
                  .authorizeRequests()
                      .antMatchers("/api/auth/login").permitAll() 
                      .anyRequest().authenticated() 
                  .and()
                  .exceptionHandling()
                      .authenticationEntryPoint(new JwtAuthenticationEntryPoint()) 
                  .and()
                  .apply(new JwtTokenFilterConfigurer(jwtTokenProvider)); 
          }
      }
      ```

**2. Role-Based Access Control (RBAC)**

* **Authorization:** Understand the concept of authorization, which determines what actions a user is allowed to perform within the application (e.g., which resources they can access, which operations they can execute).
* **Role-Based Access Control:** 
    * Learn how to implement RBAC, a common authorization model where users are assigned roles (e.g., "admin", "user", "guest") that determine their access privileges.
    * For example, an "admin" role might have full access to all resources, while a "user" role may have limited access.

* **Spring Security and RBAC:** 
    * Learn how to configure Spring Security to implement role-based access control.
    * Define roles and assign them to users within your application.
    * Secure endpoints by specifying the required roles for accessing those endpoints using the `@PreAuthorize` or `@Secured` annotations.

    * **Example:**

      ```java
      @RestController
      @RequestMapping("/api/data")
      public class DataController {

          @GetMapping("/admin")
          @PreAuthorize("hasRole('ADMIN')") 
          public String getAdminData() {
              return "Admin data";
          }
      }
      ```

**3. Securing API Endpoints**

* **Common Security Vulnerabilities:** Learn about common security vulnerabilities in web applications, such as:
    * **SQL Injection:** Attackers inject malicious SQL code into user input to manipulate the database.
    * **Cross-Site Scripting (XSS):** Attackers inject malicious scripts into web pages viewed by other users.
    * **Cross-Site Request Forgery (CSRF):** Attackers trick users into performing unintended actions on a web application.

* **Securing API Endpoints:** 
    * Implement security measures to protect your API endpoints from common attacks:
        * **Input Validation and Sanitization:** Validate and sanitize all user input to prevent injection attacks.
        * **Proper Error Handling and Logging:** Handle and log errors gracefully to prevent sensitive information from being leaked.
        * **Use of Security Headers:** Implement security headers like HTTP Strict Transport Security (HSTS) and Content Security Policy (CSP) to enhance the security of your application.

**Mini-Project: Add User Authentication to Your Backend API**

Today's challenge: Enhance your existing backend API (from Day 6) with user authentication.

* **Features:**
    * Implement user registration and login functionality.
    * Issue JWTs to authenticated users.
    * Secure API endpoints with appropriate roles and permissions (e.g., only allow authenticated users to access certain endpoints).

* **Technical Requirements:**
    * Use Spring Security and JWT for authentication.
    * Implement RBAC to control user access to different API endpoints.
    * Test your authentication and authorization mechanisms thoroughly.

**Resources:**

* **Spring Security Documentation:** [https://spring.io/projects/spring-security/](https://spring.io/projects/spring-security/) - Official documentation for Spring Security.
* **JWT Documentation:** [https://jwt.io/](https://jwt.io/) - Information about JWTs and their usage.
* **OWASP Cheat Sheet Series:** [https://cheatsheetseries.owasp.org/](https://cheatsheetseries.owasp.org/) - A valuable resource for learning about common web security vulnerabilities.

**Let's get coding!**

This enhanced README provides a comprehensive guide for Day 8 of Web Genesis, covering key security concepts and best practices for building secure backend applications. Remember to refer to the official documentation, experiment with the code examples, and prioritize security in all your development efforts.

**Bonus Tip:** Explore advanced security features like two-factor authentication (2FA), rate limiting, and security auditing to further enhance the security of your applications.


## *Created by:*

*Atharva Wakodikar*

---

## *Contributing*

Feel free to contribute by suggesting edits, adding more resources, or sharing your learning experiences.
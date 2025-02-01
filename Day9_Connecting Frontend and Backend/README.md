# Web Genesis: Day 9 - Connecting Frontend and Backend

**Welcome back to Web Genesis!** Today we'll connect the dots between our frontend and backend applications, learning how to fetch data from your Spring Boot API and display it dynamically in your React frontend.

**1. Fetching Data from the Backend**

* **Making API Requests:** 
    * Use the `fetch` API or libraries like `axios` to make HTTP requests to your Spring Boot API endpoints.
    * Handle responses from the server, including success and error cases.

    * **Example (using `fetch`):**

      ```javascript
      fetch('/api/tasks') 
          .then(response => response.json()) 
          .then(data => {
              // Handle the fetched data (e.g., update component state)
              setTasks(data); 
          })
          .catch(error => {
              console.error('Error fetching data:', error);
          });
      ```

* **Handling API Responses:**
    * Parse the JSON data received from the server.
    * Handle potential errors (e.g., network errors, server errors, invalid responses).
    * Display error messages to the user in a user-friendly way.

**2. Displaying Dynamic Data with React Components**

* **Rendering Data in Components:** 
    * Learn how to render data fetched from the backend within your React components.
    * Use JavaScript to map over arrays of data and render a list of components.

    * **Example:**

      ```javascript
      function TaskList({ tasks }) {
          return (
              <ul>
                  {tasks.map(task => (
                      <li key={task.id}>{task.title}</li> 
                  ))}
              </ul>
          );
      }
      ```

* **Conditional Rendering:** 
    * Learn how to conditionally render UI elements based on the data received from the backend.
    * Use conditional rendering techniques (e.g., `if`, `else`, ternary operator) to display loading states, error messages, or different UI components based on the data availability.

**3. Form Submissions and Handling API Responses**

* **Controlled Components:** 
    * Learn how to create controlled components in React, where the component's state is the "single source of truth" for form input values.

    * **Example:**

      ```javascript
      function MyForm() {
          const [inputValue, setInputValue] = useState('');

          const handleChange = (event) => {
              setInputValue(event.target.value);
          };

          const handleSubmit = (event) => {
              event.preventDefault(); 
              // Make a POST request to the backend API
              fetch('/api/data', {
                  method: 'POST',
                  headers: {
                      'Content-Type': 'application/json'
                  },
                  body: JSON.stringify({ data: inputValue }) 
              })
              .then(response => {
                  // Handle the response from the server
              })
              .catch(error => {
                  // Handle errors
              });
          };

          return (
              <form onSubmit={handleSubmit}>
                  <input 
                      type="text" 
                      value={inputValue} 
                      onChange={handleChange} 
                  />
                  <button type="submit">Submit</button>
              </form>
          );
      }
      ```

* **Handling API Responses in Form Submissions:**
    * Handle successful responses from the server (e.g., update state, display success messages).
    * Handle errors appropriately (e.g., display error messages to the user).
    * Implement loading states to provide visual feedback to the user while the request is in progress.

**Mini-Project: Build a Full-Stack App with React and Spring Boot**

Today's challenge: Build a simple full-stack application that connects your React frontend to your Spring Boot backend.

* **Project Ideas:**
    * **To-Do List App:** Enhance your to-do list app by fetching and displaying tasks from your Spring Boot API.
    * **Simple Blog:** Create a basic blog with a React frontend that fetches and displays blog posts from your Spring Boot backend.
    * **User Dashboard:** Build a simple user dashboard that displays user information and allows users to update their profiles.

* **Technical Requirements:**
    * Use React to build the frontend UI.
    * Make HTTP requests to your Spring Boot backend using `fetch` or `axios`.
    * Display data from the backend in your React components.
    * Implement form submissions to interact with the backend API.

**Resources:**

* **React Documentation:** [https://reactjs.org/](https://reactjs.org/) - Official documentation for React.
* **Axios Documentation:** [https://axios-http.com/](https://axios-http.com/) - Documentation for the Axios HTTP client.

**Let's get coding!**

This enhanced README provides a comprehensive guide for Day 9 of Web Genesis, covering key concepts for connecting your frontend and backend applications. Remember to refer to the official documentation, experiment with the code examples, and build your own full-stack applications to solidify your understanding.

**Bonus Tip:** Explore state management libraries like Redux or Zustand to manage data flow and handle complex interactions between components in your React applications.


## *Created by:*

*Atharva Wakodikar*

---

## *Contributing*

Feel free to contribute by suggesting edits, adding more resources, or sharing your learning experiences.
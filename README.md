1. What is the MERN Stack?
Answer: The MERN stack is a collection of technologies used to build web applications. It consists of:

MongoDB (NoSQL database)

Express.js (Web framework for Node.js)

React.js (Frontend library for building user interfaces)

Node.js (Backend JavaScript runtime)

2. What is MongoDB?
Answer: MongoDB is a NoSQL database that stores data in a flexible, JSON-like format known as BSON. Unlike relational databases, MongoDB doesn't require a predefined schema, allowing for more dynamic data structures.

3. What are the advantages of using MongoDB?
Answer:

Scalability: Easily scales horizontally through sharding.

Flexible schema: Allows storing data in a JSON-like format, making it easier to adjust the schema without downtime.

High performance: Suitable for high-speed data processing and real-time analytics.

Document-oriented: Data is stored as documents, making it more aligned with real-world entities.

4. What is Express.js?
Answer: Express.js is a lightweight web application framework for Node.js. It simplifies the development of web applications by providing features like routing, middleware support, and request handling, making it easier to build RESTful APIs.

5. What are middleware functions in Express.js?
Answer: Middleware functions are functions that have access to the request, response, and the next function in the request-response cycle. They can modify the request or response, handle errors, or terminate the request-response cycle.

Example:

js
Copy code
app.use((req, res, next) => {
  console.log('Middleware triggered');
  next(); // Proceed to the next middleware or route handler
});
6. What is Node.js?
Answer: Node.js is a runtime environment that allows you to run JavaScript code on the server side. It uses the V8 JavaScript engine (the same engine used by Google Chrome) to execute JavaScript code and is designed for building scalable, non-blocking, and event-driven applications.

7. What are the benefits of using Node.js?
Answer:

Non-blocking I/O: Asynchronous operations improve performance for I/O-heavy tasks.

Single programming language: Both frontend and backend can be written in JavaScript.

Scalability: Suitable for building scalable network applications, thanks to its event-driven, non-blocking architecture.

Active community: Node.js has a large community and many useful packages available via npm.

8. What is React.js?
Answer: React.js is a JavaScript library for building user interfaces, primarily for single-page applications (SPAs). It allows developers to create reusable UI components, manage state efficiently, and render UI dynamically.

9. What is JSX in React?
Answer: JSX (JavaScript XML) is a syntax extension for JavaScript that allows writing HTML-like elements in JavaScript code. It provides a declarative way to describe the UI structure and is compiled into JavaScript by tools like Babel.

10. What is Virtual DOM in React?
Answer: The Virtual DOM is a lightweight copy of the actual DOM in memory. When there is a change in the UI, React updates the Virtual DOM first. Then, React compares the updated Virtual DOM with the previous one (using a process called “reconciliation”) and only applies the minimal changes to the real DOM, making updates more efficient.

11. What are React Hooks?
Answer: React Hooks are functions that allow you to use state and lifecycle features in functional components. Common hooks include:

useState: To manage state in a component.

useEffect: To perform side effects in function components.

useContext: To access context values in a component.

12. Explain the concept of state and props in React.
Answer:

State: Represents the local data or information about a component that can change over time and trigger re-renders.

Props: Short for "properties," props are used to pass data from a parent component to a child component. They are immutable inside the child component.

13. What is the purpose of useEffect in React?
Answer: useEffect is used to handle side effects in functional components, such as data fetching, subscriptions, and manually updating the DOM. It runs after the component has rendered and can be used to mimic lifecycle methods (like componentDidMount, componentDidUpdate, and componentWillUnmount).

Example:

js
Copy code
useEffect(() => {
  // Code to run on component mount
}, []);  // Empty dependency array ensures it runs once after the initial render
14. What is the difference between a class component and a functional component in React?
Answer:

Class Component: A class-based component that extends React.Component and has lifecycle methods, state, and other features.

Functional Component: A simpler form of component that is a JavaScript function. It can use hooks (like useState and useEffect) to manage state and side effects in modern React development.

15. How do you manage state in a React application?
Answer: State in a React application is managed using the useState hook in functional components or this.state in class components. For complex state management across many components, state can be managed using useContext, Redux, or other state management libraries.

16. What is Redux?
Answer: Redux is a predictable state container for JavaScript apps, commonly used with React. It allows you to manage the state of the application in a centralized store and provides actions and reducers to update that state. It simplifies state management in large applications.

17. What is the role of NPM in a Node.js application?
Answer: NPM (Node Package Manager) is used to manage dependencies in Node.js applications. It allows you to install, update, and manage libraries and packages that your application depends on. You can install packages using the npm install command.

18. What is a RESTful API?
Answer: A RESTful API is an API that adheres to the principles of Representational State Transfer (REST). It uses standard HTTP methods (GET, POST, PUT, DELETE) and is stateless, meaning each request contains all the information needed for the server to process it.

19. How does the Express.js routing work?
Answer: Express.js routing defines how the server should respond to different HTTP requests made to specific endpoints. You define routes with HTTP methods (GET, POST, PUT, DELETE) and associate them with a callback function.

Example:

js
Copy code
app.get('/users', (req, res) => {
  res.send('Get list of users');
});
20. How would you connect a Node.js application to a MongoDB database?
Answer: To connect a Node.js application to MongoDB, you typically use the mongoose library. Here's an example:

js
Copy code
const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/mydatabase', {
  useNewUrlParser: true,
  useUnifiedTopology: true
})
.then(() => console.log('Connected to MongoDB'))
.catch(err => console.log('Error connecting to MongoDB:', err));
21. What is CORS and how can you handle it in Express.js?
Answer: CORS (Cross-Origin Resource Sharing) is a security feature that restricts web applications from making requests to a domain different from the one that served the web page. You can handle CORS in Express.js by using the cors middleware.

Example:

js
Copy code
const cors = require('cors');
app.use(cors());
22. How do you handle authentication in a MERN stack app?
Answer: Authentication in a MERN stack app is typically handled using JSON Web Tokens (JWT). The process involves:

User sends login credentials to the server.

The server validates the credentials and sends a signed JWT back to the client.

The client stores the token (usually in localStorage) and includes it in subsequent requests to protected routes.

23. How do you handle error handling in Express.js?
Answer: You can handle errors in Express.js using middleware that catches errors and sends an appropriate response.

Example:

js
Copy code
app.use((err, req, res, next) => {
  console.error(err);
  res.status(500).send('Something went wrong');
});
24. How would you deploy a MERN stack application?
Answer: A MERN stack application can be deployed using cloud platforms like Heroku, AWS, or DigitalOcean. The general steps include:

Push the code to a Git repository (e.g., GitHub).

Set up environment variables (e.g., MongoDB URI, JWT secret).

Deploy the frontend (React) and backend (Node.js/Express) to the cloud service.

Configure DNS and SSL certificates if needed.

These questions and answers should help you get a good understanding of MERN stack concepts for your interview preparation. Feel free to dive deeper into each topic depending on the specific job role and expectations.








25. What is the role of useReducer in React? 

Answer: useReducer is a React hook used for managing complex state logic in a component. It’s similar to useState but is typically used when state changes depend on the previous state or when the logic for state transitions is complex.

It uses a reducer function to describe how the state should change.

Example:

js

Copy code

const initialState = { count: 0 }; const reducer = (state, action) => { switch(action.type) { case 'increment': return { count: state.count + 1 }; case 'decrement': return { count: state.count - 1 }; default: return state; } }; const Counter = () => { const [state, dispatch] = useReducer(reducer, initialState); return ( <> <p>Count: {state.count}</p> <button onClick={() => dispatch({ type: 'increment' })}>Increment</button> <button onClick={() => dispatch({ type: 'decrement' })}>Decrement</button> </> ); }; 

26. How does Redux work in a MERN stack application? 

Answer: Redux is used for global state management. It consists of:

Actions: Objects that describe a change in state.

Reducers: Functions that specify how the state should change in response to actions.

Store: Holds the global state and allows access to it.

The process typically follows these steps:

The user interacts with the UI, which triggers an action.

The action is dispatched to the Redux store.

The reducer listens for the action type and updates the global state accordingly.

The updated state is reflected in the React components.

27. How would you optimize performance in React applications? 

Answer: Several strategies can optimize performance in React:

Memoization: Using React.memo to prevent unnecessary re-renders of functional components.

useCallback: Memoizing functions to prevent them from being recreated on every render.

Lazy Loading: Use React.lazy and Suspense to load components only when needed.

Code Splitting: Break down the application into smaller bundles that load on demand.

Avoid Inline Functions in JSX: Defining functions inside JSX can lead to unnecessary re-renders.

Virtualization: Use libraries like react-window to only render visible items in long lists.

28. How do you handle forms in React? 

Answer: In React, forms can be handled in two ways:

Controlled Components: Where React manages the form state via the useState hook.

Example:

js

Copy code

const MyForm = () => { const [inputValue, setInputValue] = useState(""); const handleSubmit = (e) => { e.preventDefault(); console.log(inputValue); }; return ( <form onSubmit={handleSubmit}> <input type="text" value={inputValue} onChange={(e) => setInputValue(e.target.value)} /> <button type="submit">Submit</button> </form> ); }; 

Uncontrolled Components: Letting the DOM handle the form state via ref.

29. What are the different types of HTTP requests in Express? 

Answer: In Express, HTTP requests are categorized by the following methods:

GET: Used to retrieve data from the server.

POST: Used to send data to the server to create resources.

PUT: Used to update an existing resource on the server.

DELETE: Used to remove a resource from the server.

PATCH: Used to update parts of a resource.

Example:

js

Copy code

app.get('/users', (req, res) => { /* Handle GET request */ }); app.post('/users', (req, res) => { /* Handle POST request */ }); app.put('/users/:id', (req, res) => { /* Handle PUT request */ }); app.delete('/users/:id', (req, res) => { /* Handle DELETE request */ }); 

30. What is the purpose of npm start and npm run build? 

Answer:

npm start: Runs the development server and starts the application in development mode. Typically, it invokes the command specified in the "start" script in the package.json file (e.g., react-scripts start for React apps).

npm run build: Creates a production-ready build of the application. It bundles, minifies, and optimizes the code for deployment. For React, it creates a build/ folder with all the static assets.

31. What is mongoose in Node.js? 

Answer: Mongoose is an ODM (Object Data Modeling) library for MongoDB and Node.js. It provides a straightforward way to interact with MongoDB databases, offering features such as schema validation, middleware support, and more. Example:

js

Copy code

const mongoose = require('mongoose'); const userSchema = new mongoose.Schema({ name: String, age: Number }); const User = mongoose.model('User', userSchema); User.create({ name: 'Alice', age: 25 }) .then(user => console.log(user)) .catch(err => console.log(err)); 

32. How do you implement authorization using JWT in a MERN application? 

Answer: JWT (JSON Web Tokens) is used to securely transmit information between the client and server. The typical flow is:

The client sends login credentials (email and password) to the server.

The server verifies the credentials and sends a signed JWT token to the client.

The client stores the token (usually in localStorage or sessionStorage).

For each subsequent request to protected routes, the client includes the token in the Authorization header.

The server verifies the JWT on every request to ensure the user is authenticated.

Example:

js

Copy code

const jwt = require('jsonwebtoken'); // After validating the user credentials: const token = jwt.sign({ userId: user._id }, 'secretKey', { expiresIn: '1h' }); // Send token to client res.json({ token }); 

In the frontend, the token is added to requests:

js

Copy code

fetch('/api/protected', { headers: { 'Authorization': `Bearer ${token}` } }) 

33. What is the purpose of dotenv in a Node.js application? 

Answer: dotenv is a zero-dependency module used to load environment variables from a .env file into process.env. This allows for easy management of environment-specific configurations, such as database credentials, API keys, or server port numbers.

Example:

Install the dotenv package:

bash

Copy code

npm install dotenv 

Create a .env file:

ini

Copy code

DB_URI=mongodb://localhost/mydb JWT_SECRET=your-secret-key 

Use it in the app:

js

Copy code

require('dotenv').config(); console.log(process.env.DB_URI); // Access environment variable 

34. How would you handle database migrations in MongoDB? 

Answer: Unlike relational databases, MongoDB doesn't have built-in support for migrations. However, you can manage schema changes manually or with libraries like migrate-mongo or mongodb-migrations to facilitate migration.

For example, using migrate-mongo:

Install the package:

bash

Copy code

npm install migrate-mongo 

Set up migration configuration and define migration scripts to manage schema changes.

35. How can you make an Express API RESTful? 

Answer: To make an API RESTful, follow these principles:

Use HTTP methods correctly (GET for fetching, POST for creating, PUT for updating, DELETE for deleting).

Use meaningful and plural resource names (e.g., /users, /posts).

Make the API stateless (no session data on the server).

Return appropriate status codes:

200 OK for successful GET requests.

201 Created for successful POST requests.

400 Bad Request for invalid data.

404 Not Found for missing resources.

500 Internal Server Error for server-side issues.

Example of a simple RESTful API route:

js

Copy code

app.get('/users', (req, res) => { /* Fetch users */ }); app.post('/users', (req, res) => { /* Create user */ }); app.put('/users/:id', (req, res) => { /* Update user */ }); app.delete('/users/:id', (req, res) => { /* Delete user */ }); 

These questions delve deeper into advanced concepts and topics within the MERN stack. They cover areas such as state management, optimization, security, deployment, and database handling that will be essential in a real-world MERN stack development environment.







36. What is useContext in React and how is it different from useState? 

Answer: useContext is a React hook used to share state across multiple components without having to manually pass props through every level of the component tree. It is often used for global state management like themes, authentication, or language settings. useState, on the other hand, is used to handle local state in a single component.

Example using useContext:

js

Copy code

const ThemeContext = React.createContext('light'); const ThemeProvider = ({ children }) => { const [theme, setTheme] = useState('light'); return ( <ThemeContext.Provider value={{ theme, setTheme }}> {children} </ThemeContext.Provider> ); }; const MyComponent = () => { const { theme, setTheme } = useContext(ThemeContext); return ( <div> Current theme: {theme} <button onClick={() => setTheme('dark')}>Change Theme</button> </div> ); }; 

37. What is the difference between async/await and Promises in JavaScript? 

Answer:

Promises: A Promise is an object that represents the eventual completion (or failure) of an asynchronous operation and its resulting value.

async/await: This is syntactic sugar over Promises, making asynchronous code look and behave more like synchronous code. It makes the code easier to read and maintain.

Example with Promises:

js

Copy code

fetchData().then(result => { console.log(result); }).catch(err => { console.error(err); }); 

Example with async/await:

js

Copy code

const fetchData = async () => { try { const result = await fetch('/api/data'); console.log(result); } catch (err) { console.error(err); } }; 

38. What are Higher-Order Components (HOCs) in React? 

Answer: A Higher-Order Component (HOC) is a pattern in React that allows you to reuse component logic. HOCs are functions that take a component and return a new component with enhanced behavior.

Example:

js

Copy code

function withLoading(Component) { return function LoadingComponent({ isLoading, ...props }) { if (isLoading) return <div>Loading...</div>; return <Component {...props} />; }; } const MyComponent = ({ data }) => <div>{data}</div>; const MyComponentWithLoading = withLoading(MyComponent); 

39. What is the purpose of useMemo in React? 

Answer: useMemo is a hook used to memoize expensive function results so that the function is not recomputed unless the dependencies change. It helps improve performance by preventing unnecessary re-calculations on every render.

Example:

js

Copy code

const expensiveCalculation = (num) => { console.log("Calculating..."); return num * 2; }; const MyComponent = ({ num }) => { const memoizedValue = useMemo(() => expensiveCalculation(num), [num]); return <div>{memoizedValue}</div>; }; 

40. What is CORS and how do you handle it in Node.js? 

Answer: CORS (Cross-Origin Resource Sharing) is a security feature implemented by browsers that restricts web pages from making requests to a domain other than the one that served the web page. To enable CORS in a Node.js application, you can use the cors middleware.

Example:

js

Copy code

const cors = require('cors'); app.use(cors()); // This enables CORS for all routes 

You can also configure it for specific routes or domains:

js

Copy code

app.use(cors({ origin: 'http://example.com' })); 

41. What is the role of require in Node.js? 

Answer: In Node.js, require is used to import modules (built-in or external) or files into a script. It loads and executes the module and returns its exports so they can be used in the current file.

Example:

js

Copy code

const fs = require('fs'); // Importing built-in fs module const myModule = require('./myModule'); // Importing a local module 

42. How does MongoDB handle relationships between data? 

Answer: MongoDB, being a NoSQL database, typically doesn't use traditional relational data models. However, relationships can be modeled in the following ways:

Embedded documents: Storing related data inside the same document.

Referenced documents: Storing references to other documents using ObjectId.

Example of embedded document:

js

Copy code

const userSchema = new mongoose.Schema({ name: String, posts: [{ title: String, content: String }] // Embedding posts inside the user document }); 

Example of referenced documents:

js

Copy code

const userSchema = new mongoose.Schema({ name: String }); const postSchema = new mongoose.Schema({ title: String, user: { type: mongoose.Schema.Types.ObjectId, ref: 'User' } // Referencing User model }); 

43. What is the difference between var, let, and const in JavaScript? 

Answer:

var: Function-scoped or globally scoped. It can be redeclared and updated.

let: Block-scoped. It can be updated but not redeclared in the same scope.

const: Block-scoped. It cannot be updated or redeclared.

Example:

js

Copy code

var x = 10; let y = 20; const z = 30; 

44. What is the purpose of React.StrictMode? 

Answer: React.StrictMode is a wrapper component used in development mode to identify potential problems in an application. It helps identify unsafe lifecycles, legacy API usage, and other issues that might cause problems in future React versions. It does not affect the production build.

Example:

js

Copy code

<React.StrictMode> <App /> </React.StrictMode> 

45. How do you create a custom middleware in Express? 

Answer: Custom middleware functions in Express are functions that have access to the request, response, and next function in the request-response cycle. You can create custom middleware to log data, handle authentication, validate requests, etc.

Example of custom middleware:

js

Copy code

const myMiddleware = (req, res, next) => { console.log('Request received'); next(); // Pass control to the next middleware }; app.use(myMiddleware); 

46. What is useRef in React? 

Answer: useRef is a React hook that returns a mutable object called a ref, which can hold a value that persists across renders. It is typically used to access DOM elements directly or store mutable values that do not trigger a re-render when updated.

Example:

js

Copy code

const MyComponent = () => { const inputRef = useRef(null); const focusInput = () => { inputRef.current.focus(); // Focus the input element }; return ( <div> <input ref={inputRef} /> <button onClick={focusInput}>Focus the input</button> </div> ); }; 

47. What is the role of next() in Express middleware? 

Answer: In Express middleware, next() is a function used to pass control to the next middleware function in the stack. If next() is not called, the request-response cycle will not continue, and the client will not receive a response.

Example:

js

Copy code

const myMiddleware = (req, res, next) => { console.log('Processing request...'); next(); // Passes control to the next middleware }; app.use(myMiddleware); 

48. What is a JWT Token's payload, and what does it consist of? 

Answer: A JSON Web Token (JWT) consists of three parts: the header, the payload, and the signature.

Header: Specifies the algorithm used (e.g., HS256).

Payload: Contains the claims, such as user information and metadata (e.g., user ID, roles, expiration).

Signature: Ensures the token has not been tampered with by signing it using a secret key.

Example payload:

json

Copy code

{ "sub": "1234567890", // Subject (e.g., user ID) "name": "John Doe", "iat": 1516239022 // Issued at time } 

49. What is the useEffect cleanup function in React? 

Answer: The cleanup function in useEffect is executed when the component is unmounted or before the effect is re-run. It is useful for cleaning up resources like subscriptions, event listeners, or timers.

Example:

js

Copy code

useEffect(() => { const timer = setInterval(() => { console.log('Timer running'); }, 1000); // Cleanup function return () => { clearInterval(timer); // Stops the timer when the component is unmounted or re-renders }; }, []); 

50. What are some ways to secure a Node.js application? 

Answer: Several strategies can be used to secure a Node.js application:

Use HTTPS: Encrypt data in transit using SSL/TLS.

Sanitize inputs: Prevent SQL injection and XSS attacks by sanitizing user inputs.

Authentication & Authorization: Implement JWT or OAuth for secure authentication and role-based access control (RBAC).

Rate Limiting: Use libraries like express-rate-limit to limit the number of requests.

Helmet.js: Use the helmet middleware to set secure HTTP headers.

Environment Variables: Store sensitive data (e.g., API keys, DB passwords) in environment variables.

Example:

js

Copy code

const helmet = require('helmet'); app.use(helmet()); 

These additional questions dive deeper into advanced topics like optimization, performance, state management, security, and understanding key React features and Node.js concepts. They should help prepare you for even more challenging interview questions.



51. What is the significance of React.Fragment? 

Answer: React.Fragment is used to return multiple elements from a component without adding extra nodes to the DOM. It doesn’t create an additional DOM element like a div, which helps avoid unnecessary nesting of elements.

Example:

js

Copy code

const MyComponent = () => { return ( <React.Fragment> <h1>Title</h1> <p>Content</p> </React.Fragment> ); }; 

Alternatively, you can use the shorthand version:

js

Copy code

const MyComponent = () => ( <> <h1>Title</h1> <p>Content</p> </> ); 

52. What is the purpose of getServerSideProps in Next.js? 

Answer: getServerSideProps is a function in Next.js used for server-side rendering (SSR). It runs on the server on each request and provides data to the page before rendering. This is useful for dynamic data fetching on the server before rendering the page.

Example:

js

Copy code

export async function getServerSideProps() { const res = await fetch('https://api.example.com/data'); const data = await res.json(); return { props: { data } }; } const Page = ({ data }) => { return <div>{data}</div>; }; export default Page; 

53. What is the difference between React.Component and React.PureComponent? 

Answer:

React.Component: The base class for all React components, which re-renders when any props or state change.

React.PureComponent: A subclass of React.Component that implements shouldComponentUpdate with a shallow prop and state comparison. This helps optimize performance by preventing unnecessary re-renders when the props and state have not changed.

54. What is the purpose of redux-thunk in a Redux-based application? 

Answer: redux-thunk is a middleware used in Redux to handle asynchronous actions. It allows action creators to return a function (instead of an action object) that can dispatch other actions and handle async operations like API calls.

Example:

js

Copy code

const fetchData = () => { return (dispatch) => { dispatch({ type: 'FETCH_START' }); fetch('/data') .then((res) => res.json()) .then((data) => { dispatch({ type: 'FETCH_SUCCESS', payload: data }); }) .catch((error) => { dispatch({ type: 'FETCH_ERROR', payload: error }); }); }; }; 

55. What are the different types of database indexes, and why are they important? 

Answer: Indexes are used to optimize query performance in databases:

Single-field index: An index on a single field, improving the performance of queries filtering or sorting on that field.

Compound index: An index on multiple fields, improving queries that filter or sort by multiple fields.

Text index: Used for full-text search.

Geospatial index: Used for spatial queries, such as location-based searches.

Indexes speed up read operations but can slow down write operations (insertion, update, and deletion) as the index needs to be updated.

56. What is a Promise.all() in JavaScript? 

Answer: Promise.all() is a method that allows you to execute multiple asynchronous tasks in parallel. It returns a promise that resolves when all the input promises are resolved, or it rejects as soon as one of the promises is rejected.

Example:

js

Copy code

const fetchData = () => Promise.resolve("Data fetched"); const fetchMoreData = () => Promise.resolve("More data fetched"); Promise.all([fetchData(), fetchMoreData()]) .then((results) => { console.log(results); // ["Data fetched", "More data fetched"] }) .catch((error) => { console.error(error); }); 

57. How does useLayoutEffect differ from useEffect in React? 

Answer:

useEffect: It runs after the component has rendered and is useful for handling side effects like fetching data or updating the DOM asynchronously.

useLayoutEffect: It runs synchronously after all DOM mutations, before the browser has painted. This is useful for situations where you need to measure the DOM or make DOM updates before the page is rendered to the user.

Example:

js

Copy code

useEffect(() => { // Side effect that runs after render }, []); useLayoutEffect(() => { // Runs synchronously after all DOM mutations }, []); 

58. How do you handle pagination in MongoDB? 

Answer: In MongoDB, pagination is typically done using the skip() and limit() methods, or using the range operator with find() queries. The skip() method skips a number of records, while limit() sets the number of records returned.

Example:

js

Copy code

const page = 1; const limit = 10; const skip = (page - 1) * limit; db.collection('items') .find() .skip(skip) .limit(limit) .toArray((err, result) => { console.log(result); }); 

Alternatively, you can use the _id field for efficient pagination by storing the last item’s _id in the frontend and querying for items after that ID.

59. How do you handle file uploads in Express? 

Answer: File uploads in Express can be handled using middleware like multer. Multer is a middleware for handling multipart/form-data, primarily used for uploading files.

Example:

Install multer:

bash

Copy code

npm install multer 

Use multer in an Express route:

js

Copy code

const multer = require('multer'); const upload = multer({ dest: 'uploads/' }); app.post('/upload', upload.single('file'), (req, res) => { console.log(req.file); // Information about the uploaded file res.send('File uploaded'); }); 

60. What is the useCallback hook in React? 

Answer: useCallback is a React hook used to memoize a function, ensuring that it doesn't get redefined on every render. It's useful when passing functions as props to child components, preventing unnecessary re-renders of those components.

Example:

js

Copy code

const ParentComponent = () => { const [count, setCount] = useState(0); const handleClick = useCallback(() => { setCount(count + 1); }, [count]); // Only re-create the function when `count` changes return <ChildComponent onClick={handleClick} />; }; 

61. What is a RESTful API and how does it differ from a GraphQL API? 

Answer:

RESTful API: REST (Representational State Transfer) is an architectural style for designing networked applications. It uses standard HTTP methods (GET, POST, PUT, DELETE) to perform CRUD operations on resources that are represented as URLs.

Example:

GET /users – Get a list of users

POST /users – Create a new user

GraphQL API: GraphQL is a query language for APIs that allows the client to request specific data. Unlike REST, where you define multiple endpoints for different operations, GraphQL exposes a single endpoint and lets the client query exactly what it needs.

Example:

A query might look like:

graphql

Copy code

{ users { id name } } 

62. How do you handle cross-site scripting (XSS) in Node.js? 

Answer: Cross-site scripting (XSS) is a vulnerability where malicious scripts are injected into web pages viewed by other users. To prevent XSS in Node.js:

Sanitize inputs: Use libraries like sanitize-html or validator to remove or escape user input that could contain HTML or JavaScript.

Use proper Content Security Policy (CSP): Implement CSP headers to control which resources can be loaded by the browser.

Escape HTML characters: Ensure any user-generated content rendered in the HTML is properly escaped to prevent scripts from executing.

Example using express-validator:

js

Copy code

const { body } = require('express-validator'); app.post('/submit', [ body('name').escape() // Escape user input to prevent XSS ], (req, res) => { // Handle submission }); 

63. What is useImperativeHandle in React? 

Answer: useImperativeHandle is a hook used to customize the instance value that is exposed when using React.forwardRef. It allows you to control what values are accessible via ref, typically used to expose certain methods to parent components without exposing the entire component instance.

Example:

js

Copy code

const MyComponent = React.forwardRef((props, ref) => { const focusInput = () => { console.log('Focusing input'); }; useImperativeHandle(ref, () => ({ focusInput })); return <input />; }); const Parent = () => { const ref = useRef(); const handleFocus = () => { ref.current.focusInput(); }; return ( <> <MyComponent ref={ref} /> <button onClick={handleFocus}>Focus Input</button> </> ); }; 

These additional questions explore more complex topics in the MERN stack, such as advanced React hooks, security, optimization, and server-side practices. They will help you prepare for higher-level interview scenarios and deepen your understanding of key concepts.


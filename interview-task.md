### JS Final Sprint

| Task                      | Focus                           | Difficulty  | Est. Time |
| ------------------------- | ------------------------------- | ----------- | --------- |
| **1. The Color Flipper**  | DOM Selection & Style           | Easy        | 15 mins   |
| **2. Character Guardian** | Events & Conditionals           | Easy-Medium | 20 mins   |
| **3. Price Calculator**   | Array Iteration & Checkboxes    | Easy-Medium | 25 mins   |
| **4. Precision Timer**    | Asynchronous JS (`setInterval`) | Medium-Hard | 30 mins   |
| **5. The Data Fetcher**   | Async/Await & API Logic         | Hard        | 30 mins   |

---

### 1. The Background Color Flipper

**Goal:** Create a button that changes the `document.body` background to a random color from an array: `['#FF5733', '#33FF57', '#3357FF', '#F333FF']`.

- **Requirement:** Display the hex code of the current color in a `<span>`.
- **Why?** Tests basic element selection and property manipulation.

### 2. Live Character Guardian

**Goal:** Create an `<input>` field and a counter (e.g., "0/20"). Update the number as the user types.

- **Requirement:** If the count exceeds 20, turn the counter text red and disable the "Submit" button.
- **Why?** Teaches `input` events and UI state synchronization.

### 3. Product Price Calculator

**Goal:** Create a page where users select products and calculate the total price using the provided array.

- **The Array:**

```js
const products = [
  { id: 1, name: "Keyboard", price: 50 },
  { id: 2, name: "Mouse", price: 30 },
  { id: 3, name: "Monitor", price: 300 },
  { id: 4, name: "Headphones", price: 80 },
];
```

- **Requirement:** 1. Render a list where each product has a **checkbox**.

2. When the user clicks a **"Calculate Total"** button, sum up only the checked items and display the total.

- **Why?** Teaches students how to link DOM elements (checkboxes) to a data source (array).

---

### 4. The 60-Second Countdown

**Goal:** Build a "Start" button that kicks off a countdown from 60 to 0 displayed on the screen.

- **Requirement:** Prevent the timer from speeding up if "Start" is clicked multiple times. Alert "Time's up!" at zero.
- **Why?** Master `setInterval` and the "clearing" logic required to prevent memory leaks or buggy UI.

### 5. The "Random User" Card

**Goal:** Use `fetch()` to grab one random user from `https://jsonplaceholder.typicode.com/users`.

- **Requirement:** 1. Display the user's name, email and address info.

2. Add a "New User" button to refresh the data.
3. Use a `try...catch` block to handle potential network errors.

- **Why?** This is the final boss—integrating external data, handling asynchronous flow, and updating the DOM dynamically.

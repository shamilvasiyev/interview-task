### The JS Final Sprint Part 2

| Task                            | Focus                     | Difficulty  | Est. Time |
| ------------------------------- | ------------------------- | ----------- | --------- |
| **1. Product Price Calculator** | Checkboxes & Math         | Easy        | 20 mins   |
| **2. User List Manager**        | Array CRUD (Add/Delete)   | Easy-Medium | 20 mins   |
| **3. Live Search Filter**       | `filter()` & Real-time UI | Medium      | 25 mins   |
| **4. Todo Filter System**       | State-driven UI           | Medium-Hard | 25 mins   |
| **5. Interactive Quiz App**     | Logic Flow & Score State  | Hard        | 30 mins   |

---

### 1. Product Price Calculator

**Goal:** Render a product list from an array and calculate a total based on user selection.

- **Requirements:** \* Generate a list of products (name/price) with a checkbox for each.
- When "Calculate Total" is clicked, sum the prices of only the checked items and display it on the page.

- **Why?** Teaches how to link UI elements (checkboxes) to data properties (price) using loops or `reduce`.

### 2. User List Manager

**Goal:** Build a dynamic list where users can enter names and remove them.

- **Requirements:** \* An input field and "Add" button that pushes a name to a list.
- Each list item must have a "Delete" button that removes that specific item.
- Prevent empty strings from being added.

- **Why?** Introduces the concept of "Event Delegation" and basic array manipulation (`push`, `splice`).

### 3. Live Search Filter

**Goal:** Create a real-time search engine for a course list that updates as the user types.

- **Requirements:** \* Display a list of courses from an array.
- As the user types in the search bar, use `.filter()` to show only matching courses (case-insensitive).
- Display "No courses found" if the array length hits zero.

- **Why?** Masters the link between `input` events and array filtering logic.

---

### 4. Todo List with Status Filter

**Goal:** A "State-first" Todo app where the UI changes based on a "Filter" setting.

- **Requirements:** \* Users can add tasks and mark them as "Completed" (toggling a class).
- Provide three buttons: **All**, **Completed**, and **Active**.
- The list must automatically re-render to show only the tasks that match the selected filter.

- **Why?** This is a massive leap in logic. It teaches students to treat their JS array as the "Source of Truth" for the UI.

### 5. Interactive Quiz App

**Goal:** A multi-step application that tracks progress and calculates a final score.

- **Requirements:** \* Show one question at a time using an object-based array.
- A "Next" button that only works if an answer is selected.
- A final screen that reveals the total score once the array is exhausted.

- **Why?** Tests "State Management" (tracking the current index) and complex conditional logic in a multi-step workflow.

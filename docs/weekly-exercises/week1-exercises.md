# Week 1: Foundation Building - Coding Exercises

## 🎯 Learning Objectives
- Understand React component structure
- Practice reading and modifying existing code
- Learn about props and state basics
- Explore the project file structure

---

## 📚 Exercise 1: Customize Your App Title
**Difficulty:** ⭐ Easy  
**Time:** 10 minutes

### Task
Personalize the main title in `src/pages/Index.tsx` to include your name.

### Steps
1. Open `src/pages/Index.tsx`
2. Find line 52-54 with the main title
3. Change "Plug-N-Learn" to "[Your Name]'s Data Hub"
4. Save and observe the changes in the preview

### Success Criteria
- [X] Title displays your personal name
- [X] Styling remains unchanged
- [X] No console errors appear

### Learning Focus
Understanding JSX and how React renders content.

---

## 📚 Exercise 2: Add a Personal Subtitle
**Difficulty:** ⭐ Easy  
**Time:** 15 minutes

### Task
Add your own custom subtitle below the main description.

### Steps
1. In `src/pages/Index.tsx`, find the description paragraph (lines 56-58)
2. Add a new paragraph after it with your own message
3. Use the same styling classes: `text-lg text-slate-500 max-w-2xl mx-auto`
4. Make it personal! Example: "Built by [Your Name] - Future Data Scientist"

### Success Criteria
- [X] New subtitle appears below the main description
- [X] Uses consistent styling with existing text
- [X] Appears properly centered and styled

### Learning Focus
JSX structure and CSS class application.

---

## 📚 Exercise 3: Explore Component Props
**Difficulty:** ⭐⭐ Medium  
**Time:** 20 minutes

### Task
Examine how the `DataUpload` component receives and uses props.

### Investigation Questions
1. What props does `DataUpload` expect? (Check the interface)
   - Based on the interface, DataUpload only expects the prop onDataLoad, which is a function that takes data (array of DataRow objects), fileName (string representing the name of the file), and it returns nothing (void).
2. How is the `onDataLoad` function passed from parent to child?
   - The parent creates a function named handleDataLoad that knows how to use the CSV data. From there, the parent passes it down as onDataLoad. The child function, DataUpload, calls that function once the parsing is done.
3. What happens when you upload a CSV file?
   - When a CSV file is uploaded, the application reads the file, registers the comma-separated data as rows & columns, the processes the data according to the application.

### Steps
1. Open `src/components/DataUpload.tsx`
2. Find the `DataUploadProps` interface (line 21)
3. Trace how `onDataLoad` is used in the component
4. Look at how it's called in `Index.tsx` (line 121)

### Success Criteria
- [X] Can identify the prop interface
- [X] Understand the data flow from child to parent
- [X] Can explain what `onDataLoad` does

### Learning Focus
React props, interfaces, and parent-child communication.

---

## 📚 Exercise 4: State Management Investigation
**Difficulty:** ⭐⭐ Medium  
**Time:** 25 minutes

### Task
Analyze the state management in the main `Index` component.

### Investigation Checklist
- [X] Identify all `useState` hooks in `Index.tsx`
- [X] Understand what data each state variable stores
- [X] Trace how state changes when a file is uploaded
- [X] Find where the conditional rendering happens (data vs. no data)

### Questions to Answer
1. What are the two main pieces of state being managed?
   - The two main pieces of state being managed are DataRow[] (Stores uploaded data), and string (Remembers file name).
2. What triggers the state to change?
   - The parent's event handler triggers the state to change; when a user uploads a CSV file, DataUpload parses it, calls onDataLoad, which updates state in the parent.
3. How does the UI change based on state?
   - The UI changes based on state (data & fileName), triggers handleDataLoad when the CSV file uploads, and switches from upload screen to dashboard screen.

### Success Criteria
- [X] Can list all state variables and their purposes
- [X] Understand the conditional rendering logic
- [X] Can predict UI changes based on state changes

### Learning Focus
React hooks, state management, and conditional rendering.

---

## 🔍 Self-Assessment Quiz

### Question 1
What does JSX stand for and why is it useful?
- [X] A. JavaScript XML - allows HTML-like syntax in JavaScript
- [ ] B. JavaScript Extension - adds new features to JavaScript  
- [ ] C. Java Syntax Extension - connects Java and JavaScript
- [ ] D. JSON XML - converts between data formats

### Question 2
In React, what is a "prop"?
- [ ] A. A CSS property for styling components
- [X] B. Data passed from parent component to child component
- [ ] C. A JavaScript function that returns HTML
- [ ] D. A file that contains component code

### Question 3
What happens when you call a `setState` function in React?
- [ ] A. The component immediately re-renders
- [X] B. The component schedules a re-render for the next cycle
- [ ] C. The entire page refreshes
- [ ] D. Nothing happens until you manually refresh

### Answer Key
1. A - JSX allows HTML-like syntax in JavaScript
2. B - Props are data passed from parent to child
3. B - setState schedules a re-render for the next cycle

---

## 🏆 Challenge Exercise: Add a Footer
**Difficulty:** ⭐⭐⭐ Advanced  
**Time:** 30 minutes

### Task
Add a footer component to the bottom of your app with your name and the current year.

### Requirements
- Create the footer inside the main container
- Include your name and copyright notice
- Use consistent styling with the rest of the app
- Make it stick to the bottom of the page

### Bonus Points
- Add social media links (can be placeholder)
- Include a "Built with React" message
- Make the footer responsive

### Learning Focus
Component creation, styling, and layout management.

---

## 📝 Reflection Questions
1. What was the most challenging part of today's exercises?
   - The footer was definitely the most challenging part of all the exercises.
2. Which concept (JSX, props, state) do you want to explore more?
   - I'd like to explore more into JSX.
3. How comfortable do you feel reading existing React code?
   - Comfortable enough, I'd say.
4. What questions do you have about the project structure?
   - No, no questions.

---

## 🔗 Additional Resources
- [React Documentation - Components and Props](https://react.dev/learn/passing-props-to-a-component)
- [React Documentation - State](https://react.dev/learn/state-a-components-memory)
- [JSX Introduction](https://react.dev/learn/writing-markup-with-jsx)

## 💻 **Technical Round (HTML/CSS, JS, React.js)**

**1. Explain the difference between semantic and non-semantic HTML tags. Why does semantic HTML improve SEO and accessibility?**

> Semantic tags like `<header>`, `<article>`, `<nav>` clearly describe their purpose, while non-semantic tags like `<div>` or `<span>` don’t.
> Semantic HTML improves SEO because search engines understand page structure better, and it helps screen readers improve accessibility for users with disabilities.

---

**2. What are ARIA roles and how do they help improve accessibility?**

> ARIA roles provide extra information to assistive technologies.
> For example, `role="button"` on a custom element helps screen readers announce it as a button, making the app more accessible.

---

**3. How do CSS Specificity and Cascade rules interact?**

> Specificity decides which CSS rule wins if multiple rules target the same element.
> Inline styles > IDs > Classes > Elements.
> Cascade means later rules can override earlier ones if specificity is the same.

---

**4. Compare inline, block, and inline-block elements with examples.**

> * Inline: takes only as much width as needed (`<span>`).
> * Block: takes full width and starts on a new line (`<div>`).
> * Inline-block: behaves like inline but allows width and height (`<img>`).

---

**5. How can you make a complex layout responsive without using media queries (e.g., using Flexbox or Grid techniques)?**

> Using **Flexbox** or **CSS Grid** — they automatically adjust layout based on available space.
> For example, `flex-wrap: wrap` or `grid-template-columns: repeat(auto-fit, minmax(200px, 1fr))` helps elements adapt to screen size.

---

**6. Explain the difference between shallow copy and deep copy in JavaScript. How would you implement a deep copy manually?**

> Shallow copy copies only one level of an object; nested objects still share references.
> Deep copy duplicates everything.
> Example:
>
> ```js
> const deepCopy = JSON.parse(JSON.stringify(obj));
> ```

---

**7. What is the difference between call, apply, and bind? Give examples of each.**

> * **call()** – calls function with given `this` and arguments separated.
> * **apply()** – same but arguments are passed as an array.
> * **bind()** – returns a new function with bound `this`.
>
> ```js
> func.call(obj, a, b);
> func.apply(obj, [a, b]);
> const newFunc = func.bind(obj);
> ```

---

**8. How would you debounce and throttle a function manually without libraries?**

> * **Debounce:** waits for a pause before executing (e.g., search input).
> * **Throttle:** limits execution to once in a set time (e.g., scroll).
>
> ```js
> function debounce(fn, delay){ let t; return (...a)=>{clearTimeout(t); t=setTimeout(()=>fn(...a),delay);} }
> ```

---

**9. What is a WeakMap and when would you prefer it over a normal Map?**

> WeakMap keys must be objects and are garbage-collected automatically.
> It’s used for private data storage where we don’t want memory leaks.

---

**10. What are React Fiber and Concurrent Rendering? How do they improve UI responsiveness?**

> React Fiber is the re-written core algorithm that allows **splitting rendering work into chunks**.
> Concurrent Rendering improves UI responsiveness by pausing and resuming rendering tasks, so the UI stays smooth.

---

**11. Difference between controlled and uncontrolled components. Which one is better for large forms and why?**

> Controlled: React manages the form state.
> Uncontrolled: DOM manages it via refs.
> For large forms, controlled components are better since they provide full control and validation handling.

---

**12. Explain custom hooks — when would you create one? Provide an example for data fetching with error handling.**

> Custom hooks reuse logic across components.
> Example for data fetching:
>
> ```js
> function useFetch(url){
>  const [data,setData]=useState(null);
>  const [error,setError]=useState(null);
>  useEffect(()=>{
>   fetch(url).then(r=>r.json()).then(setData).catch(setError);
>  },[url]);
>  return {data,error};
> }
> ```

---

**13. How does React.memo differ from useMemo?**

> * `React.memo` memoizes entire **components**.
> * `useMemo` memoizes **values or calculations** inside a component.
>   `React.memo` avoids re-renders, while `useMemo` avoids expensive recalculations.

---

**14. How do you handle error boundaries in React functional components (since they only exist for class components)?**

> Functional components can handle errors using **`ErrorBoundary` wrappers** or **`useErrorBoundary`** from libraries like React Error Boundary.
> Alternatively, use try-catch inside async functions or data-fetching logic.

---

**15. How do you implement code-splitting and dynamic imports in React?**

> Use `React.lazy()` and `Suspense`:
>
> ```js
> const About = React.lazy(() => import('./About'));
> ```
>
> This loads the component only when needed, improving performance.

---

**16. Difference between Context API and Redux — when would you choose one over the other in a mid-size project?**

> * Context API: lightweight and great for simple state sharing (like theme or auth).
> * Redux: better for large apps with complex state logic and middleware.
>   For mid-size projects, Context API is often enough.

---

**17. React Component Task: Build a Search with Suggestions Component. 
Requirements: 
-- Input box that fetches suggestions (simulate with a static array or mock API). 
-- Show filtered suggestions below as the user types. 
-- Highlight the matching characters in suggestions.**

> Create an input that filters from a static array as user types.
> Highlight matching text using regex and wrap it with a `<mark>` tag.
> You can manage state using `useState` and filter suggestions in real-time.

---

## 🧠 **Managerial Round**

**1. Tell me about a situation where you had to deal with conflicting priorities or multiple deadlines. How did you manage your tasks?**

> During my internship, I had to deliver a UI feature and fix bugs simultaneously.
> I prioritized tasks based on deadlines and impact, communicated timelines clearly, and broke the work into smaller deliverables to stay on track.

---

**2. Describe a time when you disagreed with your team or manager about a technical approach. How did you resolve it?**

> Once, I suggested using a simpler layout instead of adding a library.
> I explained the performance benefits, and we reviewed both options.
> We agreed on my approach after testing the results together.

---

**3. How do you handle pressure situations — like production bugs or urgent client requirements?**

> I stay calm and analyze the issue first.
> For example, if a bug occurs, I reproduce it, check logs, and test possible fixes locally before pushing.
> I focus on solving, not panicking.

---

**4. Have you ever mentored or onboarded a new developer? What approach did you take to help them ramp up?**

> As a fresher, I haven’t mentored yet, but I often help peers understand React basics or project setup.
> I prefer explaining concepts visually and giving small practice tasks.

---

**5. In your opinion, what defines a good front-end engineer beyond just writing code?**

> A good engineer writes clean, reusable code, understands user experience, and communicates well with designers and backend teams.
> It’s not just about coding but delivering an intuitive, responsive interface.

---

## 💬 **HR Round**

**Expected CTC & Negotiation ?**

> As a fresher, I’m open to the company’s standard range for entry-level roles. My main focus is on learning and growing technically.

---

**Notice Period Discussion ?**

> Since I’m available immediately (or within 30–45 days if applicable), I can join as per project requirements.

---

### 🟡 **Intermediate / 2–5 Years Experience Level**

> These show up when the interviewer wants to test **depth** or **real-world understanding**:

**9. WeakMap and when to use it**

**10. React Fiber and Concurrent Rendering**

**14. Error boundaries in functional components (edge concept)**

> You won’t usually get these in the **first round** as a fresher, but sometimes interviewers throw one or two to see if you’ve gone beyond tutorials.

---

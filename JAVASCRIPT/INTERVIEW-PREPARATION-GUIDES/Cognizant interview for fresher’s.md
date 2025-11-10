💻 Technical Round (HTML/CSS, JS, React.js)

1. Semantic vs Non-Semantic HTML

Semantic tags like <header>, <article>, <nav> clearly describe their purpose, while non-semantic tags like <div> or <span> don’t.
Semantic HTML improves SEO because search engines understand page structure better, and it helps screen readers improve accessibility for users with disabilities.

⸻

2. ARIA Roles

ARIA roles provide extra information to assistive technologies.
For example, role="button" on a custom element helps screen readers announce it as a button, making the app more accessible.

⸻

3. CSS Specificity and Cascade

Specificity decides which CSS rule wins if multiple rules target the same element.
Inline styles > IDs > Classes > Elements.
Cascade means later rules can override earlier ones if specificity is the same.

⸻

4. Inline, Block, Inline-Block

	•	Inline: takes only as much width as needed (<span>).
	•	Block: takes full width and starts on a new line (<div>).
	•	Inline-block: behaves like inline but allows width and height (<img>).

⸻

5. Responsive Layout without Media Queries

Using Flexbox or CSS Grid — they automatically adjust layout based on available space.
For example, flex-wrap: wrap or grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)) helps elements adapt to screen size.

⸻

6. Shallow vs Deep Copy

Shallow copy copies only one level of an object; nested objects still share references.
Deep copy duplicates everything.
Example:

const deepCopy = JSON.parse(JSON.stringify(obj));



⸻

7. Call, Apply, Bind

	•	call() – calls function with given this and arguments separated.
	•	apply() – same but arguments are passed as an array.
	•	bind() – returns a new function with bound this.

func.call(obj, a, b);
func.apply(obj, [a, b]);
const newFunc = func.bind(obj);



⸻

8. Debounce and Throttle

	•	Debounce: waits for a pause before executing (e.g., search input).
	•	Throttle: limits execution to once in a set time (e.g., scroll).

function debounce(fn, delay){ let t; return (...a)=>{clearTimeout(t); t=setTimeout(()=>fn(...a),delay);} }



⸻

9. WeakMap

WeakMap keys must be objects and are garbage-collected automatically.
It’s used for private data storage where we don’t want memory leaks.

⸻

10. React Fiber and Concurrent Rendering

React Fiber is the re-written core algorithm that allows splitting rendering work into chunks.
Concurrent Rendering improves UI responsiveness by pausing and resuming rendering tasks, so the UI stays smooth.

⸻

11. Controlled vs Uncontrolled Components

Controlled: React manages the form state.
Uncontrolled: DOM manages it via refs.
For large forms, controlled components are better since they provide full control and validation handling.

⸻

12. Custom Hooks

Custom hooks reuse logic across components.
Example for data fetching:

function useFetch(url){
 const [data,setData]=useState(null);
 const [error,setError]=useState(null);
 useEffect(()=>{
  fetch(url).then(r=>r.json()).then(setData).catch(setError);
 },[url]);
 return {data,error};
}



⸻

13. React.memo vs useMemo

	•	React.memo memoizes entire components.
	•	useMemo memoizes values or calculations inside a component.
React.memo avoids re-renders, while useMemo avoids expensive recalculations.

⸻

14. Error Boundaries in Functional Components

Functional components can handle errors using ErrorBoundary wrappers or useErrorBoundary from libraries like React Error Boundary.
Alternatively, use try-catch inside async functions or data-fetching logic.

⸻

15. Code-Splitting and Dynamic Imports

Use React.lazy() and Suspense:

const About = React.lazy(() => import('./About'));

This loads the component only when needed, improving performance.

⸻

16. Context API vs Redux

	•	Context API: lightweight and great for simple state sharing (like theme or auth).
	•	Redux: better for large apps with complex state logic and middleware.
For mid-size projects, Context API is often enough.

⸻

17. Search with Suggestions (Concept)

Create an input that filters from a static array as user types.
Highlight matching text using regex and wrap it with a <mark> tag.
You can manage state using useState and filter suggestions in real-time.

⸻

🧠 Managerial Round

1. Handling Conflicting Priorities

During my internship, I had to deliver a UI feature and fix bugs simultaneously.
I prioritized tasks based on deadlines and impact, communicated timelines clearly, and broke the work into smaller deliverables to stay on track.

⸻

2. Disagreement with Team

Once, I suggested using a simpler layout instead of adding a library.
I explained the performance benefits, and we reviewed both options.
We agreed on my approach after testing the results together.

⸻

3. Handling Pressure Situations

I stay calm and analyze the issue first.
For example, if a bug occurs, I reproduce it, check logs, and test possible fixes locally before pushing.
I focus on solving, not panicking.

⸻

4. Mentoring or Onboarding

As a fresher, I haven’t mentored yet, but I often help peers understand React basics or project setup.
I prefer explaining concepts visually and giving small practice tasks.

⸻

5. What Defines a Good Front-End Engineer

A good engineer writes clean, reusable code, understands user experience, and communicates well with designers and backend teams.
It’s not just about coding but delivering an intuitive, responsive interface.

⸻

💬 HR Round

Expected CTC

As a fresher, I’m open to the company’s standard range for entry-level roles. My main focus is on learning and growing technically.

⸻

Notice Period

Since I’m available immediately (or within 30–45 days if applicable), I can join as per project requirements.

⸻

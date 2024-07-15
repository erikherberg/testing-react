# components

In React, components are functions
React components should be capitalized

```
function Header() {
  return <h1>Develop. Preview. Ship.</h1>;
}
 
const root = ReactDOM.createRoot(app);
root.render(<Header />);
```

# Props

```
function Header({ title }) {
  console.log(title);
  return <h1>{title}</h1>;
}
```

curly braces: any JavaScript expression

# Iteration

<ul>
    {names.map((name) => (
        <li>{name}</li>
    ))}
</ul>

# Event listener

`<button onClick={handleClick}>Like</button>`

# State Hook

- descriptive variable name
- descriptive setter
- initial state

```function HomePage() {
  // ...
  const [likes, setLikes] = React.useState(0);
 
  function handleClick() {
    setLikes(likes + 1);
  }
 
  return (
    <div>
      {/* ... */}
      <button onClick={handleClick}>Likes ({likes})</button>
    </div>
  );
}
```

- Instead, when you want to update an object and array, you need to create a new one
- React state behaves more like a snapshot. Setting it does not change the state variable you already have, but instead triggers a re-render. => updater function
- React lets you override the default behavior, and force a component to reset its state by passing it a different key, like <Chat key={email} />.
- consolidate all the state update logic outside your component in a single function, called “reducer”.

- create context ???

# SSR

- Client component: add `'client'` directive

- After Server Components are rendered, a special data format called the React Server Component Payload (RSC) is sent to the client. The RSC payload contains:
    - The rendered result of Server Components.
    - Placeholders (or holes) for where Client Components should be rendered and references to their JavaScript files.

- Next.js uses Server Components by default 

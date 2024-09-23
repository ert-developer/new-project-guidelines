```bash
Stage: COMPLETE
Contributor(s): Sai
```

The objective of this page is to document Code Review Checklist to follow by the Developers. The Code Reviewers must follow the same checklist. The Reviewers may have additional criteria, and they are free to provide comments based on them. If the checklist needs an update, please raise a request to do that ASAP.

## Get the Basics Right
- ✔ If you are creating/editing a Play, please update the related `Readme.md` file with relevant info. For any other changes, please look for any documentation impact and consider them accordingly.
- ✔ Your changes must support responsiveness. It means it should work on mobile devices without breaking or providing bad UX.
- ❌ Do not commit sensitive information. Always keep them in `.env` file. In this case, please inform the maintainers to include the environment variables in Vercel's settings so that the production build works well.
- ❌ Do not commit unnecessary files like VS code settings, yarn lock, etc. Make sure you have an entry to ignore them in the `.gitignore` file.
- ❌ There shouldn't be any new Error or Warning in the console due to your changes.
- ❌ There shouldn't be any typo or spelling mistake.
- ✔ Finally check if your code changes work as expected without impacting other functionalities.

## Coding Standards
This section provides you with pointers to make your code look and work better in practice.

### General
- ✔ Take care of the casing of variables, function names, modules, and style names.
- ✔ Refactor duplicate code by creating functions.
- ✔ Create smaller functions.
- ✔ Remove commented out code.
- ✔ Remove unused code.
- ✔ Remove console logs.
- ✔ Provide precise comments with "why have you done certain things". The "what" and "how" part is already covered by your code.

### JavaScript
- ✔ Use modern JavaScript features as much as possible. Like Spread, Rest operators, Array/Object destructuring, Nullish coalescing operator, Optional Chaining, and many more.
- ❌ Do not use var.
- ✔ Use let and const. Prefer const over let wherever possible.
- ✔ Use Arrow functions.

### React
- ✔ Create lean components. Do not overload the component with too much logic inside the render method.
- ✔ Return early from your component as much as possible. Do not encourage too much of if-else in the JSX part.
- ✔ Check out for duplication. Refactor your components into Hooks and re-usable utils.
- ✔ Identify side-effects and handle them in standard hooks like `useEffect`.
- ✔ Do not over-engineer performance with React.memo, useMemo(), or useCallback(). Ask yourself 5 times before using them, "Do I really need them?".
- ✔ Destructure props.
- ✔ Use functional components as much as possible.
- ✔ Handle data loading with a loading text/indicator.
- ✔ Handle error with an error message.
- ✔ Embrace custom hooks. Build a mindset to write them.
- ✔ Create and use context wisely.
- ✔ Create and use the Global data store wisely. Do not mutate state in reducer.
- ✔ Too many states to handle in a component? You may want to handle them as one state with an object as the value.
- ✔ Always clear off timers like setTimeout, setInterval in the useEffect.

### Styling
- ✔ Apply CSS specificity rules
- ❌ No Inline Styles.
- ❌ Do not duplicate styles.

## Pull Request Etiquettes
- ✔ When you create a PR, you need to provide all the answers in the description. Please do not leave them empty. You need to minimally provide a description and a link to the related issue on GitHub. A Code reviewer may not start reviewing without these details provided.
- ✔ When Ready for review, please add the `review ready` label. If you do not have permission to add it, please provide a comment saying Review Ready.
- ✔ Always Resolve all the comments.
- ✔ Keep the PR comments interactive. Ask questions, and clarify doubts, Code Reviewers are listening!
- ✔ Please check and respond to your PR comments at least once in 2 days to get it merged faster.
- ✔ Have Patience!







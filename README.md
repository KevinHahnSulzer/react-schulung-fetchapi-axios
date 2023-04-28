# Exercise: FetchAPI and axios

## Description:

A `DuckContext` that provides a image url state and two methods to load a static and a dynamic duck image into the url. Two components, `StaticDuckButton` and `DynamicDuckButton`, that use these methods to load a respective duck image. Then a third component, `DuckWalk`, that displays the current duck image using the data from the `DuckContext`

- The `DuckContext` should provide a state called `duckUrl` with an initial value of `''`, and two methods, `loadStaticDuck` (using `fetch()`) and `loadDynamicDuck`(using `axios.get()`), that update the duck image url state.
- The `StaticDuckButton` component should use the `loadStaticDuck` method from the DuckContext to load a static duck image when clicked.
- The `DynamicDuckButton` component should use the `loadDynamicDuck` method from the DuckContext to load a dynamic duck image when clicked.
- The `DuckWalk` component should display the current count using data from the `DuckContext`.

## Here are the steps to complete this exercise:

1. Create a new file called `DuckContext.tsx`. Inside this file, create a new `DuckContext` using the `createContext` function from the react library.
2. In DuckContext.tsx, create a new state variable called `duckUrl` with an initial value of `''`, using the `useState` hook from the react library.
3. In `DuckContext.tsx`, create two new methods called `loadStaticDuck` and `loadDynamicDuck` that update the `duckUrl` state, using the `setState` function returned by the useState hook.
   - `loadStaticDuck` have to use the url `https://random-d.uk/api/random?type=jpg` and the `fetch()` method
   - `loadDynamicDuck` have to use the url `https://random-d.uk/api/random?type=gif` and the `axios.get()` method
4. Wrap the `StaticDuckButton` and `DynamicDuckButton` components in the `DuckContext.Provider` component in order to provide the `duckUrl`, `loadStaticDuck`, and `loadDynamicDuck` values to these components.
5. In `StaticDuckButton.tsx`, create a new button that calls the `loadStaticDuck` method from the DuckContext when clicked.
6. In `DynamicDuckButton.tsx`, create a new button that calls the `loadDynamicDuck` method from the DuckContext when clicked.
7. In `DuckWalk.tsx`, use the `useContext` hook from the react library to access the count value from the DuckContext. Render this value as image to the screen.

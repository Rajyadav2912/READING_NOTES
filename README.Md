Package’s

1. npm install
2. npm start (for react)
3. npm run dev (for vite + react)
4. npx create-react-app project-name-app (for install or create a react app)
5. npm create vite@latest project-name-app – –template react (for install or vite + react app)
   codehelp-testimonial

---

Tailwind install 6. npm install -D tailwindcss (simple install in react) 7. npx tailwindcss init

8. npm create vite@latest project-name -- --template react (for tailwind install in vite + react)
9. npm install -D tailwindcss postcss autoprefixer
10. npx tailwindcss init -p

11. jo tailwind folder create hua hai usme yee fill krdo

/** @type {import('tailwindcss').Config} \*/
export default {
content: [
"./index.html",
"./src/**/\*.{js,ts,jsx,tsx}",
],
theme: {
extend: {},
},
plugins: [],
}

12. go to index.css and put these lines
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

13. npm i react-icons

14. npm i react-toastify
15. npm i react-hot-toast

16. npm i axios {this axios is automatically convert data into json formate}

---

Download Router

npm install react-router-dom

import { BrowserRouter } from "react-router-dom";

<BrowserRouter> <App/> </BrowserRouter>

import { Route, Routes } from "react-router-dom";
<Routes>
<Route path="" element={component}/>
</Routes>

---

Redux start

17. npm install @reduxjs/toolkit react-redux

# How to create a single slice using this function. createSlice()

// step 1 : create createSlice() and write three thing
// 1. name
// 2. initialState
// 3. reducers isme functionality & definition set hoti hai and then export

import { createSlice } from "@reduxjs/toolkit";

const initialState = {
value: 0,
};

export const CounterSlice = createSlice({
name: "counter",
initialState,
reducers: {
increment: (state) => {
state.value += 1;
},
decrement: (state) => {
state.value -= 1;
},
},
});

// createSlice 2 thing provide krta hn 1. reducer 2. action creator

// Action creators are generated for each case reducer function
// action creator me humre function & behaviour present hote hn unko
// destructure krke export kr deta hai

export const { increment, decrement } = CounterSlice.actions;

export default CounterSlice.reducer;

---

# // single ko export karna hota hai

The main step in redux. Create a store.jsx file

import { configureStore } from "@reduxjs/toolkit";
import CounterSlice from "./slices/CounterSlice";

// its is centralized store. its create by multiple slices
// CounterSlice is a single slice

export const store = configureStore({
reducer: {
counter: CounterSlice,
},
});

---

# How to link Redux code to React code using 3 step

import { Provider } from "react-redux";

// 1st export store file
// 2nd wrapped
/*  
// < Provider >
    < App/ >
< /Provider >
*/

// 3rd passed store in Provider component as a props

/*  
// < Provider  store={store}>
    < App/ >
< /Provider >
*/

# important thing

# How to access state in our component

import { useDispatch, useSelector } from "react-redux";

1st. const count = useSelector((state) => state.counter.value);

Ab isme jo functions hai unko call krna hai toh using useDispatch() Hook

2nd. const dispatch = useDispatch();

onClick={() => dispatch(increment())}
onClick={() => dispatch(decrement())}

# Backend Start

1. npm init -y
2. npm install express
3. npm install mongoose

4. npm i nodemon
5. npm i dotenv





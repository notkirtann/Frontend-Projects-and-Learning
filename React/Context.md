
# Context API in React
## Introduction to Context API
- The Context API is a built-in feature in React that allows you to share data between components without passing props manually at every level.
- It is useful for managing global state or sharing data that needs to be accessed by multiple components.
### Design Example for understanding problem before Context API :

- Imagine a component tree where a deeply nested child component needs access to a piece of data from a top-level parent component. Without Context API, you would have to pass the data down through each intermediate component, which can become cumbersome and hard to maintain.

- **Hindi mai explain kre toh :** 
Ek `<App/>` component hai jisme ek `<Card/>` component hai, uske andar ek `<Profile/>` component hai, fir uske andar ek `<Avatar/>` component hai. Ab maan lo ki `<Avatar/>` component ko `<App/>` component se koi data chahiye jaise ki user ka name ya theme color. Toh hume ye data pehle `<Card/>` ko dena padega, fir `<Card/>` se `<Profile/>` ko dena padega, aur fir `<Profile/>` se `<Avatar/>` ko dena padega. Is tarah se har intermediate component ko ye data pass karna padega, chahe unhe wo data ki zarurat na ho. Ye process bahut tedious ho sakta hai, especially jab component tree deep ho jata hai.
### Solution using Context API:
With Context API, you can create a context that holds the data and allows any component in the tree to access it directly, without the need to pass props through every level. 

This issues is commonly referred to as "prop drilling," and the Context API helps to eliminate it by providing a way to share data globally within a component tree.

Yeh jo context api hai yeh sirf react ke andar hi kaam karta hai, iska matlab yeh hai ki agar aap kisi dusre library ya framework ke sath kaam kar rahe hain toh aapko alag se state management solution use karna padega.
Uske liye use hota hai Redux ya MobX jaise libraries.

Redux ko react ke sath use karne ke liye aapko `react-redux` package install karna padega jo ki Redux ko React ke sath integrate karta hai.
`redux-toolkit` ek official, opinionated, batteries-included toolset hai jo Redux ke sath use hota hai jisse Redux ka setup aur development process asaan ho jata hai.

### UserContext Example:
```jsx
import React from "react";

const UserContext = React.createContext()

export default UserContext
```
### Using Context Provider and Consumer:
```jsx
import React, { useState } from "react";
import UserContext from "./UserContext";
import Avatar from "./Avatar";
const App = () => {
  const [user, setUser] = useState({ name: "Kirtan Nahar", theme: "dark" });

  return (
    <UserContext.Provider value={user}>
      <Avatar />
    </UserContext.Provider>
  );
};
export default App;
```
need of user context provider is to make the user data available to all components that are wrapped inside the provider. In this case, the `<Avatar />` component can access the user data without needing to receive it as a prop from the `<App />` component.
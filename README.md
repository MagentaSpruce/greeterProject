# greeterProject
Created with CodeSandbox using React

This simple React app uses dynamic insertions to render a greeting determined based upon a range of hours in the day. Each range of hours is further denoted by being rendered in a specific color. This can easily be utilized in a variety of applications with minimal changes.

Creating this app helped me to better learn and practice the following:
1) Creating React applications
2) JSX attributes and styling 
3) Inline styling

A brief walkthrough of the react code is given below:

First create the React App.
```React
import React from "react";
import ReactDOM from "react-dom";
```

Next create the dates needed.
```React
const date = new Date();
const currentTime = date.getHours();
```

Create the greeting and custom styling to be dynamically inserted.
```React
let greeting;

const customStyle = {
  color: ""
};
```

Implement the logic.
```React
if (currentTime < 12) {
  greeting = "Good Morning";
  customStyle.color = "red";
} else if (currentTime < 18) {
  greeting = "Good Afternoon";
  customStyle.color = "green";
} else {
  greeting = "Good evening";
  customStyle.color = "blue";
}
```

Finally render dynamically to the page.
```React

ReactDOM.render(
  <div>
    <h1 className="heading" style={customStyle}>
      {greeting}
    </h1>
  </div>,
  document.getElementById("root")
);
```

***End Walkthrough


## Structure

- **App.jsx**  
  The main application component. Sets up the theme context and renders the UI.

- **main.jsx**  
  Entry point for the React app. Renders the [`App`](App.jsx) component into the DOM.

- **index.css**  
  Global styles using Tailwind CSS.

- **Components/**
  - **Card.jsx**  
    A sample product card component with theme-aware styling.
  - **ThemeBtn.jsx**  
    A toggle button for switching between light and dark themes.

- **context/**
  - **theme.js**  
    Provides the theme context, including the current theme and functions to switch themes.

## How It Works

- The [`ThemeProvider`](context/theme.js) supplies theme state and functions to the app.
- [`ThemeBtn`](Components/ThemeBtn.jsx) allows users to toggle between light and dark modes.
- The selected theme is applied to the `<html>` element, enabling Tailwind's dark mode classes.
- [`Card`](Components/Card.jsx) demonstrates theme-aware UI.

## Usage

All components in this folder are imported and used in [`App.jsx`](App.jsx).  
You can add more components or contexts as needed for your application.

## remeber to change config in tailwind

```javascript 
    /** @type {import('tailwindcss').Config} */
    export default {
        content: [
        "./index.html",
        "./src/**/*.{js,ts,jsx,tsx}",
    ],
    darkMode: "class",
    theme: {
        extend: {},
    },
    plugins: [],
    }

```
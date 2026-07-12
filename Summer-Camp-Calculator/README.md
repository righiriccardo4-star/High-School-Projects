# Summer Camp Fee Calculator

A lightweight, client-side web application designed to automate and validate fee computations for summer camp registrations. 

This project is an internationalized, refactored, and optimized English version of a live high school programming exam originally developed in Italian. The codebase has been upgraded to implement clean code architecture, robust state management, and strict input validation boundaries.

## Features

- **Dynamic Fee Estimation**: Computes total registration costs based on customizable package options (Base, Sport, Languages, Premium), catering services, and extracurricular activities.
- **Age-Based Discount Logic**: Automatically applies a **75% discount** for children under 6 years old.
- **Strict Input Validation**: Features front-end sanitization to prevent logical errors (e.g., negative weeks, empty inputs, or entering a higher number of underage children than the total amount of children).
- **Interactive State Workflow**: Synchronizes values between user selections and the DOM, forcing calculation updates before allowing form submission.

## Tech Stack

- **HTML5** – Structured form layout using semantic fieldsets and accessible labeling.
- **CSS3** – Minimalist styling with dynamic status alert panels (`#ffcccc` for validation errors, `#d4edda` for success states).
- **JavaScript (ES6)** – Vanilla functional programming leveraging DOM manipulation, prompt alerts, array iteration, and floating-point precision parsing (`toFixed(2)`).

## Architectural Improvements (Refactoring Notes)

Compared to the original examination script written under tight time constraints, this version introduces:
1. **Scope Safety**: Eliminated unstable global leaks by properly scoping block variables (`const` and `let`).
2. **Encapsulation**: Abstracted the radio button parsing into a reusable lookup function (`getSelectedRadioValue`).
3. **Bug Fixes**: Resolved edge-case errors where users could trigger confirmation strings with `undefined` balances prior to calculating the actual fee.
4. **Clean Code Naming**: Fully converted all functions, variables, and HTML attributes from Italian to standard English *camelCase* notation.

## How to Run

Since this application relies entirely on client-side vanilla JavaScript, it requires zero external dependencies or server environments. 
Simply open `index.html` in any modern web browser, or launch it directly via GitHub Pages.

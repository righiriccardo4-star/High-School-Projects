# C++ Probability Simulator (Dice Rolls) 🎲

This is a foundational C++ project developed during my 3rd year of High School. It focuses on the implementation of procedural programming and basic statistical analysis.

### Features
- **Customizable Simulation**: Input the number of faces (D4 to D20) and the number of dice (up to 5).
- **Statistical Analysis**: Calculates both **Absolute** and **Relative Frequency** for specific outcomes over a set number of trials (up to 100).
- **Multi-modal Testing**: 
  - Single roll probability.
  - Multiple rolls of a single die.
  - Simultaneous multi-dice rolls (checking for identical outcomes).

### Technical Implementation
- **Memory Management**: Uses 2D arrays (`matrix`) to track results across multiple trials.
- **Pass-by-Reference**: Efficient handling of variables using C++ references (`int &Facce`).
- **Control Flow**: Implements a robust menu-driven interface using `switch-case` and `do-while` loops for input validation.

### Project Context
This script represents my first steps into **stochastic modeling**. Although it uses a basic pseudo-random generator (`rand()`), it establishes the logic required for more advanced Monte Carlo simulations used in Aerospace Engineering and Financial Modeling.

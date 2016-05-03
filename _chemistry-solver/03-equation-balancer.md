---
title: "Equation Balancer"
permalink: /chemistry-solver/equation-balancer/
---
{% include base_path %}

![Equation Balancer]({{base_path}}/images/portfolio/chemistry-solver/equation-balancer.png){: .align-center}

{% include toc %}

### Overview
The Equation Balancer is a tool that quickly balances equations and displays the results in a clear and beautiful way. What differentiates this equation balancer from others are the methods for equation input; complete chemical equations can be entered via the provided keyboard, or manually by typing it in the required format.

### Equation Input
There are two methods for entering equations into the application, the first is through the keyboard-like tool, and the second is through manually typing it in. The method chosen is solely based the user's discretion. To facilitate the ease of entering equations, newcomers are encouraged to use the keyboard method initially.

In the keyboard method, equation input is done through the clicking of elements, pluses, and arrows. As each button on the keyboard is clicked, the element or symbol it represents will be printed into the equation input text box in the proper format. When clicking an element button, subsequent clicks will increase the element count in the subscript.

The manual method is where the user types the equation into the input textbox, in the correct format, instead of utilizing the keyboard method described above.

### Equation Format
Equations entered into the equation balancer are interpreted from a format that's unique to this application. The anatomy of a Chemistry Solver equation can be broken down into a few parts: reactants and products, and then separators.

Reactants and products are formatted the same way, and will have a coefficient in front of them indicating the number of that reactant or product present. For example, if hydrogen were a reactant, it would be formatted like ```1H```. It's intended that the number 1 will be present when there is only one of that reactant or product present.

For each element found within the reactant or product, a subscript must also accompany it. Subscripts are in the format ```_(# of atoms)```. For example, if we had the hydrogen molecule as a reactant, it would be formatted as ```1H_(2)```. Chains of elements would be formatted like ```1H_(2)O_(1)```, where there are 2 hydrogen atoms and 1 oxygen atom.

Separators come in two forms, a ```+``` and a ```-->```. Pluses separate consecutive reactants and products, and arrows separate reactants from products. If we had the equation for the formation of water, it would be formatted as it is below.

```
1H_(2) + 1O_(2) --> 1H_(2)O_(1)
```
And would appear like this in the application:

![Equation Input]({{base_path}}/images/portfolio/chemistry-solver/equation-balancer-input.png){: .align-center}

### Balancing Equations
To balance an equation, an equation in the correct format, must first be supplied. Clicking the balance button will then balance the equation and display the results in an output space at the bottom of the tool.

![Equation Input]({{base_path}}/images/portfolio/chemistry-solver/equation-balancer-balanced.png){: .align-center}

The calculated coefficients of each reactant and product will be colored in a way to make them easily noticeable so the user can see how the application balanced the equation.

### Clearing Equations
To clear all equation input and balancing results from the application, click the clear button. The Equation Balancer will reset back to a clean state.



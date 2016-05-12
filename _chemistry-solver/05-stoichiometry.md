---
title: "Stoichiometry"
permalink: /chemistry-solver/stoichiometry/
---
{% include base_path %}

![Stoichiometry]({{base_path}}/images/portfolio/chemistry-solver/stoichiometry.png){: .align-center}

{% include toc %}

### Overview
The Stoichiometry module allows the user to perform conversions for any valid chemical equation its given. When a chemical equation is entered, it is automatically balanced and is displayed in the equation textbox at the top of the window. Conversions between substance and unit pairs are represented as a mathematical equation, where the left-hand side is equal to the right. When performing a conversion, the user is free to choose between any combination of substances and units, and the application will quickly and accurately perform the conversion. 

### Equation Input
Chemical equations are entered by typing or pasting a properly formatted string into the textbox at the top of the window, and then pressing the 'Enter' button. Equations can be either balanced or unbalanced, as the application automatically balances every equation given to it. The equations entered can be constructed and copied from the [Equation Balancer](/chemistry-solver/equation-balancer/) tool, or the user can manually type them in. To learn how to properly format a chemical equation, see [this](/chemistry-solver/equation-balancer/#equation-format) documentation.

![Equation Entered]({{base_path}}/images/portfolio/chemistry-solver/stoichiometry-with-equation.png){: .align-center}

### Usage
Conversions are made based on the substance and units in both the left and right-hand side of the equality, and are calculated immediately as the user types in values into either textbox. The equality can be read as: `x units of substance A is equal to y units of substance B`, where 'substance A' is defined by the controls on the left side of the equation, and 'substance B' is on the right.

![Molecule Selection]({{base_path}}/images/portfolio/chemistry-solver/stoichiometry-molecule-selection.png){: .align-center}

To perform a conversion, the user must select the substance and units they are starting with, as well as the substance and units they wish to end with. Typing a value into either textbox will perform a conversion where the entered value is considered the starting substance, and the opposite side is the ending substance. For all other conversions, such as when the units or substance is changed on either side of the equation, the direction of the conversion is from left to right.

### Further Reading
Stoichiometry is the basis for many aspects of chemistry, ranging from finding the limiting and excess reactants in a chemical equation, to solving molarity problems. The Stoichiometry module is a tool that was designed to be generic, and thus versatile. When used in conjunction with a solid understanding of the subject, the tool serves as an excellent assistant in solving a wide array of problems. For more information on how this tool can be used and how the functionality was implemented, see my [blog post]().


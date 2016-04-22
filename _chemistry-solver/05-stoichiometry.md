---
title: "Stoichiometry"
permalink: /chemistry-solver/stoichiometry/
---
After creating the unit converter, I decided to swap out the implementation of the Stoichiometry tool with that of the unit converter. It will remove a few classes that aren't reusable, and will provide a uniform way to calculate conversion between units.

With this change, I will be borrowing the "immediate-feedback" theme of the unit converter for use in this tool. In addition, the tool will now display information about the limiting and excess reactants, and yield of the supplied equation.
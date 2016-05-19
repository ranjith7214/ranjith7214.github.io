---
title: "Programming Stoichiometry - Part 1"
header:
    overlay_color: "#777"
excerpt: "The first in a two part series about how I programmed the [Stoichiometry Module](/chemistry-solver/stoichiometry/). In this part, I discuss what stoichiometry is and why it's needed in chemistry. Topics include stoichiometric conversions, limiting and excess reactants, and yield."
categories:
    - Guides
    - Stoichiometry
tags:
    - Limiting Reactant
    - Excess Reactants
    - Theoretical Yield
    - Actual Yield
    - Percent Yield
    - Stoichiometry
    - Dimensional Analysis
---
{% include katex_import.html %}

### What is Stoichiometry?
Let's say you just got a random urge to make some cookies. You go online, find a *great* recipe, and start gathering all the ingredients you need. According to the recipe, you can make 48 cookies from the following ingredients: 

* 3 cups all purpose flour
* 1 cup butter
* 1 <span class="equation" data-expr="^1/_2"></span> cups sugar

After some searching, you realize that you have all of the required ingredients, but not in the correct amounts. You only have 2 cups of all purpose flour, instead of 3, and all of the butter and sugar. You don't want to go to the store to buy more flour, and so you're resolved to work with what you have. You know that when using all of the ingredients in the proper amounts, the recipe will make 48 cookies, but since you have fewer ingredients than what's required, you don't know how many cookies you can make. Certainly with the reduced amount of all purpose flour, the recipe will make fewer cookies, and since the cookies should taste the same, the ingredient ratios found in the original recipe must be preserved. How do you go about finding a solution to your problem? How many cookies can you make, and in what amounts are the butter and sugar needed so that you can make the same great tasting cookies with only 2 cups of flour?

To answer these questions, we need to use a tool that lets us scale quantities while maintaining the physical relationships between ingredients. What we need is stoichiometry. Stoichiometry can be translated directly as "the measure of elements," and in principal, is performed through the multiplication of conversion ratios. These ratios are often obtained from the data being worked on, and represent correlations between units. By multiplying a chain of conversion ratios that have mutual units, quantities can be translated from one unit to another, resulting in an output with the desired dimension.

To demonstrate how to perform stoichiometry, let's look back at the cookie recipe example above and answer the all of the lingering questions. We'll determine the relationships between the ingredients, and thus the conversion ratios we'll use to multiply with. We'll calculate the new amounts of butter and sugar needed, so that ingredient ratios are maintained, and finally, we'll learn how many cookies the recipe will produce with only 2 cups of all purpose flour.

**Example: Cookie Recipe**

Before we can perform any stoichiometry, we need to figure out what the relationships are between the ingredients in the recipe. This is done by equating each unit to one another, and recording the equality in the form of a ratio, where the ratio is defined as <span class="equation" data-expr="\left(\text{quantity of ingredient x} \over \text{quantity of ingredient y}\right)"></span>. If this is done for all ingredients in the recipe, you'll have <span class="equation" data-expr="{n! \over k!(n-k)!}"></span> unique ratios to work with. If we convert the aforementioned cookie recipe into an equation, we'll have:

<div class="equation" data-expr="
\displaystyle
\begin{array}{ccccccc}
\text{3 cups flour} &
+ &
\text{1 cup butter} &
+ &
\text{1}^1/_2\,\text{cups sugar} &
= &
\text{48 cookies}
\end{array}
"></div>

From the equation, we can see that there are 4 items in the equation; 3 ingredients and 1 product. The total number of items in the equation is our *n* value. Since the conversion ratios will be between one unit and another, we know that the ratio will be created between a pair of 2 ingredients, which gives us our *k* value. With this, we'll have  <span class="equation" data-expr="{4! \over 2!(2)!} = 6"></span> unique conversion ratios to use in our calculations, as shown below.

<div class="equation" data-expr="
\begin{matrix}
\left(\frac{\text{3 cups flour}}{\text{48 cookies}}\right) &
\left(\frac{\text{3 cups flour}}{\text{1 cup butter}}\right) &
\left(\frac{\text{3 cups flour}}{\text{1}^1/_2\text{ cups sugar}}\right) 

\\

\left(\frac{\text{1 cup butter}}{\text{1}^1/_2\text{ cups sugar}}\right) &
\left(\frac{\text{1 cup butter}}{\text{48 cookies}}\right) &
\left(\frac{\text{1}^1/_2\text{ cups sugar}}{\text{48 cookies}}\right) 
\end{matrix}
"></div>

Each conversion ratio should be read from top to bottom as *x of unit A is equal to y of unit B*, such that for our ingredient ratios, it would be read as *3 cups of flour is equal to 48 cookies*. If it is desirable to read the ratio from bottom to top, the fraction must be inverted. The resulting ratio will describe the same relationship as before, but coming from the opposite direction.

With the ingredient ratios identified, we can use them to determine the amount of cookies that can be made from 2 cups of flour. When performing any stoichiometric conversion, it's important to know what your starting value is, and what the value is that you're hoping to achieve. Once you know where to begin and where to end, you can determine the chain of conversion ratios that let you traverse between them. 

For this problem, we're trying to move between cups of flour to # of cookies, and so beginning with what we have, our starting value is 2 cups of all purpose flour. To determine how to convert from the starting value to the desired ending value, we need to look at the ratios that were derived from the equation. As per the theory of dimensional analysis, we need to find ratios that have cancellable units so that we can remain in the correct "ingredient" dimension. The idea is to have the unit in the numerator of the previous ratio be the same as the unit in the denominator in the current ratio. Since both units are considered values, and are the same, they will cancel once the product between them is calculated. This leads us to the following series of ratios, which will convert the starting ingredient to the desired ending ingredient, and thus, the number of cookies 2 cups of flour will make.

<div class="equation" data-expr="
\begin{array}{ccccc}
\left(\frac{\text{2 cups flour}}{1}\right) &
\times &
\left(\frac{\text{48 cookies}}{\text{3 cups flour}}\right) &
= &
\text{32 cookies}
\end{array}
"></div>

Following suit, we'll use the same process to determine how much butter and sugar we'll need in the modified recipe. The starting value will remain the same, as that's the amount that we have, and is what we're trying to convert into other ingredients. Beginning with butter, the series of ratios will be as follows.

<div class="equation" data-expr="
\begin{array}{ccccc}
\left(\frac{\text{2 cups flour}}{1}\right) &
\times &
\left(\frac{\text{1 cup butter}}{\text{3 cups flour}}\right) &
= &
^2/_3\text{ cups of butter}
\end{array}
"></div>

And for sugar,

<div class="equation" data-expr="
\begin{array}{ccccc}
\left(\frac{\text{2 cups flour}}{1}\right) &
\times &
\left(\frac{\text{1}^1/_2\text{ cups sugar}}{\text{3 cups flour}}\right) &
= &
\text{1 cup sugar}
\end{array}
"></div>

With stoichiometry, we were able to solve the baker's ingredient dilemma, and determine that with 2 cups of all purpose flour, the recipe will make 32 cookies. Furthermore, to maintain the same ingredient ratios, the other ingredients in the recipe needed to be used in less amounts. We determined that <span class="equation" data-expr="^2/_3"></span> cups of butter and 1 cup of sugar will combine with the 2 cups of flour to produce the same *great* tasting cookies.

The baking example above is a real life application of stoichiometry, but chemistry is the field where it's most commonly used. Where chemical equations are to recipes, ingredients and the finished result is to reactants and products. A chemical equation is essentially the 'recipe' for a chemical reaction, where reactants are the ingredients, and the products are the end result. In chemistry, similar situations as what was solved above arise frequently. For example, a chemist might have a limited amount of reactant, or might want to know how much of each reactant that will be needed to produce an exact quantity of product. 

For the latter question, the amount of product created by a chemical reaction is a little more difficult to obtain than in the recipe example. The rate of consumption between reactants has to be considered, as not all compounds are used uniformly. This leads to some reactants being used quicker than others, which limits the amount of product that is created.

### Limiting and Excess Reactants
When a chemical reaction takes place between the reactants in an equation, the amount of each reactant consumed isn't uniform. The reaction might require less of one reactant and more of another, and depends on the substances present in the equation. This leads to a logistical issue between the amount of substances that are given, and the amount of each substance that's needed to completely react with one another. If one substance is completely consumed before any other substance, then the reaction is halted and no more product is created. This reactant is called a *limiting reactant* since it limits the amount of product that's produced in a chemical reaction. The substances that remain after the limiting reactant is completely consumed are called *excess reactants*, since the amounts that remain aren't needed.

There are a few ways to determine what the limiting and excess reactants are in a chemical equation. One way revolves around the comparison between how much of each reactant that's present, to how much of each reactant that is required for a complete chemical reaction. If one reactant is needed in a quantity greater than what is given, then that reactant is the limiting reactant. For the opposite situation, where we have more of a reactant than what's required, the reactant is considered to be in excess.

**Example: Determining Limiting and Excess Reactants**

The combustion of propane is a useful chemical reaction that occurs in everyday life. It's used as a heat source when grilling, as a fuel for various engines, and for other interesting applications. To analyze the reaction and determine which reactants are limiting and which are in excess, we'll find the difference between the amounts of each reactant we have, and what's required in the reaction. The smallest value indicates that the respective reactant is the limiter and that all others are in excess. 

So, if we have 90 g of propane and 150 g of oxygen, which reactant is limiting and which is in excess? To answer this, we first need to know what the balanced equation is for the combustion of propane:

<div class="equation" data-expr="
\begin{array}{ccccccc}
\text{C}_3\text{H}_8 &
+ &
\text{5O}_2 &
\rightarrow &
\text{4H}_2\text{O} &
+ &
\text{3CO}_2 &
\end{array}
"></div>

Having a balanced equation is necessary because it gives us the correct information to work with while creating conversion ratios. In chemistry, conversion ratios are made based on both the units and the substances you're trying to convert between. There are an infinite combination of elements that react with one another, and it's possible to determine the mass, moles, and number of particles found in each. This leads to a multitude of conversion ratios that are available to use, which I'll discuss in more detail in the next part of this series. 

When determining which conversion ratios are useful for your specific problem, it's important to know that the mole is the gateway to other units. You can convert the mole into both the mass and the number of particles of a substance *by summing the molar mass of all elements included in the substance*, and by *knowing that 1 mole of any element is equal to 6.022E+23 atoms*, respectively. For our problem, we need to determine how much of each reactant we have, in moles, and compare that to how many moles of each reactant that's needed. This leads us to the following useful conversion ratios, which can be inverted as needed:

<div class="equation" data-expr="
\begin{matrix}
\left(\frac{\text{1 mole C}_3\text{H}_8}{\text{44.1 g C}_3\text{H}_8}\right) &
\left(\frac{\text{1 mole O}_2}{\text{32.0 g O}_2}\right) &
\left(\frac{\text{1 mole C}_3\text{H}_8}{\text{5 moles O}_2}\right) &
\end{matrix}
"></div>

The conversion ratios were created based on the relationship between the different units and the mole. For example, *1 mole of propane is equal to 44.1 grams of propane*, which is the molar mass of the compound. Similarly, *1 mole of molecular oxygen is equal to 32 grams of molecular oxygen*. Lastly, it is necessary to know the molar relationship between the reactants, which is described in the remaining ratio: *1 mole of propane is equal to 5 moles of molecular oxygen*.

To determine the amount of each reactant that we have, we need to convert the given mass of each into moles. 

<div class="equation" data-expr="
\begin{matrix}
\left(\frac{\text{90 g C}_3\text{H}_8}{1}\right) &
\times &
\left(\frac{\text{1 mole C}_3\text{H}_8}{\text{44.1 g C}_3\text{H}_8}\right) &
= &
\text{2.04 moles C}_3\text{H}_8 

\\

\left(\frac{\text{150 g O}_2}{1}\right) &
\times &
\left(\frac{\text{1 mole O}_2}{\text{32.0 g O}_2}\right) &
= &
\text{4.69 moles O}_2
\end{matrix}
"></div>

Next, we need to determine how much of each reactant that's needed to completely react with one another.

<div class="equation" data-expr="
\begin{matrix}
\left(\frac{\text{2.04 moles C}_3\text{H}_8}{1}\right) &
\times &
\left(\frac{\text{5 mole O}_2}{\text{1 mole C}_3\text{H}_8}\right) &
= &
\text{10.2 moles O}_2 

\\

\left(\frac{\text{4.69 moles O}_2}{1}\right) &
\times &
\left(\frac{\text{1 mole C}_3\text{H}_8}{\text{5 moles O}_2}\right) &
= &
\text{0.938 moles C}_3\text{H}_8
\end{matrix}
"></div>

This tells us that 10.2 moles of molecular oxygen is needed to completely react with the 90 g of propane we were given, and that .938 moles of propane are needed to completely react with the 150 g of molecular oxygen. If we find the difference between the moles of reactants that we have, with what we need, we can figure out which reactant is the limiter and which is in excess.

<div class="equation" data-expr="
\begin{matrix}
\text{2.04 moles C}_3\text{H}_8 &
- &
\text{.938 moles C}_3\text{H}_8 &
= &
\text{1.102 moles C}_3\text{H}_8 

\\

\text{4.69 moles O}_2 &
- &
\text{10.2 moles O}_2 &
= &
\text{-5.51 moles O}_2 
\end{matrix}
"></div>

With the quantities given initially, the 150 g of oxygen will run out before the 90 g of propane. This is because we have 1.102 more moles of propane than what is required, but not enough oxygen. This indicates that oxygen is the limiting reactant and that propane is in excess. Knowing this information will let us predict how much yield a reaction will produce, and is called the theoretical yield.

### Theoretical, Actual, and Percent Yield
The theoretical yield of a reaction is the maximum amount of product that can be produced from a chemical reaction, as determined by the limiting reactant. It is calculated by performing stoichiometric conversions between the mass or moles of the limiting reactant into the mass or moles of a product. The product chosen is irrelevant because the limiting reactant is only dependant on the other compounds it reacts with. Once the reaction takes place, all products cease to be created as soon as the limiting reactant runs out.

**Example: Calculating Theoretical Yield**

In the example given above, about the combustion of propane, we were given the mass of the reactants that was present before the combustion occurred. If we were asked to determine how much water was produced as a result of the reaction, we'd need to calculate water's theoretical yield. We know that oxygen was the limiting reactant in the equation, and so we'll use that to determine the mass of the water produced.

<div class="equation" data-expr="
\begin{array}{ccccccccc}
\left(\frac{\text{150 g O}_2}{1}\right) &
\times &
\left(\frac{\text{1 mol O}_2}{\text{32.0 g O}_2}\right) &
\times &
\left(\frac{\text{4 mol H}_2\text{O}}{\text{5 mol O}_2}\right) &
\times &
\left(\frac{\text{18.015 g H}_2\text{O}}{\text{1 mol H}_2\text{O}}\right) &
= &
\text{67.6 g H}_2\text{O} 
\end{array}
"></div>

Observant readers might note that by calculating the yield of a product, for each reactant in the equation, they can compare the amount of product being created by each and determine what the limiting reactant is. The reactant with the least amount of product created is the limiting reactant.
{: .notice--info}

In reality, there will be a difference between the amount of product that is theorized to be created, and what actually will be created. *The amount of a compound produced during experimentation is the actual yield*, and varies depending on the skill of the chemist and the quality of reactants used. If a chemist isn't meticulous in recording data, using equipment, and handling  materials, error will begin to affect the yield in the reaction. Similarly, if the reactants aren't of high quality, then the rate at which they are assumed to react with other compounds will be different than what's expected. The error between the actual and theoretical yield is noted as the *percent yield* of a reaction, and is defined as <span class="equation" data-expr="{\text{Actual Yield} \over \text{Theoretical Yield}} \times 100"></span>.

### In Closing
This blog post should have given you a basic overview of what stoichiometry is and how it's used in chemistry and in various other applications. You should have an understanding of how to derive conversion ratios from the equation you're working with, and how to perform stoichiometric conversions. Furthermore, you should be familiar with what a limiting and excess reactant is and how to determine what they are in a reaction, as well as how to use the limiting reactant to calculate the theoretical yield of a product. 

*In the second part of this series, I'll discuss the process I took when creating the [Stoichiometry Module](/chemistry-solver/stoichiometry/), and will touch upon how I implemented it, the challenges I was presented with during development, and what I did to overcome them*.

{% include katex_render.html %}
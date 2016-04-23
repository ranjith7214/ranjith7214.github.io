---
title: "Unit Conversion"
permalink: /chemistry-solver/unit-conversion/
---
![Unit Converter](/images/portfolio/chemistry-solver/unit-converter.png){: .align-center}

{% include toc %}

### Overview
The Unit Conversion tool provides the functionality to convert between units of the same conversion type, such as length to length and energy to energy. The tool provides immediate feedback as you change the text within either of the text boxes, as well as when units are changed between the initial and resulting values. There are a variety of conversion types supplied with the tool, and more can be added at the users discretion. By default, the supplied conversion types are ones potentially applicable to chemistry.

### Usage
For the Unit Conversion tool to perform any conversions, the conversion type and the units of the initial and desired values must first be selected. The conversion type is chosen from the large combo box at the top of the window.

![Unit Converter](/images/portfolio/chemistry-solver/unit-converter-type-selection.png){: .align-center}

The units of the initial and desired values are selected by changing the combo boxes on both sides of the '=' sign, to the desired values. The units on both sides of the equation are exactly the same, and changes when the conversion type is changed.

![Unit Converter](/images/portfolio/chemistry-solver/unit-converter-unit-selection.png){: .align-center}

The '=' sign signifies that the values on both side are equivalent at all times, and so modifying the values in the text boxes on either side of the equation will cause a resulting change on the opposite side to ensure equality. In addition, as values are changed, the resulting change will happen immediately.

### Adding Custom Units
To add custom units, or modify exisiting units, the 'UnitConversion.csv' file must be edited. The conversion file can be found in the '\data' folder.  This file is the data file containing all of the unit conversion information, which is stored as a series of tables followed by an empty row.

A conversion table provides the functionality to convert between units found within it, and must be formatted correctly in order for it to be read by the program. In the upper left hand corner of the table, the type of conversion the table performs is listed. Every cell directly below the upper left hand corner will contain a single, unique, unit for every unit the table provides a conversion for. The rows directly to the right of the upper left hand corner will contain the transposed column of units previously mentioned. The table is read from left to right, such that 1 of the unit listed in the unit column is equal to x of the unit in the unit row.

![Conversion Table Format](/images/portfolio/chemistry-solver/conversion-table-setup.png){: .align-center}

Consequently, this creates a diagonal of 1's going from top left to bottom right for conversions between units of the same type, and also separates the table into upper and lower triangles. The upper triangle, diagonal included, is the only information that needs to be filled out. Information in the lower triangle is the inverse of the transposed value in the upper triangle, and is calculated by the program automatically during run time. For example, a table that provides conversion information for time with the units: nanosecond, microsecond, milisecond, and second, would be formatted as follows:

![Conversion Table Format](/images/portfolio/chemistry-solver/conversion-table-completed.png){: .align-center}

{: .notice--warning}
**Be careful!** Editing the 'UnitConversion.csv' file can be dangerous as the file is required for the Unit Conversion tool to run correctly. If the file is ever undesireably changed, a new copy can be obtained from [here](https://github.com/Hoshiningen/Chemistry-Solver/blob/master/Chemistry-Solver/Chemistry-Solver/data/UnitConversion.csv).
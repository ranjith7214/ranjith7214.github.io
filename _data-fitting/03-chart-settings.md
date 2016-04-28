---
title: "Chart Settings"
permalink: /data-fitting/chart-settings/
---
![Chart Settings](/images/portfolio/data-fitting/chart-settings-gui.png){: .align-center}
{% include toc %}

### Overview
The Chart Settings tab is where the user can customize the appearance of their chart and create polynomial fits for their data. The user can add a title and axis labels, customize point and background appearances, and preview all their changes as they're made in the chart preview section.

### Chart Labels
To add a title to the x and y axis, and the chart, the user must navigate to the Chart Labels section and type in the names they wish for each respective section. As the user types in information, the Chart Preview will update immediately to reflect those changes.

![Chart Labels](/images/portfolio/data-fitting/chart-settings-with-labels.png){: .align-center}

### Point Appearance
The user has a variety of options for changing the appearance of points, which include the color, shape, and size of the point. To change the point color, the user has two options. They can select a color from the predefined list, or create a custom color by clicking the 'custom' button.

* The point sizes the user can choose from range from sizes 3 - 10.
* For a list of preset colors the user can choose from, look [here](https://msdn.microsoft.com/en-us/library/system.drawing.color_properties(v=vs.110).aspx).
* A list of point shapes are [here](https://msdn.microsoft.com/en-us/library/system.web.ui.datavisualization.charting.markerstyle(v=vs.110).aspx). 

![Point Customization](/images/portfolio/data-fitting/chart-settings-with-point-customization.png){: .align-center}

### Background Appearance
The background appearance of the chart can be changed in many ways, by choosing the background style, and the color(s) the styles use. The color options available to the user are the same as what's available in the point customization, which include predefined and custom colors. 

For background styles, there are three options to choose from: solid color, gradient, and hatch. A solid color background uses whatever color selection the user chose, and applies it to the entire plot area. A gradient requires two colors, and for the user to choose what type of gradient to apply. The hatch style requires one color, and a hatch style selection. For the gradient and hatch background styles, the respective types will be populated into a combo box underneath the 'Back Style' radio buttons. This combo box becomes active when the 'Solid' option is not selected.

* For a list of available gradient styles, look [here](https://msdn.microsoft.com/en-us/library/system.windows.forms.datavisualization.charting.gradientstyle(v=vs.110).aspx).
* For a list of available hatch styles, look [here](https://msdn.microsoft.com/en-us/library/system.windows.forms.datavisualization.charting.charthatchstyle(v=vs.110).aspx).

![Background Customization](/images/portfolio/data-fitting/chart-settings-with-background-customization.png){: .align-center}

### Regression
The type of regression that's currently in the application is polynomial regression, but there might be more options available in the future. In order to perform regression on a set of data, move the slider in the regression section to change the degree of the resulting polynomial. As the degree changes, the curve will be plotted on the Preview Chart to show the user how well it fits the their data. For fit validation, various statistics and a residuals chart are presented in the next tab, 'Data Visualization.'

![Chart Settings](/images/portfolio/data-fitting/chart-settings-regression.png){: .align-center}

Polynomials are fit through the least squares method, which is provided by the C# math library, [Math.Net Numerics](http://numerics.mathdotnet.com/).

### Resetting Chart Customization
To reset all customization, and regression values back to defaults, press the 'Reset' button at the bottom left portion of the window.

---
layout: post
title: The Worst Chart Ever
---
I spend a great deal of my day thinking about how to accurately and honestly present data, because it's my job. To do my job well I research best practices, network with other people in the field, and look at a lot of charts.

Sometimes in my research I find something that strikes me. Well today I found the most striking chart I have ever seen. I call it the *worst chart ever*.

{% include image.html url="http://assets.bwbx.io/images/i10RvPmdxQsI/v1/-1x-1.png" description="the worst chart ever" %}
[Source: Bloomberg Businessweek](http://www.bloomberg.com/news/articles/2015-10-27/what-killed-america-s-climate-saving-nuclear-renaissance-)

There are two main reasons this is the the worst chart ever.

##It's a "Half Pie, Pie Chart"

Seriously what the hell? Who thinks up a "Half Pie, Pie Chart"? There are "gauge charts", but those are for presenting one thing falling in a range (guage charts are not recommend for displaying values falling in ranges). I tried figuring out how to make a "half pie chart" and the only way you can do it in excel is with a [tricky hack](http://www.extendoffice.com/documents/excel/2016-excel-half-pie-chart.html). Pro-Tip, if you have to hack a chart together, it's probably not the best chart for the situation.

*Worst of all* the "half pie, pie chart" is incredibly misleading. Anyone who has ever seen a pie chart knows that all the pieces of the pie add up to one whole pie. If you use the visual of "pieces of a pie" but not the well understood concept of a whole you're deliberately confusing readers. You know force your reader to read the data label and once that happens you might as well have used a table.

(All the numbers don't even add up to 100%)

##Why is there a X-Axis?

The only thing crazier than the "half pie, pie chart" is that the creator included a X-Axis on on the bottom. There isn't even a scale with it, they just physically ordered the slices of the "half pie" so that they line up from largest to smallest on "greenhouse gas emissions per kwh". This gives you no relational information about how far apart the various energy generating methods are in greenhouse gas emissions. I consider this X-Axis to be intentionally misleading.

##How to do this chart correctly.

*Where the U.S. gets it's electricity*

|Energy Source|Percent of Total U.S. Electricity Produced|Greenhouse Gas Emissions per kwh|
|---|---|---|
| Manufactured and Waste Gas | 0.3% | 10|
| Coal | 39% | 9|
| Petroleum | 1% | 8|
|Natural Gas | 28% |7|
| Biomass | 1% |6|
| Geothermal | 0.4%|5|
| Solar |0.2%|4|
| Hydro | 6% |3|
| Nuclear | 19% |2|
| Wind | 4% |1|

See how much better a table would have been? Much easier to understand and read. If I had the emissions data it would have been ever better.

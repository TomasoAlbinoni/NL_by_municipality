# The Netherlands by Municipality (2015)

## Summary

This D3 data visualization shows how Dutch cities have a younger population with smaller average households than rural areas. Both geometrical and numerical data are from a .shp file downloaded from Statistics Netherlands (Centraal Bureau voor de Statistiek). The source file was converted to geojson using ogr2ogr and the polygons were simplified using mapshaper.org.

## Design

When the page first loads, all municipalities are white. In order to prevent bodies of water from appearing like municipalities, I used a gray background.

For the one categorical variable &ndash; top age group &ndash; I used the following color scheme: light green, as in new foliage, for children up to 14 years, and the fall colors yellow, orange and dark red for increasingly older folks. Or, one could think of these colors as representing the sequence: green lemonade - beer - scotch - port wine. The oldest age group, having no or only gray hair, is represented by the color gray.

For the continuous variables, I used a scale from light blue, representing low values, to bright red, representing high values. For population density, % unmarried inhabitants and % one-person households, the resulting patterns are very similar. Since high percentages of unmarried inhabitants and one-person households lead to a low average household size, the color pattern is roughly inverted for the average household size map. Because of this, and because of the fact that one person (backfeeder 3) found the hues on the household size map too similar, I experimented with different color schemes for the average household size map, and settled on pale yellow to dark blue. In addition, I added intermediate values to the legend.

Backfeeder 1 suggested that I add proper attribution, which I promply did.

Backfeeder 2 gave some fascinating suggestions: to put maps showing different metrics side by side, and to combine data in some mathemetical way to highlight relationships. While I agree it would be interesting to see multiple metrics at the same time, I believe the power of having just one map lies in being able to switch between metrics and seeing municipalities change color in place. As for combining data, I have given it some thought, but failed to come up with a way to do this without obscuring the message I want the visualization to convey. For example, if I color the municipalities based on the ratio of population density / % unmarried inhabitants, perhaps after rescaling the denominator to get the least possible variation, I will end up drawing attention to the outliers instead of the pattern I want to show.

## Feedback

### Backfeeder 1:

**What do you notice in the visualization?**

- *That Urk and Laren stand out.*
- *The big cities have high population densities and high numbers of single-person households. For some reason the islands also have many single-person households.*
- *Rural areas have a higher proportion of married people.*

**What questions do you have about the data?**

- *What makes Urk and Laren so different?*
- *What is different about the places with 25-44 top age group?*

**What relationships do you notice?**

*Municipalities with a high population density tend to have a younger population with a relatively high number of unmarried people and a smaller average household size.*

**What do you think is the main takeaway from this visualization?**

*That the cities and university towns have a younger population.*

**Is there something you don’t understand in the graphic?**

*Where did you find the data?*

### Backfeeder 2:

**What do you think is the main takeaway from this visualization?**

*That the most densely populated areas have the smallest household sizes (except for Urk).*

**Do you think the visualization is effective?**

*No, those maps should be side by side. It's just that I'm highly trained at reading maps like this, so I immediately noticed the relationship. Also, it would be more interesting with election results, and church membership. Oh, the visualization should highlight a relationship or pattern in the data? In that case you should combine the data in some mathematical way, like dividing or multiplying or something like that.*

**Do you like the use of color?**

*Yes, I'm not color blind, so no problems with the choice of color.*

### Backfeeder 3:

**What do you notice in the visualization?**

*In big cities there are younger people and more unmarried people, more one-person households, and the average household size is smaller.*

**What would you change?**

*The hue differences in the average household size map are too small and make it difficult to estimate which color stands for which value.*

## Resources

- https://www.cbs.nl/nl-nl/dossier/nederland-regionaal/geografische%20data/wijk-en-buurtkaart-2015
- https://ben.balter.com/2013/06/26/how-to-convert-shapefiles-to-geojson-for-use-on-github/
- http://mapshaper.org/
- http://www.jeromecukier.net/blog/2011/08/11/d3-scales-and-color/
- https://gist.github.com/biovisualize/1016860
- http://www.d3noob.org/2013/01/adding-tooltips-to-d3js-graph.html
- https://stackoverflow.com/questions/2901102/how-to-print-a-number-with-commas-as-thousands-separators-in-javascript
- https://www.w3schools.com/cssref/css_colors_legal.asp
- https://github.com/d3/d3-scale
- https://stackoverflow.com/questions/27376295/getting-key-with-the-highest-value-from-object
- https://bl.ocks.org/zanarmstrong/0b6276e033142ce95f7f374e20f1c1a7
- https://stackoverflow.com/questions/20142951/how-to-set-the-background-color-of-a-d3-js-svg
- https://stackoverflow.com/questions/41396786/align-text-within-d3-svg
- https://stackoverflow.com/questions/22161624/how-to-render-svg-elements-with-crisp-edges-while-still-keeping-anti-aliasing
- https://stackoverflow.com/questions/3751520/how-to-generate-sequence-of-numbers-chars-in-javascript
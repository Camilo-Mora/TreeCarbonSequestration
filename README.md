# TreeCarbonSequestration
Simple java app that uses published equations to calculate the carbon sequestered by a tree

Summary: Climate change is truly a terrifying thing. By increasing the amount of CO2 in the atmosphere, we are increasing the temperature of the planet, which in turn is increasing drought, heatwaves and wildfires in some areas, and extreme precipitation and floods in others. Add sea-level rise to the mixture and you get the picture. All these climatic hazards have the capacity to make humanity sicker, hungrier, thirsty, homeless, poor, and unsafe.

Remarkably, all these disasters can be traced back to a simple unbalance of the Earth's atmospheric CO2 concentration: we produce more CO2 than it can be removed. From this perspective, averting the threat of climate change will require some degree of luck discovering new types of "green"/zero-emissions energy, or a considerable improvement of existing methods that capture carbon emissions; and trees, may be just what we need. Trough photosynthesis, trees break some of the “nasty” CO2 we produce into carbon, which they store, and oxygen, which they release: a win-win.

This app has been developed using several published equations to estimate the amount of CO2 that can be stored as carbon in a tree.

Background: Firsts, we need to start by understanding "allometric" relationships. Basically, as any individual grows, parts of its body will most likely correlate with other body parts; like the length of your arms relates to the length of your legs. Thus, by knowing a single attribute of the individual, you can predict other attributes of that individual.

In the case of trees, Chave et al (2001) collected data from 12 different studies that predicted tree above ground biomass by simply knowing the tree Diameter at Breast Height or so called "DBH". In their article, they reported 12 mathematical equations, which I display below:


Above ground tree mass predictions based on tree diameter.
Using multi-model averaging from the studies reported by Chave et al (2001), then one can predict above ground dry body mass as:

Body Mass =0.0998 * DBH^2.5445

In turn, Niklas & Enquist (2001) found that one can use tree body mass to predict their growth rate, as:

Growth Rate =0.208 * Body Mass^0.763

By knowing the weight of a tree, and their growth rate, one could predict the weight of the tree at different time intervals. Just like a pediatrician is able to predict the approximate weight of a child at different ages.

Until now, all weight calculations are for the part of the tree that one sees above ground. It turns out, that Cairns et al (1997) found that below ground biomass is about 24% the weight of the tree above ground.

So we need to multiply the tree mass from Chave et al . (2001) by 1.24. That is, the weight of the tree above ground, plus the 0.24 fraction below ground.

Up to this moment, we have been able to calculate the weight of the tree (below and above ground), but not all that weight is carbon.

As one may expect, the tissue of the tree has many other chemical elements. Lucky for us, Kirby & Potvin (2007) found that 47% of the dry weight of a tree is carbon. So, we can simply multiply our estimated weight of a tree by 0.47 to know the approximated carbon in the given tree.

Ok, we now have a good approximation to the carbon stored in a tree. But carbon is different from CO2. CO2 has two molecules of oxygen, so it is heavier. The molecular weight of carbon is 12.0107, while that of oxygen is 15.999. So the molecular weight of CO2 is 44.0087 or 3.6663 times heavier that carbon alone.

So to estimate the CO2 that could be taken from the atmosphere by a tree, one needs to multiply the weight of the carbon in the tree by 3.6663.

The result is a time series projection of the CO2 likely to be removed by a tree from the atmosphere and stored in its body by simply knowing the diameter of the tree.




Tree CO2 sequestration calculator

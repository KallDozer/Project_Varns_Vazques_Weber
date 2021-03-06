> * Group Name: The Quarter Dirty Dozen
> * Group participants names: Brian Varns, Gabrielle Vasquez, Matthias Weber
> * Project Title: City-Traffic-Planning

Our project is dealing with the issue of city-planning and in special measures that can decrease the traffic in certain areas (e.g. by adding new roads). We decided to take the example of the Autobahn (A10) that is surrounding Berlin as our model. Once we create this model we want to analyze the resulting traffic data (including hotspots) to identify where traffic is at its worst. Once we determine these spots we will add additional highways to determine if this will alleviate traffic or cause additional hotspots to arise in different areas.

<p align="center"><img src="../images/Berlin_road_map.png" width="700"></p>
<p align="center">Figure 1: Map of A10</p>


## General Introduction

Congestion on any modern highway greatly reduces our quality of life and steals our valuable free time.  There have been many proposed solutions to fix this issue, such as autonomous vehicles, connected vehicles, ramp metering, and active traffic monitoring.  (Dvosrsky, 2014)  These technologies will allow vehicles to move in a more efficient manner on roadways and move them along the most efficient path to their destination.  However, these technologies are years, if no decades away from realization and the cost of implementation would cost hundreds of millions of dollars.  Are these new technology really the solution to this issue or can some common sense could put an end to traffic congestion? 

## Problem Statement: 

A 2010 RAND study noted that traffic congestion is created by an imbalance in the supply of and demand for road space.  This, coupled with the fact that we have limited options to build ourselves new roads that bypass these issues, is creating traffic jams in large cities on a scale never seen before.  (Sorensen, et al. 2010)  Autobahns located in Germany in 2017 experienced: (Mcintosh, 2018)

+ Traffic jams increased by 4 percent in 2017 or by 723,000 more than 2016.

+ The length of the jams in 2017 totalled 1,448,000 kilometers (899,745 miles), a rise of 5 percent.

+ Road users were stuck in traffic for a total of 457,000 hours, a rise of 9 percent.

## Motivation:

Traffic congestion on the Autobahn is amongst the worst in the world.  This congestion has many issues that are similar amongst many different roadways in the world and has taken a toll on driving safety, air quality, and quality of life for its citizens. Future technologies are being created to ease this issue, but are many years away from being effectively implemented.  If a simple solution can be found, by adding key roadways, it will save countries millions of dollars and allow for further research to identify how to alleviate traffic congestion in other cities. 

## Proposed Solution:

To complete this experiment the researchers will conduct a study to identify a strategy to reduce traffic congestion that could be implemented in different cities across the world.  For the purpose of this experiment we will use the Autobahn 10 in Germany.  The researchers reviewed literature related to congestion and typical driving patterns of humans, examined existing data for traffic flow on and off of the Autobahn, and will analyze historical hotspots for traffic congestion.  With this data we will create a model of the Autobahn, of vehicles (cars and trucks), and of drivers.  Once created we will run this model to identify key hotspots on the Autobahn and develop simple bypasses for alleviating this congestion.

## Contributions:
+ Our research should present a resilient approach/guidance for city-planner to fight the common traffic problems of congestion
+ Our research will be replicable to allow large cities to analyze their traffic congestion.
+ Our code and models will be open sourced to be used by any individual or organization.

## The Model
Our created model is a good abstraction of the given problem, due to the fact that we tried to focus on the core elements “Road” and “Vehicle”. The element “Road” is consisting out of “Lanes” and several “ON/Off-sections”. Whereas the element “Vehicle”, that will interact with the previous mentioned parts, is consisting out of the elements “Car” and “Truck”.  The vehicle component will have the ability for freedom of movement, meaning they will have the ability to enter and exit freely to get to their destination; the "Vehicle" will operate simliarly to typical, human driving behaviors in that the "Vehicle" driving behavior will be more predictiable than humans.  This will be part of their programing and is the reason we left out “People” from the experiment.  

![Structural_Diagram](../images/Structural_Diagram.PNG)
<p align="center">Figure 2: Object Diagram</p>


![Behavioral_Diagram](../images/Behavioral_Diagram.PNG) 
<p align="center">Figure 3: Behavior Diagram</p>

We identified these elements, due to the following requirements:
+ The simulation should mimic the traffic-situation on the A10, that is surrounding Berlin (Germany)
+ The simulation-model must pay attention to the dimension of the corresponding and used roads
+ The model should just pay attention to the major in- and outflow areas
+ The position of the in- and outflow areas should be based on their counterparts in the real world
+ The simulation must handle 2 different kind of vehicles (car and truck) 
+ The simulation must include car following behaviour
+ As a data source the simulation must use appropriate collected and realistical data
+ The simulation should show whether infrastructural improvements can significantly reduce congestions or not


## Fundamental Questions
In the first part of our project, we want to clarify if the traffic situation can be adequately mapped, including the existing restrictions on the traffic flow.  Our primary question here focuses on determining the peak traffic times and locations of congestion.  Our primary question, “Can we reduce traffic through common sense city planning”, will then be tested through our experiment.  We will do this by identifying if infrastructural measures can reduce traffic congestion (by adding one or more streets of the same type) or even eliminate them. Or whether the restrictions take place in another area and therefore other suitable measures need to be researched.

## Expected Results

For our two fundamental questions we expect for first identify traffic congestion during peak times.  We expect these conjestion areas to align with heavy traffic flow from the busiest on and off ramps identified in Figure 8.  Once identified we will attempt to allieviate this traffic through addition or subtraction of roads (on and off ramps, highways).  Below are some proposed solutions to reduced traffic congestions bz adding routes in along different parts of the A10:4

<br><u>1 road from North to South:</u></br>
<p align="left"><img src="../images/Berlin_N_S.png" width="400"></p>
Figure 4: Expected Results (v1)


<br><u>1 road from West to East:</u></br>
<p align="left"><img src="../images/Berlin_W_E.png" width="400"></p>
Figure 5: Expected Results (v2)


<br>Mix from both previous attempts:</br>
<p align="left"><img src="../images/Berlin_BOTH.png" width="400"></p>
Figure 6: Expected Results (v3)


## Research Methods

**Models

For this simulated experiment, we will be developing simulated cars and agents to mimic the common driving behaviors of everyday human, civilians. The sample size that we have implemented within the simulation was based on real and synthetic data that we have derived  from www.bast.de and http://www.autobahnatlas-online.de/A10.htm.


**Experimental Protocol 

For the purpose of this project, we will be implementing an agent-based simulation using AnyLogic to simulate our experiment. We plan on running our simulation 10 times to ensure our data accurate to the best of its capabilities. 

**Experimental Paradigm 
 
In setting up the simulation, we have ensured that the agents developed best mimicked the driving behaviors of humans by having them have the possibility of committing am rear-end accident. These agents were developed based from a comparison study conducted by McDonald, Curry,  Kandadai, Sommers, & Winston (2014). They found after looking at data comparing across ages and genders that the most common crash incident to occur among all groups were rear-ended accidents. Such accidents will be simulated into a design to mimic one of the possible ways that highway traffic could occur. 
Overall, the simulation will be developed in such a way to accurately mimic the typical behaviors we see in human driving behaviors and functions of motor vehicles.
 

## Data

The below image includes the 14 identified On/Off-sections, with the amount of vehicles per day for the road-section between these areas.  We will use this data to determine how many cars will enter and exit the points of the A10 and identify where and when traffic congestion occurs.

<p align="center"><img src="../images/Ramps_Traffic.png" width="800"></p>
<p align="center">Figure 7: On/Off-sections</p>

The length of the A10 is 195 km in total and the locations for the On/Off-sections are located at the following autobahn-positions:

![Berlin_Ramps_Positions](../images/Berlin_Ramps_Positions.png)
<p align="center">Figure 8: A10 Real Data</p>

The A10 consists of three lanes of traffic heading in both directions.  There is one exception, which is between point 9 and point 14 where the A10 offers two lanes for each direction.


## References

Dvorsky, G. (2014). Here’s how to get rid of traffic jams.  Found at: https://io9.gizmodo.com/could-new-technologies-make-traffic-jams-a-thing-of-the-1602353172

McDonald, C. C., Curry, A. E., Kandadai, V., Sommers, M. S., & Winston, F. K. (2014). Comparison of teen and adult driver crash scenarios in a nationally representative sample of serious crashes. Accident Analysis & Prevention, 72, 302-308.

Navigation und Service. (2018). Retrieved February 22, 2018, from http://www.bast.de/DE/Verkehrstechnik/Fachthemen/v2-verkehrszaehlung/Aktuell/zaehl_aktuell_node.html?cms_map=1&cms_filter=true&cms_jahr=Jawe2016&cms_land=12&cms_strTyp=&cms_str=&cms_dtvKfz=&cms_dtvSv= 

Mcintosh J. (2018).  German traffic jams piled on misery for drivers in 2017.  Found at:http://www.dw.com/en/german-traffic-jams-piled-on-misery-for-drivers-in-2017/a-42268383

Scholl, P. (2018). Autobahnatlas. Retrieved February 22, 2018, from http://www.autobahnatlas-online.de/A10.htm
Sorensen, P., Wachs, M., Daehner, E., Kofner, A., Ecola, L., Hanson, M., Yoh, A., Light, T., Griffin, J. (2010). Reducing Traffic Congestion in Los Angeles. Found at: https://www.rand.org/pubs/research_briefs/RB9385.html



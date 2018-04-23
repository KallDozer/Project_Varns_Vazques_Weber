# IDS6145(SimTech 2018) - Research Plan

> * Group Name: The Quarter Dirty Dozen
> * Group participants names: Brian Varns, Gabrielle Vasquez, Matthias Weber
> * Project Title: City-Traffic-Planning

Our project is dealing with the issue of city-planning and in special measures that can decrease the traffic in certain areas (e.g. by adding new roads). We decided to take the example of the Autobahn (A10) that is surrounding Berlin as our model. Once we create this model we want to analyze the resulting traffic data (including hotspots) to identify where traffic is at its worst. Once we determine these spots we will add additional highways to determine if this will alleviate traffic or cause additional hotspots to arise in different areas.

<p align="center"><img src="/images/Berlin_road_map.png" width="700"></p>
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

![Structural_Diagram](/images/Structural_Diagram.PNG)
<p align="center">Figure 2: Object Diagram</p>


![Behavioral_Diagram](/images/Behavioral_Diagram.PNG) 
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
<p align="left"><img src="/images/Berlin_N_S.png" width="400"></p>
Figure 4: Expected Results (v1)


<br><u>1 road from West to East:</u></br>
<p align="left"><img src="/images/Berlin_W_E.png" width="400"></p>
Figure 5: Expected Results (v2)


<br>Mix from both previous attempts:</br>
<p align="left"><img src="/images/Berlin_BOTH.png" width="400"></p>
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

<p align="center"><img src="/images/Ramps_Traffic.png" width="800"></p>
<p align="center">Figure 7: On/Off-sections</p>

The length of the A10 is 195 km in total and the locations for the On/Off-sections are located at the following autobahn-positions:

![Berlin_Ramps_Positions](/images/Berlin_Ramps_Positions.png)
<p align="center">Figure 8: A10 Real Data</p>

The A10 consists of three lanes of traffic heading in both directions.  There is one exception, which is between point 9 and point 14 where the A10 offers two lanes for each direction.

## Discussion

Our results indicate that the Autobahn 10 should be a government controlled road, similar to the system that is implemented in the Florida road system (i.e. the Fast Pass system). With such a system, we would suggest charging taxes to the citizens of Germany to allow them to use the bypass will decrease traffic on these roads; we assume that only a certain percentage of drivers will pay the tax to use this bypass allowing the other roads to not become overcrowded. 

We have chosen to use an exponetial distrubtion to see what effect it has on arrival rate on the cars in this model. The purpose of using the Exponential distribution is for its ability to represent the time between random occurrences, such as the time between arrivals at a specific location in a queuing model, in our experiment, eliminating traffic on the Autobarn 10 in Germany. It has also been used to represent the services times of a specific operation. Further, it serves as an explicit manner in which the time dependence on noise may be treated. One issue we have came across was that we cannot apply an exponential distribution. For each on and off ramp, we have set the probabilities so that each car has the probability of using that specific

We did not discover any difference in effect size after multiple runs of our simulation. We found that no matter the number of times we run the simulation, we would see similar results. This causes an issue with validity of the model itself, which then leads us to believe there are issues with our simulation that we unable to determine. We have also saw issues in the behaviors of the cars themselves. Collisions were occuring in areas that were causing the cars to be backed up, eventually causing the cars on the Autobahn 10 to stop moving. The cars that tend to be affected by these collision issues are those around exit 10 and 13. 

(insert image here) 

Figures 1 & 2: The above images depicts traffic on exits 10 and 13. All intersections were built identical to one another, however, we have ran into issues which traffic would build up on these exits. 


We have put in the efforts to replicate each exit to eliminate the issues of collisions and traffic, however, these exits tend to be affected no matter what we decide to implement (elongating roads, adding exits prior to other exits, etc.). Due to the capabilities of AnyLogic’s Learner Edition, we are limited to the functionalities that we could implement in this expeirment. There is a possilbity that this problem is occuring because of AnyLogic's ability to handle these types of problems; modeling such a problem is too large and requires too much processing power from AnyLogic. We were also limited to amount of code we could use for our model. The AnyLogic' Learner Edition limoits users to 200 boxes for their code; our base model code is alone over 100 boxes. Due to this limitation, we were unable to properly build our model to fix the complications that we have encountered. This issue had also prevented us from further testimng with the direction of the roads; this particular model needed more than 200 boxes worth of code which AnyLogic did not allow us to do. This effected pur testing with a road going from North to South. 


Due to complications from the build of our simulation, we have came to the possibility of two reasons as to why this would occur: 1) the AnyLogic program was not built to handle a simulation of this type and another program should be used to model this issue or 2) adjustments to the construction of the Autobahn 10 must be made. AnyLogic is a multimethod simulation modeling tool meant to model discrete, agent-based, and system dynamics. Given this, this makes AnyLogic ideal for investigating systems in the domains of healthcare, marketing, supply and demand, and particularly for road traffic. We had chosen to model and simulate our problem with the AnyLogic system because of its ability to model the characteristics of road traffic (traffic jams, cars entering and exiting from exits and roads, etc.). Working more with this system, we started seeing issues with our simulation in that we had collisions occurring in areas of the Autobahn 10; cars were getting stuck on the exits. We discovered that the methods we were going about with trying to solve this issue were not working, which then leads us to believe that the AnyLogic system was not ideal for such a model. 
The student edition only allows users to run models for only an hour. This limits us to use real world data to accurately simulate problems that run for a minmiumn of 24 hours. We also assume that the AnyLogic Student Edition lacks processing power in that it is unable to handle the amount of variables, paramters, agents, etc. that we have included within our model - is it not built for such high, processing power models that contain high values. It has forced us to manipulate the numbers in which to change the model's behavior. This has disabled us to represent the behaviors of cars in an applied setting; we cannot account for ecological validity. The behaviors of our agents are not representative of what we would see on the Autobahn 10 or any other highway.

## Future Work

For future implementation, we would go about with running our model in an edition of AnyLogic that is not the student package. As stated in the previous section, the student edition has limit in that we were not able to run our model for the time necessary to have accruate results. We would want to utlaize the features in the other AnyLogic editions in hopes that we can run our model properly and get results that would replicate what we would see in an applied setting. Further, we believe that we will not be as limited in what we can do with our model and run for a full day versus the one hour maxmium from AnyLogic. 
With other simulations editiors and languages out there to our deposial, we would possibly want to take advanatge of these systems. We are particularly interested in using a gaming engine to help visualize and simulate our model that was orginally built in this experiment; we would lean towards using Unreal Engine to run this simulation. Unreal Engine has a visualization coding system that allows for its user and developers to "code" while visualizing how componenets (agents, objects, etc.) intertact with one another. If we were allowed the option to look at how our agents were interacting with their environment and other components in the simulation, we may have been able to troubleshoot where and why collisions were occurring the way they were in our experiment. Unreal Engine also has the processing capability to run dynamic, complex systems such as our model. With these considerations, we believe that we will then be able to also account for ecological validity along with having the processing power to properly test our simulation. Replication of the Autobahn 10 will be critical for future experimentation of this model and to be successful in doing so, we would then need to look into the possbility of importing real world data into these types of systems. Currently, there is no method of importing real world data into the Unreal Engine. Unreal Engine does allow the capability to "hard code" (code by hand certain functionalities) and we would be interested in knowing the methods required to implement these methods for future experimentation. Overall, future work should focus on finding a system that can handle the processing needs of a complex, dynamic model and look into methods of importing real world data into these systems to then replicate the environments that were are looking to solve these problems for. 


## References

Dvorsky, G. (2014). Here’s how to get rid of traffic jams.  Found at: https://io9.gizmodo.com/could-new-technologies-make-traffic-jams-a-thing-of-the-1602353172

McDonald, C. C., Curry, A. E., Kandadai, V., Sommers, M. S., & Winston, F. K. (2014). Comparison of teen and adult driver crash scenarios in a nationally representative sample of serious crashes. Accident Analysis & Prevention, 72, 302-308.

Navigation und Service. (2018). Retrieved February 22, 2018, from http://www.bast.de/DE/Verkehrstechnik/Fachthemen/v2-verkehrszaehlung/Aktuell/zaehl_aktuell_node.html?cms_map=1&cms_filter=true&cms_jahr=Jawe2016&cms_land=12&cms_strTyp=&cms_str=&cms_dtvKfz=&cms_dtvSv= 

Mcintosh J. (2018).  German traffic jams piled on misery for drivers in 2017.  Found at:http://www.dw.com/en/german-traffic-jams-piled-on-misery-for-drivers-in-2017/a-42268383

Scholl, P. (2018). Autobahnatlas. Retrieved February 22, 2018, from http://www.autobahnatlas-online.de/A10.htm
Sorensen, P., Wachs, M., Daehner, E., Kofner, A., Ecola, L., Hanson, M., Yoh, A., Light, T., Griffin, J. (2010). Reducing Traffic Congestion in Los Angeles. Found at: https://www.rand.org/pubs/research_briefs/RB9385.html



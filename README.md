# FACTS_placement_w_load_share
FACTS_placement_w_load_share is a tool for studying FACTS placement attending to load share. A STATCOM-type FACTS device is implemented in the power system simulator and load share is changed among 3 demand zones iteratively. 

Power system stability indices are calculated and different charts may be created. 

This tool is implemented using Python 2.7.13 so as to use PSS-E 34 as a simulation platform.

# Configuration files

In "FACTS_placement_study_config.txt" the FACTS placement study must be configurated. Name and path of the file containing power system data must be provided, as well as configuration data for power flow calculation and FACTS device configuration.

In "demand_scenarios_config.txt" demand zones have to be defined.

# FACTS placement procedure

For each demand scenario, PV analysis is performed. Later on, the FACTS device is implemented in every one of the available locations specified in "FACTS_placement_study_config.txt" and a PV analysis is performed. Finally, power system stability indices are calculated.

# Demand scenarios creation

First, power system nodes have to be split into 3 "demand zones" (this has to be specified in "demand_scenarios_config.txt"). Once the program is initiated, total demand power is calculated and demand scenarios are created. In order to do so, total demand power is distributed among the different demand zones iteratively by 5%. Hence, total demand is constant, while load share among demand zones difers from one demand scenario to another. Within a demand zone, the asigned power is distributed among its load nodes according to their initial power.

# Plotting

So as to plot results, "FACTS_placement-demand-variation.py" needs to be properly executed and different objects files need to be created. Then, using "representation.py" one can plot different results.


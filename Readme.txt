
There are 60 instances to evaluate the problem of timely delivery of medical items by using a fleet of drones. For more information read:

There are 60 data files. Each instance include a set of 20 providers(supply point), 30 candidate platforms(drone charging stations) and 25 clinics(demand points). The problem is to optimally select a set of platforms and concurrently schedule and sequence drone trips such that all the demand points are met within a specific operational time. The objective is to minimize the total completion time.

The instances are divided into two class of configurations. Directory ClassM includes 30 instances representing Mixed Configuration instances where providers, platforms and clinics are randomly distributed over an area of 80km X 80km. Each instance of Mixed class is denoted by M. Directory ClassC includes 30 instances where the providers and clinics are clustered separately. We refer to this class of instances as Clustered Configuration instances and denote them by C.

We assume a drone can carry up to two loads, e.g., 2 kg, and is equipped with one built-in battery. For each instance, we considered two different possible operational scenarios:

Scenario (a): We assume drones are loaded with two loads of medical packages and are allowed to visit at most two charging platforms during each trip. For this scenario, imposing a smaller number of stops mostly resulted in infeasible solutions, so the results are not discussed.

Scenario (b): We assume that out of the two loads capacity, one load is assigned to medical packages and one to an additional battery (assuming an additional battery takes exactly one load) and up to one charging station can be visited. In this scenario, drones technically have two batteries, which gives them a longer range.

The input parameters are as follows:
for each clinic in clinics:
	demand = 2 packages

timeslot granularity = 15min, operational time= 4hrs, Drone battery capacity=700 Wh, additional battery: 300 Wh, frame weight=7kg, battery weight=1kg, lift_to_drag ratio of drone = 3

The format for each of these data files is;

number of providers
number of candidate platforms
number of clinics

for each provider in providers:
	x_coordinate y_coordinate
for each platform in platform:
	x_coordinate y_coordinate
for each clinic in clinics:
	x_coordinate y_coordinate

optimum solution to scenario(a)
for each q in (1,30):
	q ObjVal

optimum solution to scenario(b)
for each q in (1,30):
	q ObjVal

*(Note that we provided the solutions as far as increasing q improve the objective value. For example in case of M1 under scenario(a), we presented solutions up to q = 6, which means that for values of q>6, the objective value does not improve.)






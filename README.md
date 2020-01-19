# Vehicle Routing Problem

## -Summary
The project consists in designing and writing a working VBA program that heuristically solves a vehicle routing problem (VRP) 
using stochastic optimisation techniques. Specifically, the program will read in a problem instance from a file and then will 
produce a heuristic quality solution using descent-based methods and possibly more advanced optimisation techniques. It will 
also output information to the user during and after a run, including animated graphical output.

-----------------------------------------------------------------------------------------------------------------------------

## -Problem Specification
Every day a delivery firm is given a list of locations to make deliveries to. The delivery firm has a fleet of vehicles that start at the depot in the morning. Each individual vehicle leaves the depot, visits some of these locations in a given order and then returns to the depot. The firm is interested in minimising the total distance travelled by the vehicles while ensuring that its vehicles visit all the locations for deliveries during the day.

This routing problem can be stated more precisely as follows. We are given a single pair of coordinates specifying the location of the depot, together with n pairs of coordinates for deliveries. The number of available vehicles v is also specified (1 ≤ v ≤ n). The firm has as a rule that all drivers must be allocated m deliveries (locations) in a day, where m = n/v (i.e. for convenience, we always assume that n/v gives a whole number). The distance between any two locations (including the depot) is assumed to be measured on a straight line (i.e. as the Euclidean distance), similarly to the TSP example shown in class.

Particular problem instances are specified in text files as follows. Each text file starts with the depot coordinates. Then the next two numbers in the text file are numbers n and v, followed by the coordinates of each of the n locations for deliveries. Here is a baby-size example with n = 9, v = 3 (and therefore m = 9/3 = 3). The depot is at coordinates (3, 3), as given in the first line. All coordinates are integers.

       3	3
       9	3
       2	7
       4	4
       7	5
       2	5
       3	4
       1	1
       6	2
       6	1
       4	0

A candidate solution to this problem can be conveniently stored as a 2D array with v rows and m columns. Here the locations to visit that are assigned to vehicle i appear in row i in the given order for deliveries, i=1,2,…,v. For example, the following array S refers to the solution illustrated below (for the problem instance given above).


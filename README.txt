====================================================================
The MVA base is 100 MVA.

====================================================================
"branch.txt" is the branch data of the modified IEEE 118-bus system.
The first line of this file is the number of branches of the system.
The following part is the data of each branch and the data format is as follows.

     1            2                             3                              4          5         6                     7                          8         9
"From" bus    "To" bus    Branch type(0-transmission line, 1-transformer)    NO-USE    R(p.u.)   X(p.u.)    Y0(p.u.) or transformation ratio k    NO-USE    NO-USE

Note: Shunt elements are considered as branches that their "From" bus is identical to the "To" bus and their susceptance(p.u.) is stored in column 6.

====================================================================
"node.txt" is the bus data of the modified IEEE 118-bus system.
The first line is the number of buses of the system.
The following part is the data of each bus and the data format is as follows.

   1          2                       3                         4             5           6
Bus No.    Bus No.    Bus type(0-PQ, 1-PV, 2-slack)    Voltage magnitude    Angle    Base voltage 

====================================================================
"data.txt" is the measurement data of the modified IEEE 118-bus system.
The first line is the number of measurements.
The following part is the data of each measurements and the data format is as follows.

         1                     2              3        4                 5                         6              7        8
Measurement type 1    Measurement type 2    Bus i    Bus j    Measurement value(p.u.)    Standard deviation    NO-USE    NO-USE

Measurement type table:

Measurement type 1    Measurement type 2    Measurement type
        1                      1            Active power injected at bus i (p.u.) (transformer)
	1                      2            Reactive power injected at bus i (p.u.) (transformer) 
	2                      1            Active power injected at bus i (p.u.) (transmission line)
	2                      2            Reactive power injected at bus i (p.u.) (transmission line)
	3                      1            Active power injection (p.u.)
	3                      2            Reactive power injection (p.u.)
	3                      5            Voltage magnitude (p.u.)
	4                      1            Active power consumption (p.u.) of shunt element at bus i
	4                      2            Reactive power consumption (p.u.) of shunt element at bus i

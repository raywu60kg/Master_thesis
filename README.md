# Master_thesis
algorithm for finding optimal design

From OPTIMIZING TWO-LEVEL SUPERSATURATED DESIGNS USING SWARM INTELLIGENCE TECHNIQUES(2016) /n
and we upated it to deal with the multistratum designs.

1: Randomly generate a set of balanced (n1*n2)*(m1+m2) multistratum SSDs as initial particles
2: Evaluate objective function value of each SSD
3: Initialize the LB for all SSDs
4: Initialize the GB
5: while not converge do
6: For each SSD, perform the MIX operation
7: For each SSD, perform the MOVE operation
8: Evaluate objective function value of each SSD
9: Update the LB for all SSDs
10: Update the GB
11: end while

MIX operation:
MOVE operation:

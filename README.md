# Master_thesis
It is an algorithm for finding optimal design from OPTIMIZING TWO-LEVEL SUPERSATURATED DESIGNS USING SWARM INTELLIGENCE TECHNIQUES(2016)
and we upated it to deal with the multistratum designs.

## Algorithm
1.  Randomly generate a set of balanced (n1 x n2)(m1+m2) multistratum SSDs as initial particles  
2.  Evaluate objective function value of each SSD  
3.  Initialize the LB for all SSDs 
4.  Initialize the GB 
5.  while not converge do   
6.   For each SSD, perform the MIX operation     
7.   For each SSD, perform the MOVE operation  
8.   Evaluate objective function value of each SSD   
9.   Update the LB for all SSDs  
10.  Update the GB
11. end while  

LB(local best) is the largest objective function value attained by the particle to date and this SSD.<br /> 
GB(global best) is the largest objective function value from all particles (SSDs), 
which share information by comparing its LB with other LBs.<br /> 

### MIX operation:    
  For each of the generated candidate SSD,replace qLB = [m1+m2/3] or  
[m1+m2/4] and qGB = [m1+m2/6]  from the LB and GB ,respectively. 

we do the following step:   
* Radomly chioce the number of columns to exchange for whole plot and sub plot,    
  however the sum of wholeplot and subplot equal to "q". 
* Delete the SSD "q" columns form whole plot and sup plot such that the remain design has the largest objective function value.    
* Add "q" columns from LB or GB to make the objective function value become largest from all the columns adding combination. 
  If we add columns form GB, "q" equal to qGB and a new design called mixwGB and If we add columns form LB, "q" equal to qLB and a new design called mixwGB.<br /> 
  
When all particles finish these step, we complete the MIX operation process. 

### MOVE operation:  
  If the objective function value of mixwGB is the largest form mixwLB and current SSD, we replace the current SSD by mixwGB. 
  If, on the other hand, mixwLB has the largest value objective function among all the three designs, current SSD is replaced by mixwLB; otherwise some columns of X are randomly chosen to be replaced by some random balanced 
columns. We recommend the number of such columns to be replaced is qLB.

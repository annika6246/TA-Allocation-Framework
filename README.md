# TA-Allocation-Framework

An optimization framework that allocates teaching assistants to lab practicums based on availability and preference. This object-oriented program employs evolutionary computing to cyclically produce new solutions, measure their fitness based on predefined criteria, and discard inferior solutions. Agents, functions that produce solutions from currently optimal results, both introduce randomization and remove conflicts in potential solutions. 

Evaluation metrics (attempt to minimize all): 
- Overallocation: Sum of times a TA is assigned to more practicums than they can support (ex. if a TA can support 2 sections but is assigned to 5, penalty=3).
- Conflicts: Sum of times a TA is assigned to practicums occurring simultaneously.
- Undersupport: Sum of underallocation occurrences for lab practicums (ex. if a section requires 3 TAs and 1 is allocated, penalty=2).
- Unwilling: Sum of times a TA is allocated to a section they are unable to support.
- Unpreferred: Sum of times a TA is assigned to a section they can support but do not prefer. 

This algorithm produced the optimal solution (unpreferred --> 2, all other metrics --> 0) using our defined evaluation metrics when tested with real course data from Northeastern University (including 43 TAs and 17 lab sections).

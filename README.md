# On-computing-with-some-convex-relaxations-for-the-maximum-entropy-sampling-problem
This project includes the data, results, plots for paper "On computing with some convex relaxations for the maximum-entropy sampling problem"."

#### Data File ####

The benchmark instances are stored in .mat format:

1. ``data63.mat``: positive definite with order $63$ (environmental monitoring network)
2. ``data90.mat``: positive definite with order $90$ (environmental monitoring network)
3. ``data124.mat``: positive definite with order $124$ (temperature data from monitoring stations in the Pacific Northwest of the United States)
4. ``dat2000.mat``: positive definite with order $2000$ and rank $949$ (reddit data)

#### Experimental Setting ####

We ran our experiments under Windows, on an Intel Xeon E5-2667 v4 @ 3.20 GHz processor equipped with 8 physical cores (16 virtual cores) and 128 GB of RAM. We implemented our code in Matlab using the commercial software Knitro, version 12.4, as our nonlinear-programming solver.

#### Results-unconstrained ####

The experimental results for upper bounds without linear constraint $Ax\le b$ are stored in .xlsx format: ``data63.xlsx``, ``data90.xlsx``, ``data124.xlsx``, ``data2000.xlsx``.

In the .xlsx file, each row represents the results for a specific $s$. The columns represent:

1. lower bounds computed by heuristic method
2. upper bounds constructed from a dual feasible solution
3. integrality gaps ($=$ upper bound $-$ lower bound)
4. dualgaps when solving the continuous realxations of MESP
5. number of variables fixed to $0$ 
6. number of variables fixed to $1$
7. number of variables fixed to $0$ or $1$
8. wall clock time for solving the continuous relaxations of MESP
9. cpu time for solving the continuous relaxations of MESP


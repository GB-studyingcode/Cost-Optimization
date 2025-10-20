# Cost Optimization

This my practice on operations research where I use Gurobi solver on Python environment to minimize the cost of transportation

## Parameter
- I is the set of Plant , $I = \{1, 2, 3\}$
- K is the set of Warehouse, $K = \{4, 5\}$
- J is the set of Customer, $J = \{6, 7, 8,9\}$

### Set up cost matrices
cost_ik = [[4,7],[8,5],[5,6]]  
cost_kj = [[6,4,8,4],[3,6,7,7]]

### Set up supply capacity matrix
s_i = [440,650,410]

### Set up demand matrix
d_j = [300,300,250,400]

### Decision variable
- $x_{ik}$ is the interger decision variable of unit delivery from Plant to Warehouse
- $y_{kj}$ is the interger decision variable of unit delivery from Warehouse to Customer


### Objective function
- Minimizing the total workforce assigned: $\min \sum_{i=1}^{3} \sum_{k=4}^{5} x_{ik} c_{ik} +  \sum_{k=4}^{5}  \sum_{j=6}^{9} y_{kj} c_{kj}$

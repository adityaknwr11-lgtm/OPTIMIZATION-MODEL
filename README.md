# OPTIMIZATION-MODEL

COMPANY: CODTECH IT SOLUTIONS  
NAME: ADITYA KANWAR  
INTERN ID: CT06DF952  
DOMAIN: DATA SCIENCE
DURATION: 6 WEEKS  
MENTOR: NEELA SANTOSH  


Objective
The primary goal of this task is to solve a transportation cost minimization problem by applying Linear Programming (LP) techniques using Python. The scenario simulates a supply chain environment where two factories are tasked with supplying goods to three different warehouses. The challenge is to determine the most cost-effective way to transport units from factories to warehouses without exceeding supply or underdelivering demand.

Tools and Libraries
• PuLP: Python library for linear programming.
• Pandas: For data visualization and tabular representation.
• Jupyter Notebook: For interactive and visual implementation of the code logic.

Problem Description
In the given supply chain model:
• Factories:
• Factory_A has a production/supply capacity of 35 units.
• Factory_B has a production/supply capacity of 50 units.
• Warehouses:
• Warehouse_1 demands 30 units.
• Warehouse_2 demands 25 units.
• Warehouse_3 demands 30 units.
Each transportation route between a factory and a warehouse has a fixed cost per unit, forming the cost matrix:

• Factory_A → Warehouse_1: ₹2 per unit
• Factory_A → Warehouse_2: ₹4 per unit
• Factory_A → Warehouse_3: ₹5 per unit
• Factory_B → Warehouse_1: ₹3 per unit
• Factory_B → Warehouse_2: ₹1 per unit
• Factory_B → Warehouse_3: ₹7 per unit

The goal is to minimize the total transportation cost by deciding how many units to send from each factory to each warehouse, while adhering to the supply and demand constraints.

Approach

• Model Setup
A linear programming problem is defined using pulp.LpProblem with a minimization objective.

• Variable Initialization
Decision variables are created for each route from a factory to a warehouse, defined as continuous variables with a lower bound of zero.

• Objective Function
The total cost is formulated as the sum of the product of cost per unit and the number of units transported for all valid routes:

• Constraints
• Supply constraints: Each factory should not ship more than its available supply.
• Demand constraints: Each warehouse must receive at least its required demand.
• Model Solution

The model is solved using model.solve(), and the optimal solution is derived, showing how units should be distributed for minimum cost.

Results
Upon successful execution, the model outputs:
• Status: Optimal
• Total Cost: ₹260.0

• Optimal Distribution Plan:
• Ship 5 units from Factory_A to Warehouse_1
• Ship 30 units from Factory_A to Warehouse_3
• Ship 25 units from Factory_B to Warehouse_1
• Ship 25 units from Factory_B to Warehouse_2

• Unused Routes:
• Factory_A to Warehouse_2
• Factory_B to Warehouse_3
These decisions ensure that:
• All demand is fulfilled,
• Supply constraints are not violated,
• And total transportation cost is minimized effectively.

Visual Summary
The solution includes detailed tables showing:
• The supply available at each factory
• The demand at each warehouse
• The cost matrix per unit
• A summary table with shipped quantities and corresponding costs
Each part is presented using Pandas DataFrames for better clarity and insight.

Conclusion
This task exemplifies the power of linear programming for solving real-world logistics and supply chain optimization problems. By accurately modeling supply and demand constraints and minimizing costs, businesses can achieve higher efficiency and profitability. The use of PuLP provides a flexible, programmable interface for solving such problems, making it highly scalable for more complex networks.
This implementation offers a compact, readable, and accurate demonstration of LP modeling in Python — ideal for both academic understanding and industrial prototyping.


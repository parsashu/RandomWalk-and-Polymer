# RandomWalk-and-Polymer
This project simulates the behavior of polymer molecules using the Freely Jointed Chain (FJC) model, representing polymers as a series of rigid segments connected by flexible joints. The goal is to understand the statistical properties and dynamics of polymers through random walk and FJC simulations, visualizations, and force-extension analysis.

Project Description
This project aims to simulate the behavior of a polymer molecule using the Freely Jointed Chain (FJC) model, a fundamental approach in polymer physics. The FJC model represents a polymer as a series of rigid segments connected by flexible joints allowing free rotation, creating a random walk configuration.

Goals
Simulate Random Walks:

Implement random walk simulations in 1D and 3D.
Analyze statistical properties like mean squared displacement.
Simulate Polymer Using FJC:

Implement FJC model simulations.
Calculate and analyze the end-to-end distance and its distribution.
Compare with theoretical predictions.
Visualize Configurations:

Create 3D visualizations of polymer configurations.
Show changes in conformation with different segment numbers.
Analyze Force-Extension Behavior:

Simulate polymer response to external forces.
Calculate and compare force-extension relationships with theoretical models.
Methodology
Random Walk Simulation:

Start at the origin, choose random directions, and move one segment length 

a.
Repeat for many steps to gather data.
FJC Polymer Simulation:

Initialize a polymer with 

N segments of length 

a.
Randomly orient each segment in 3D space.
Calculate end-to-end distance and gather statistical data.
Visualization:

Use plotting libraries to visualize random walks and polymer chains.
Generate distribution plots of end-to-end distances.
Force-Extension Analysis:

Apply external forces, measure polymer extension, and compare with theoretical models.
Tools and Technologies
Programming Language: Python
Libraries: NumPy (numerical calculations), Matplotlib (visualization)
This project provides a comprehensive exploration of the FJC model and its applications, offering insights into the statistical and mechanical properties of polymers.


Assumptions, Techniques and Conclusions

b.	The step_vector norm is always 1. We choose x and y randomly, and z is then determined.
    Note that the signs of y and z should also be chosen randomly.

c.	The results are two Gaussian curves which shows the randomness.
    The mean on the Gaussian function grows by adding more steps which shows for higher step numbers the particle can explore more reach further. 
    I thought the mean should always be on zero!

d.	The result of this section confirm that with more steps particle indeed can explore more and get higher displacement.

e.	In this FJC model I assumed the force make alignment probability bias to the force direction.
    I did this by adding bias to probability of aligning to force direction and the bias is indeed “f” because “f” is normalized between 0 and 1.
    The result is by adding more force the length of polymer goes up linearly.

f.	In this section I assumed that two forces are being applied in just x axis and not only they bias choosing x over y and z 
    but they bias aligning chains to the direction of the force.
    So “f’ affection multiplies because of two biases.
    and the result are parabolic as expected. In grid form concavity is up because by adding force choosing x bias increases.
    But in free form concavity is down because bias has a threshold (step norm is always 1).
    and they both reach straight form and the length stay constant.






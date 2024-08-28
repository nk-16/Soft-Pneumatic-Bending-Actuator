# Soft-Pneumatic-Bending-Actuator

Working on optimisation of the design parameters of a soft pneumatic actuator using finite element methods. The goal was to achieve maximum bending at specific pressures while minimising stress concentrations. Additionally, I explored alternative designs to enhance efficiency within soft robotics. I have used FEM as it can accommodate significant deformations and material nonlinearities within Soft Pneumatic Actuators. The following steps I have followed in the modelling of the Pneunet Bending Actauator in Ansys:-

* **Material Assessment**
  
Yeoh 3rd-order model and its parameters for silicon material were chosen for the material assignment. The Yeoh model is chosen because it only needs a small amount of experimental data to get reasonable
numerical results. It can also describe a wide range of deformation.

* **Mshing Parameters**
  
A global element size of 1 to 2 mm is ideal for modelling using the Multizone or Hex Dominant methods for body sizing. The Multizone method and Hex Dominant mesh give good results regarding computation efficiency and element quality. I also tried using the Cartesian method but found it computationally heavy. The multizone method gave better element quality than Hex Dominant mesh while being more computationally efficient. I have used symmetry to reduce the number of nodes.

* **Loads and Boundary Conditions**
  
The load applied is of internal pressure of 1 KPa in tabular form. This pressure is applied slowly with 0.1 KPa in each time step. Other than this, standard earth gravity has been applied while one end is fixed as a boundary condition. For better convergence of results, I have used neqit,50, which increased the number of iterations per substep. The following image depicts these boundary conditions.

![image](https://github.com/nk-16/Soft-Pneumatic-Bending-Actuator/assets/128499808/7e5ff896-0ebd-49b8-9856-e16fbb237d51) 

* **Design Optimization of Soft Pneumatic Actuator**
  
Optimization is done based on the relation between the design parameters and the curvature of the Pneunet Bending Actuator (k). I have varied the thickness t of the bottom restraining layer and height H of the chamber in order to increase the curvature of the pneumatic soft actuator. This relation has been derived by assuming the condition of static equilibrium and thus equating the derivative of potential energy to zero.

![image](https://github.com/nk-16/Soft-Pneumatic-Bending-Actuator/assets/128499808/b720c582-d4df-4be9-b492-410b8cf535ef)

* **Results and Conclusion**

The following table compares the initial design of the Pneunet Bending Actuator and the optimised one.

![image](https://github.com/nk-16/Soft-Pneumatic-Bending-Actuator/assets/128499808/817d9e09-9d0f-4ad1-ac54-e7a6d0053d58)
![image](https://github.com/nk-16/nk-16/assets/128499808/8cc0b9f2-19a4-4a60-bd12-ac241881dffa)

* **Alternative Designs**

I have also explored alternative designs for Soft Pneumatic Actuators and observed their pros. These alternative designs are a Tetrahedral chamber pneumatic actuator, a Tail-based pneumatic actuator and a Claw-based pneumatic actuator.

![image](https://github.com/nk-16/nk-16/assets/128499808/c3101167-0ace-41a2-80bf-a0cebcbc8b93)

# AE667_Assignment2 / 170010036

Programming language: Python

Editor: Jupyter notebook

Notebook is devided into two parts:
1. Implementation of BEM Theory
This is the basic code for implementation of Tip loss and without tip loss model. 
Global Parameters: 
rho                           #Density 
V                             #Forward or climb speed of propeller or rotor
blades=b                      #No of blades
rpm                           #RPM
omega   
R                             #Radius
Rrc                           #Root cut out
chord_length 
C0                            #Taper Length at the Root of Blade 
C1 = -0.05

a = 5.75                      #Slope of Cl vs alpha
cd_min = 0.0113               #min value of Coefficient of Drag
eps = 1.25     

For Calculating Thrust, Torque, CT, CQ, Power we have to specify above mentioned parameters and simply run:


=================================================================================
#calculation total thrust in Newton and coefficient of thrust for Tip loss model
Thrust_tip_loss = quad(dT_tip_loss,Rrc,R)
Ct_tip_loss = (Thrust[0])/(rho*math.pi*(omega**2)*(R**4))
print (Thrust_tip_loss[0])
print (Ct_tip_loss)
----------------------------------------------------------------------------------
#calculation total torque in Newton*Meter and coefficient of torque for Tip loss model
Torque_tip_loss = quad(dQ_tip_loss,Rrc,R)
Cq_tip_loss = (Torque_tip_loss[0])/(rho*math.pi*(omega**2)*(R**5))
print(Torque_tip_loss[0])
print (Cq_tip_loss)
=================================================================================
#calculation of total power in Watt and coefficient of power for Tip loss model
Power_tip_loss = Torque_tip_loss[0]*omega
Cp_tip_loss = Cq_tip_loss
print (Power_tip_loss)
print (Cp_tip_loss)
===================================================================================
.
.
.
.
.
.
2. Results and Experiment: This sectiona include the all plots mentioned in report. all can be regenerated by running all cells in order after running Part1 functions. I have already mentioned and defined the above metioned parameters for every result according to need. You can change those value and try for different value of parameters. 



## Just Run the code in order to regenerate the all results mentioned. For try different i have created different part where we can change the values if we want to check the thrust and power for different values. 










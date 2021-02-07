# TrackVehicleSimulation
This is a simple 2D simulation of a tracked vehicle composed of two rectangular tracks attached to a central plate. By track we refer to a continous belt that is in contact with the ground (also known as a tank tread). 

Given the track is in contact with the ground over a large area and not concentrated at a single point, the contact area is subdivided into a grid of contact elements. The friction force acting on these elements is the numerically integrated using simpson's rule, and these results are used as estimates for the net force and torque acting on the track. These net track forces are then combined under the assumption that the vehicle is a rigid body to generate the net forces acting on the vehicle.

The net vehicle force and torque are the integrated twice using the trapezoidal rule to find its instantaneous velocity and position. The velocity estimates are then fed back into the track force routine in order to generate a new iteration of the velocity and position - Esenstially, a system of ordinary differential equations is solved simultaneously in order to estimate the state of the vehicle.

These estimates are then fed into a simple canvas animation which is displayed at the end of the program. This animation can then be saved as a video that is created next to the .py file. 

NOTE: This was written in Python 3.

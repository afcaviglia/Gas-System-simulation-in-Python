This script creates a molecular dynamics simulation for a system of particles interacting through the Lennard-Jones potential in a periodic cubic box. 

Summary:

    Initialization:
        Import necessary libraries: NumPy, random, pickle, pandas, and math.
        Define user variables like box size (L), particle density (σ), particle mass (m), temperature (T), time step (Δt), total duration (Nt), and output frequencies.

    Initialization for Testing:
        Provide some default values for testing purposes.

    Functions:
        VelocitiesInit: Assigns random velocities to particles based on the Maxwell-Boltzmann distribution.
        ForceCalculation: Calculates the net force on each particle based on the Lennard-Jones potential and provided coordinates.
        toDF: Converts coordinates to a DataFrame for PDB file preparation.
        writePDB: Writes the coordinates of the system to a PDB file.

    Initial System Setup:
        Initializes the system by calculating particle distances based on density (σ).
        Generates a 3D grid with distributed positions.
        Selects random positions for particles from the grid.

    Main Loop - Equations of Motion (Verlet Integration):
        Iterates over time steps to simulate the motion of particles.
        Calculates forces between particles using the Lennard-Jones potential.
        Updates positions and velocities using the Verlet integration method.
        Writes the coordinates to a PDB file for each time step.

    Output:
        Saves energy values (potential, kinetic, and total) at each time step to a binary file.
        Saves velocities at each time step to a binary file.

    Visualization:
        Plots velocities and energy values over time.

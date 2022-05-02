---
title: MDsrv
---

# Examples

### Streaming trajectories from our MDsrv instance:

All trajectories are stored on our server and then streamed frame-by-frame to the frontend that hosts the Mol* viewer. This makes an efficient visualization of even large trajectories (> 4.5 GB as in example 2) even on a mobile device possible. This server-frontend communication does not limit instant analysis calculations for time-trace plots.

- <a href="https://proteininformatics.informatik.uni-leipzig.de/?session-url=https%3A%2F%2Fremote.sca-ds.de%2Fget%2Fsession%2F80de2863-618b-4e4d-b811-316027fed991" target="_blank">Trajectory Streaming 1</a>


- <a href="https://proteininformatics.informatik.uni-leipzig.de/?session-url=https%3A%2F%2Fremote.sca-ds.de%2Fget%2Fsession%2Ff010cb1f-44ed-4938-8e56-610936224006" target="_blank">Trajectory Streaming 2 - Large Trajectory</a>

### Time-trace plot 

 A time-trace plot is an interactive plot that links to the trajectory frames. By clicking on any point in the plot, the corresponding frame is show. A time-trace plot can show the distances between 2 selections (e.g. atoms), the angle between 3 points, the dihedral between 4 points, or the RMSD of the complete structure and their changes over the time of the simulation.

Usage instructions: To view the line plot of the example, you need to open the _Extension_ panel at the bottom and then go to the _Time Trace Graph_ menu. In the lower left corner of the white canvas you can see the progress of the measurement calculation. When the calculation is complete, the measurement is available in the _Time Trace Plot_ menu. You can switch to the RMSD plot for the entire structure by selecting the _RMSD_ button in the _Time Trace Plot_ menu while the desired measurement is selected.

- <a href="https://proteininformatics.informatik.uni-leipzig.de/?session-url=https%3A%2F%2Fremote.sca-ds.de%2Fget%2Fsession%2Fa491ac86-989a-416f-96e4-85fae55c4a2f" target="_blank">Distance time-trace</a>

### Alignment View

Usage instructions: To view the sequence alignment of the example, you need to open the _Extension_ panel at the bottom and then open the _View Sequence Alignment_ menu. You can hover over the residues to highlight them in the canvas. You can focus on a single residue by clicking on it.

- <a href="https://proteininformatics.informatik.uni-leipzig.de/?session-url=https%3A%2F%2Fremote.sca-ds.de%2Fget%2Fsession%2F9ddf37db-a249-4f6e-b542-9626b1cf6182" target="_blank">Alignment View</a>









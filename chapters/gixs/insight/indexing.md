# Indexing

Indexing GIWAXS data is a challenging task that requires a solid understanding of crystallography. INSIGHT provides a convenient way to compare experimental data with simulated diffraction peak positions. Note that these calculations are performed within the Born approximation and do not account for refraction effects. For most GIWAXS experiments, however, this approximation is sufficient.

The first step is to simulate the diffraction peak positions for a given crystal lattice.

```python
#########################
# GIWAXS simulation
#########################
# set simulation parameters
max_q = 2.  # maximum q values to be calculated

# define the crystal lattice parameters
# choose space group and parameters, create your own spacegroups if necessary
# See here for the list of space groups :
# https://rlennart.github.io/insight_scatter.giwaxs_sim.html
# NOTE: not all space groups are implemented, but you can easily add the ones you need
# check out http://img.chem.ucl.ac.uk/sgp/large/sgp.htm for more information about space groups

crystal = ins.gs.hexagonal.SG168(a_length=16.5,c_length=1e6)

# specify what orientations you want to simulate
crystal_orientations = [[0, 1, 0],
                         [-1, 2, 0]]

# specify range of hkl for calculations
hkl_ranges = (range(-2, 3), range(-2, 3), range(1))
...

```

You can adjust the simulation parameters to match your system, including:
- The maximum q range (```max_q```)
- The crystal structure and lattice parameters
- The crystal orientations relative to the substrate
- The range of Miller indices (```hkl_ranges```)

In this example, we use a hexagonal lattice that is effectively two-dimensional by setting the c parameter to a very large value. Two crystal orientations relative to the substrate are simulated.

Running the simulation produces a table listing all calculated diffraction peaks. This table is also saved as a text file.

![](images/list-peaks-calc.png)


The simulated peak positions can then be visualized in reciprocal space.

![](images/simulation-indexing.png)


Finally, run the next cell to overlay the simulated diffraction peaks onto the experimental GIWAXS images. This allows direct comparison between the measured and calculated peak positions, facilitating phase identification and crystal orientation analysis.

![](images/image-indexing.png)

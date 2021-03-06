The evolutionary multiobjective experiments described in M. Sipper, J. H. Moore, and R. J. Urbanowicz, "Solution and Fitness Evolution (SAFE): A Study of Multiobjective Problems", in _Proceedings of 2019 IEEE Congress On Evolutionary Computation_, 2019.

* `safe.py`: the main evolutionary algorithm
* `general.py`: additional general functions, also used in experiments other than multiobj
* `multiobj.py`: the multiobjective code
* `plot_front.py`: used to plot the evolved Pareto fronts
* `f1f2.py`: function name (e.g., 'ZDT1') and evolved f1 and f2 fronts (used by `plot_front.py`)

To run: 
1. set parameters in `general.py` (GENERATIONS, SOLUTION_POP_SIZE, OBJECTIVE_POP_SIZE, etc.)    
2. run safe.py directly, or from command line:   
`python safe.py [StandardEA/Novelty/SAFE/Random] MultiObj [ZDT1/ZDT2/ZDT3/ZDT4/ZDT6]`    

At the end of a run the `results` folder will contain a csv file and a text file, e.g.:   
`SAFE_MultiObj_ZDT1_VBHEPM.csv`   
`SAFE_front_MultiObj_ZDT1_VBHEPM.txt`   

The csv contains a summary of the results. The txt file contains the fronts found (one per experiment) and their _igd_ values.

To plot an evolved Pareto front simply copy front values from the txt file -- `f1` and `f2` lists -- into `plot_front.py` and in that file also set `func_name` to the correct problem, e.g., 'ZDT1'. Then run `plot_front.py` to generate a figure such as this:   

<img src="https://github.com/EpistasisLab/SAFE/blob/master/multiobj/results/zdt1_evolved_front.png" alt="evolved Pareto front" width="400"/>


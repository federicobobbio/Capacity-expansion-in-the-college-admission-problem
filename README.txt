Capacity expansion in the college admission problem

Two mathematical programming methods (quadratic and linear) and two heuristics (LP-based and greedy) to solve the problem of expanding optimally capacities in the college admission process. The goal is to allocate optimally funding that expand the capacities of the universities. The objective function is the cost of the students, which we wish to minimize.

This project contains the following python scripts and folders:

1) An "__init__.py" script in which it is possible to run the aggregated linearization mathematical method.

2) An "instance.py" script that given as input the number of students and colleges, it produces a randomly generated instance of the problem.

3) An "heuristics.py" script in which are contained the LP-based heuristic, the Greedy heuristic and a function "add_bound" that porvides a warm-up solution to the mathematical programming methods.

4) A "math_models.py" script that contains the two mathematical programming models: 
A quadratically constrained integer program and a McCormick convex linearization of the former model. 

5) A "read.py" script in which we define a function "read" that reads the logs.txt of the computation that we have conducted. 
Moreover, we also provide the function "produce_data_table" that prints the data to be insert in Table 2 of the paper. 

6) A "plot.py" script with the code needed to produce the plots.

7) Some data folders:
	
	7.A) "Experiments_n1=1000" contains the log.txt of the experiments that we have conducted with 1000 students

	7.B) "Experiments_n1=2000" contains the log.txt of the experiments that we have conducted with 2000 students

	7.C) "Heuristics_sol" contains the cost value and the computational time for all the experiments that employed the heuristics. 
		"greedy" refers to the greedy heuristic, while "LP_based" refers to the LP-based heuristic.

	7.D) "Histogram_data" contains the data about the computations made to produce the histogram.

 	7.E) "Instances XXXX students and YY universities" contains all the instances of all the computations that we have made. 
		To read an instance it suffices to run the following function:

		def read_instance(filename):
    			return np.load("Instances/"+filename+".npy", allow_pickle=True)

	
		Note that in each instance we only save the preferences of the students, the preferences of the colleges and the capacities of the colleges. 
		It is possible to retrieve the remaining information (e.g., the sets T,S, Gamma) from the function "create_instance" in the script instance.py.

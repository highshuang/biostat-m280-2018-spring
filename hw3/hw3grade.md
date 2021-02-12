*GAO, SHUANG*  

### Overall Grade: 93/100

### Quality of report: 10/10

* Is the homework submitted (git tag time) before deadline?

	Yes. `2018-05-24 22:12:00 -0700` for tag `hw3`. 
	
* Is the final report in a human readable format html? 

	Yes. `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility?  

	Yes. `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report?

    Yes, the report is clear and easy to read
 
### Correctness and efficiency of solution: 45/50 

* Q1 (15/20)

  **efficiency** (0/5 pts)
  Let ![](https://latex.codecogs.com/gif.latex?X%20%3D%20%5BX_%7B2003%7D%27%2C%20%5Cldots%2C%20X_%7B2008%7D%27%5D%27) and ![](https://latex.codecogs.com/gif.latex?y%20%3D%20%5By_%7B2003%7D%2C%20%5Cldots%2C%20y_%7B2008%7D%5D), we have ![](https://latex.codecogs.com/gif.latex?%5BX%3A%20y%5D%27%20*%20%5BX%3A%20y%5D%20%3D%20%5Csum_%7Bi%20%3D%202003%7D%5E%7B2008%7D%5BX_i%3A%20y_i%5D%27%20*%20%5BX_i%3A%20y_i%5D). Since the 26 by 26 matrix ![](https://latex.codecogs.com/gif.latex?%5BX%3A%20y%5D%27%20*%20%5BX%3A%20y%5D) contains all the information for fitting linear regression, we can read in the large matrix ![](https://latex.codecogs.com/gif.latex?X_i%2C%20i%3D%202003%2C%20%5Cldots%2C%202008) one by one and generate ![](https://latex.codecogs.com/gif.latex?%5BX%3A%20y%5D%27%20*%20%5BX%3A%20y%5D) iteratively.  In this way, you don't need the memory for all the design matrics at the same time, which drains off the RAM quickly. 
 
  **correctness**(15/15 pts)
    Good job!
	
* Q2 (30/30)

Notice in Dr. Zhou's answer, he set all the diagonal elements of A to be 0. Your answer for Q2 may be different from Dr. Zhou's answer.

Q2(1) (3/3pts) Good job!

Q2(2) (3/3pts) Good job!
Q2(3) (6/6pts)

number of pages: right (500)
number of edges: right (11158)
number of dangling nodes (pages with no out links) right (96)
which page has max in-degree? right ("http://www.ucla.edu")
which page has max out-degree? right ("http://giveto.ucla.edu")
visualize the sparsity pattern of  A: good


Q2(4) (12 / 12pts) 

1) (3 / 3 pts): Good job!

2) (3 / 3 pts): Good job!

3) (3 / 3 pts): Good job!

4) (3 / 3 pts): Good job!

Q2(5) (3/3pts) Good job!

Q2(6) (3/3pts): Good job!



### Usage of Git: 10/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.
	
* Are there enough commits? Are commit messages clear? 

	 Yes. 
	
* Is the hw3 submission tagged?

	Yes.

* Are the folders (`hw1`, `hw2`, ...) created correctly? 

	Yes.

* Do not put a lot auxillary files into version control.  

	Yes. 

### Reproducibility: 8/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results?  (-2 pt)

	The path in chunk 191 `"D:\\UCLA\\quarter3\\BS280\\biostat-m280-2018-spring\\hw3\\ucla"` is for your own machine. You can use url link to download the files, or put the files in `hw3` folder and load by `readcsv("A.txt")`.

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw3.
    

### Julia code style: 20/20

* Rule (4): 4 spaces for indenting. 

* Rule (6): Never place more than 80 characters on a line. 

* Rule (7): Always include a single space after a comma. 

* Rule (8):  Never insert a space before a comma.

* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. 

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.

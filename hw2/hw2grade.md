*Shuang Gao*

### Overall Grade: 89/100

### Quality of report: 10/10

* Is the homework submitted (git tag time) before deadline? 

	Yes. `2018-05-11 21:54:25 -0700`. 

* Is the final report in a human readable format html?  

	Yes,  `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility?

	Yes, `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report?

	Very clear report
 
### Correctness and efficiency of solution: 44/50 

* Q1 (20/25 pts)

    1, 3) (11/15 pts)
    
    **Efficiency(8/11pts)**
    Dr. Zhou's implementation for `r = 20` has memory estimate 7.12 MB and allocs estimate 10, while yours is `1.60 k allocations: 5.162 GiB, 9.85% gc time`. There is a lot of room for improving efficiency.
    -  Use pre-allocation to save gabbage collection: Dr. Zhou's implement uses half of the memory in pre-allocation. For more details, please check Dr. Zhou's implement(-1 pt)
    -  Don't calculate the same matrix couple times, use pre-allocate array to save middle steps. you calculate `X - A_mul_B!(mul_VW, V, W)` at lease three times in a loop(-2 pts)
       - Use BLAS to reduce memory allocation: Instead of using `X - A_mul_B!(mul_VW, V, W)` in looping, use `LinAlg.BLAS.gemm!('N', 'N', -1.0, V, W, 1.0, X)`. This helps to reduce the memory allocation. 

     **Correctness(4/4 pts)**
    
     **Others**
    - Using `vecnorm` instead of `sum(abs2, X - A_mul_B!(mul_VW, V, W))` will speed up your function
    
    4, 5) (3/5pts) You should be able to observe that in part 5 the function ends within 3 iterations; This question is not a convex question, so there is no guarantee for unique result with random initial input matrix. 
    2, 6) (5/5pts) Good job!


* Q2 (23/25 pts)

    1) (5/5pts) 
    2) (20/20 pts)
    **Algorithm(7/7pts)**
    **Efficiency(5/7pts)**
    Dr. Zhou's implementation has memory allocation 1.34KB, yours is 5.05KB. Pretty good! Some suggestions:
    - Use `BLAS.syrk!()` to reduce memory allocation in `I + σ1^2 / σ0^2 * Z'Z` and save all symmetric matrix in form symmetric (-1 pts)
    - The extra memory allocation caused by transpose can be avoid by using Blas functions in `I + σ1^2 / σ0^2 * Z'Z` and `Z'y`. (-1 pts)
    **Correctness(6/6pts)**

    **Others**
    You can check the input to make the function more stable for wrong input.
    
### Usage of Git: 10/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.

* Are there enough commits? Are commit messages clear? 

	Yes

* Is the hw2 submission tagged? 

	Yes

* Are the folders (`hw1`, `hw2`, ...) created correctly?

	Yes.	

* Do not put a lot auxillary files into version control.  

	Yes.
		

### Reproducibility: 10/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results? 

	Yes

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw2.

### Julia code style: 16/20

* Rule (4): 4 spaces for indenting.

* Rule (6): Never place more than 80 characters on a line.

* Rule (7): Always include a single space after a comma. (-1 pts)
    - code chunk 45 line 2

* Rule (8):  Never insert a space before a comma.

* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. (-3 pt)

    - code chunk 39 line 10
    - code chunk 37 around line 11
    - code chunk 113

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.

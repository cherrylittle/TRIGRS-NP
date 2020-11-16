# the parallelization to TRIGRS model (TRIGRS 2.1)
We use OpenMP and MPI to further parallelize the latest version of TRIGRS model, TRIGRS 2.1, shortening its running time.
And we call this new version after our optimization TRIGRS-NP.

Directories:

TRIGRS-NP code : storing the codes after optimized and the data used in experiments.

TRIGRS 2.1 code: storing the codes before optimized and the data.
notice: Since dataset 2 is too large, we compress all the files in it. 
        Please unzip them to ".asc" files, as such files in dataset 1.
        
The TRIGRS code (serial code) are  included in TRIGRS 2.1 code. The files name with "_p" is TRIGRS 2.1 code, 
and the ones without "_p" is TRIGRS code.

Compiling and running steps: 
1) load the compiling environment (load MPI, GSL)
2) make (generate tpx, trg, prg) 
3) yhrun. /tpx
4) for TRIGRS code: yhrun ./trg
   for TRIGRS 2.1 code: yhrun -n ./prg
   for TRIGRS-NP code: yhbatch - N - n - c. / run1.sh

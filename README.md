The 'inputs' folder contains a sample parsed reference template for chromosome 21 and a sample parsed reads dataset simulated with SimLord (150bp long, 100K reads; error rate 0.01) that can be used for testing the prototype. 

Note: The preprocessing run will generate several auxiliary files for reference index. Additionally, user is expected to specify the path of the main directory in preprocessing.py, alignment.py, and postprocessing.py files.

Required python modules:

pip install numpy <br />
pip install mpi4py <br />

cd codes <br />

Preprocessing:

Required options for preprocessing:

--chrnum: chromosome number <br />
--nr: total number of reads <br />
--rl: read length <br />
--nrg: number of read groups <br />
--nrb: number of read batches <br />

Example: python3 preprocessing.py --chrnum 21 --nr 100000 --rl 150 --nrg 2 --nrb 8

Alignment:

Required options for alignment:

--chrnum: chromosome number <br />
--nr: total number of reads <br />
--rl: read length <br />
--nrg: number of read groups <br />
--nrb: number of read batches <br />
--tcn: template chunk number <br />
--rbn: read batch number <br />

Example: python3 alignment.py --chrnum 21 --rl 150 --nrg 2 --nrb 8 --tcn 0 --rbn 0

Postprocessing: 

Required options for postprocessing:

--chrnum --> chromosome number <br />
--rl --> read length <br />
--nrg --> number of read groups <br />
--nrb --> number of read batches <br />
--tcn --> template chunk number <br />
--rbn --> read batch number <br />

Example: python3 postprocessing.py --chrnum 21 --rl 150 --nrg 2 --nrb 8 --tcn 0 --rbn 0

This code is a prototype and is not intended for large-scale commercial applications.

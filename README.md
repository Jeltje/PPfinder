This directory contains the PPFINDER executable and library files needed by the program. It also contains a copy of gtf2fa.pl, a program called by PPFINDER.
PPFINDER needs a parameterfile as input. An example is parameter.file which should be changed to reflect the locations of all databases and programs needed. Please see explanatory text in parameter.file.
The get_synteny_files.pl program can be used to retrieve and format synteny files for different combinations of organisms (see paramter.file for explanation).

To run PPFINDER, install the programs and libraries and modify your $PATH so the program will find them. To run PPFINDER on a whole genome GTF:

PPFINDER.pl -m parameter.file <full path>/chrN.gtf

Depending on the size of the GTF file, this may run for several hours. The output is:

N.masked.txt (N being the chromosme number): a list of gene IDs marked as containing processed pseudogenes
N.masked.gtf : GTF file with masking coordinates. This can be used to mask the chromosome for the pseudogenes found
N.pgene.reason : log file

If the program fails, a detailed error message can be found in N.ERROR

To run PPFINDER in gene prediction mode, N-SCAN or Twinscan must be installed. These programs can be downloaded from
https://mblab.wustl.edu/software.html

PPFINDER can be easily modified to run with other gene predictors, providing their outputfiles are in GTF format. For details, see the comments in the script or contact the author:
jeltje.van.baren@gmail.com

Publication: 
[Iterative gene prediction and pseudogene removal improves genome annotation](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1457044/)

# Analysis Plan
**By Andrea Chua**

## Analysis 1: using kmer compositions to determine the changes in DNA composition relative to where the virus first began

Virus first began in Wuhan, and data will be collected from NCBI.
NCBI has the complete genome sequenced here [NCBI](https://www.ncbi.nlm.nih.gov/nuccore/1798174254).
I am still in the process of finding more information,
as NCBI doesn't seem to have all the information I need.
I might need to tweak it to a specific geographical range/region
to make things easier.


### Functions Needed

* Will be using Needleman-Wunsch Algorithm as the alignment algorithm
but I am concerned with the amount of data that I am able to process with my code;
but might also consider BioAlignments (below)

* kmercount function from assignment04

* calculating total kmers and then the percentage:

    function kmerPercent(kmercount, kmerTotal)
        total = (kmercount/kmerTotal) * 100 
        return total
    end

* Perhaps refer to code in: [BioAlignments.pkg](https://github.com/BioJulia/BioAlignments.jl)

    + look further into codes in [BioAlignments.jl package description](https://biojulia.net/BioAlignments.jl/stable/pairalign/)


### Plots and Display Items

* Will be using the Makie.jl to create graph

* Radial plot of percentage of changes in kmer composition in relation to the distance it is from the origin 

* A reference: ![radial plot](https://i.stack.imgur.com/sgiPd.png)

* color coded for different percentages, and radius are labeled as directions (like in the graph above)




## Analysis 2: changes in spike proteins across time in the United States (or track a certain region as I do not have an efficient enough code)

Analyzing spike proteins of current variants 
(alpha, beta, gamma, delta)
against the original strain from Wuhan. 


### Functions Needed

* Needleman Wunsch (as per the previous analysis)

* find_dna function from assignment05 to locate spike proteins

* add a section keeping track/counting regions and updating the array that stores the spike protein information 

* Perhaps refer to code in: [BioAlignments.pkg](https://github.com/BioJulia/BioAlignments.jl)

    + look further into codes in [BioAlignments.jl package description](https://biojulia.net/BioAlignments.jl/stable/pairalign/)


### Plots and Display Items

* using Makie.jl to generate a line graph

* line graph axes will be time against number of changes in spike protein 

* different colored line for each variant

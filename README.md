# primate_proteins
Coding with all analyses performed in a project that aimed to study primate proteins in a large number of genomes. 

Firstly, I downloaded all required genomes (listed on file genomes_download_links.csv) using their curl links. To see the full script, go to
## Script 01.Downloading_ENA_genomes

Before blasting selected proteins against the genomes, I corrected their sequence format, since bases from the sequences were split into several lines and this can cause a lot of trouble later on if unnoticed. I just copied them in the Firefox search bar to correct this, and them copied the sequences along with their headers to files I created using vim. This and the processing I performed on the downloaded genomes can be seen in
## Script 02.Processing_protANDgenomes

After processing our queries and the genomes that will form our genomic database, we'll BLAST the protein nucleotide sequences against the genomes downloaded (full list with names and taxonomic assignation of each assembly used to compose our genomic database can be found in the Genomes_DB_list.tsv file). For that, go to 
## Script 03.BLAST_proteins

After BLASTing our proteins of interest against the monkey genomes, we'll separate short hits from large hits, as well as only consider those results whose e-value is smaller than 0.001. For that, go to 
## Script 04. Processing_BLAST_output

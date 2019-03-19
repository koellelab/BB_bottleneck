Transmission Bottleneck Estimator

This is the implementation of transmission bottleneck estimation method based on beta-binomial sampling described in "Transmission Bottleneck Size Estimation from Pathogen Deep-Sequencing Data, with an Application to Human Influenza A Virus".

Requirements
R 3.5.2+
rmutil 
argparse
Rscript

Be sure to add the Rscript path to your environment variables or include the path when calling Rscript from the command line.  


Example:

For the approximate code run

Rscript --vanilla Bottleneck_size_estimation_approx.r  donor_freqs.txt recipient_freqs.txt  0.03 1 200

The command line arguments are list of donor variant frequencies, list of recipient variant frequencies, variant calling threshold, minimum bottleneck size, and maximum bottleneck size.

For the exact code run

Rscript --vanilla Bottleneck_size_estimation_exact.r donor_freqs.txt recipient_total_reads.txt recipient_var_reads.txt 0.03 1 200

The command line arguments are list of donor variant frequencies, list of recipient total reads, recipient variant reads, variant calling threshold, minimum bottleneck size, and maximum bottleneck size.


The codes will output plots in pdf format called "approx_plot.pdf" and "exact_plot.pdf".


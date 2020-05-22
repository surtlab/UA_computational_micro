# A Basic How-to Guide for Assembling Bacterial Genomes in Cyverse

Step 1: Log into [`Cyverse`](https://www.cyverse.org/)

Step 2: Launch `Discovery Environment`

Step 3: Click on the `Apps` tab

Step 4: Search for `nanoDJ` 

Step 5: Click on the `nanoDJ` program and rename the analysis so that it reflects the strain you are assembling and select an appropriate folder for the analysis files 

Step 6: Launch `nanoDJ`

A message should appear in the message center at the top right of the screen (it's shaped like a bell). If you click on the message center it will give you the option to `access your running analysis`. This will take you the Jupyter notebook running `nanoDJ`. You should see orange swirly icons as the Jupyter notebook loads.

Step 7: Click the icon for `terminal`. This should open up a command line terminal session.

I've provided a walk through video of Steps 1 through 7 [here](https://www.youtube.com/watch?v=OKPDGWGYThU)

Step 8: At the top left of the directory of this Jupyter notebook, you should see an icon for an up arrow above a horizontal line. Click this icon to upload your read files into this Jupyter notebook. If you have paired end reads, upload both Illumina read files separately. Upload the Nanopore reads as a separate file.

Step 9: On the `terminal` command line, run the program `unicycler` using the following commands

```
unicycler-runner.py -1 Illumina_read_file_1.fastq -2 Illumina_read_file_2.fastq -l Nanopore_read_file.fastq -o output_directory
```

You should have the option to tab-complete the read file names for the Illumina and Nanopore reads automatically if they were uploaded properly.

On a reasonably sized bacterial genome (~6Mb), a unicycler run should take approximately a 24 hours or so. The output files will be deposited ino the output directory specified in the command line above (which should be created in the `nanoDJ` directory tree once you start the analysis.

# Coverage-Analysis-v3
Overview
Coverage-Analysis-v3 is a software tool designed to analyze the coverage of sequences by primers for LAMP, PCR, and other nucleic acid amplification tests (NAATs). The tool is implemented in a Jupyter Notebook format, providing an interactive environment for users to explore and analyze their data. See associated publicaiton for more detailed information. Made for HIV-1 coverage but can be applied to any pathogen with nucleic acid sequence diversity.

Workflow:
Coverage is defined in a few ways (1) Perfect Alignment of all primer regions (2) Single SNP: one mismatch per primer outside of the last 5 bp of the critical termini of a primer region (3’ for all except 5’ of F1/B1) (3) ROSALIND Coverage: ROSALIND score of ≤ 3 for any primer in a LAMP assay indicating coverage. Modified ROSALIND scoring looks at individual sequences in lieu of an incident and prevalence approach. Additionally, in the context of multiplex assays, overall coverage is determined if at least one assay shows coverage. Coverage can be weighted based on global subtype prevalence.
ROSALIND Score: https://www.rosalind.bio/en/knowledge/calculating-the-severity-score-for-lamp-assays
Alignments: capabilities to extract sequences from Los Alamos National Labs (LANL) alignments or from GenBank ID
Outputs: coverage can be determined at the assay, primer and nucleotide level.

Software Components:
Main Software Process
Notebook: ChainLAMP_coverage_analysis_v3.4.ipynb
Coverage Software:
[1A] Setup for All Necessary Inputs:
This section guides you through setting up the required inputs. Please review the folder files to understand how assays and primers are denoted.
[1B] Running the Coverage Analysis:
Execute this section to determine the coverage of your sequences by the primers. Ensure that you have completed the setup in [1A] before running this.

Additional Software
Notebook: ChainLAMP_coverage_analysis_v3.4_extension.ipynb
Sequence Library Generation:
[1A] Generate a Library of Sequences:
This section helps you create a library of sequences organized by subtype, which can be used as input for the main analysis pipeline. This process involves removing gaps from alignments and categorizing sequences by subtype.
[1B] Generate Alignments with Year-Based Splits:
This optional step allows for further splitting of sequences by year, although this capability is currently not available in this version.
[1C] Gather Sequences from GenBank IDs:
An additional feature that allows users to retrieve sequences from GenBank using their IDs for further analysis.

Getting Started
Prerequisites
Python 3.11
Jupyter Notebook
Necessary Python packages

Running the Analysis
Open ChainLAMP_coverage_analysis_v3.4.ipynb in Jupyter Notebook.
Follow the instructions in the notebook, starting with section [1A] to set up your inputs.
Once setup is complete, proceed to section [1B] to run the coverage analysis.
For generating a sequence library or working with GenBank IDs, open and follow the instructions in ChainLAMP_coverage_analysis_v3.4_extension.ipynb.

Contributing
Contributions are welcome! Please feel free to submit a Pull Request or report issues to help improve this software.

Contact
For questions, suggestions, or contributions, please contact sgillig1@uw.edu.

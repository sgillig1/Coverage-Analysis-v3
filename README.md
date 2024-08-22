# Coverage-Analysis-v3

## Overview

**Coverage-Analysis-v3** is a software tool designed to analyze the coverage of sequences by primers for LAMP, PCR, and other nucleic acid amplification tests (NAATs). Implemented in a Jupyter Notebook format, this tool provides an interactive environment for data analysis. Originally developed for HIV-1, it can be applied to any pathogen with nucleic acid sequence diversity.

## Workflow

Coverage is analyzed in several ways:
1. **Perfect Alignment:** All primer regions align perfectly.
2. **Single SNP Coverage:** Allows for one mismatch per primer, excluding the last 5 bp of the critical termini (3’ for all except 5’ of F1/B1).
3. **ROSALIND Coverage:** Uses a ROSALIND score of ≤ 3 to indicate coverage for any primer in a LAMP assay. Modified ROSALIND scoring evaluates individual sequences rather than using an incidence and prevalence approach.

Additionally, in multiplex assays, coverage is determined if at least one assay shows coverage. Coverage can be weighted based on global subtype prevalence.

- **ROSALIND Score:** Learn more [here](https://www.rosalind.bio/en/knowledge/calculating-the-severity-score-for-lamp-assays).
- **Alignments:** Extract sequences from Los Alamos National Labs (LANL) alignments or from GenBank IDs.
- **Outputs:** Determine coverage at the assay, primer, and nucleotide levels.

## Software Components

### Main Software Process
**Notebook:** `ChainLAMP_coverage_analysis_v3.4.ipynb`

1. **Coverage Software:**
    - **[1A] Setup for All Necessary Inputs:**  
      Set up the required inputs. Review the folder files to understand how assays and primers are denoted.
    - **[1B] Running the Coverage Analysis:**  
      Run this section to determine sequence coverage by primers. Complete setup in [1A] before running.

### Additional Software
**Notebook:** `ChainLAMP_coverage_analysis_v3.4_extension.ipynb`

1. **Sequence Library Generation:**
    - **[1A] Generate a Library of Sequences:**  
      Create a sequence library organized by subtype, which can be used as input for the main analysis pipeline. This process involves removing gaps from alignments and categorizing sequences by subtype.
    - **[1B] Generate Alignments with Year-Based Splits:**  
      Optionally split sequences by year. (Note: This capability is not available in this version.)
    - **[1C] Gather Sequences from GenBank IDs:**  
      Retrieve sequences from GenBank using their IDs for further analysis.

## Getting Started

### Prerequisites

- Python 3.11
- Jupyter Notebook
- Necessary Python packages (see `requirements.txt`)

### Running the Analysis

1. Open `ChainLAMP_coverage_analysis_v3.4.ipynb` in Jupyter Notebook.
2. Follow the instructions in the notebook, starting with section [1A] to set up your inputs.
3. After setup is complete, proceed to section [1B] to run the coverage analysis.

For generating a sequence library or working with GenBank IDs, follow the instructions in `ChainLAMP_coverage_analysis_v3.4_extension.ipynb`.

## Contributing

Contributions are welcome! Feel free to submit a Pull Request or report issues to help improve this software.

## Future Developments

Capabilities for inclusion of gaps in alignments is in progress. Please let me know if there is any additional developments that would be good to add.

## Contact

For questions, suggestions, or contributions, please contact [sgillig1@uw.edu](mailto:sgillig1@uw.edu).

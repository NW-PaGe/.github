# [Title]

## Build Overview
- **Build Name**: [Build Name]
- **Pathogen/Strain**: [Pathogen/Strain Name]
- **Scope**: [Scope or targeted region/gene segments]
- **Purpose**: This repository contains the Nextstrain build for [briefly describe the purpose of the build]
- **Nextstrain Build/s Location/s**: [Insert the URL for the Nextstrain build on Nextstrain Groups] [Insert another URL for instances when more than one Nextstrain build exists]

## Table of Contents
- [Scientific Decisions](#scientific-decisions)
- [Getting Started](#getting-started)
  - [Data Sources & Inputs](#data-sources--inputs)
  - [Setup & Dependencies](#setup--dependencies)
    - [Installation](#installation)
    - [Clone the repository](#clone-the-repository)
- [Run the Build](#run-the-build-with-test-data)
- [Repository File Structure Overview](#repository-file-structure-overview)
- [Expected Outputs](#expected-outputs)
- [Customization for Local Adaptation](#customization-for-local-adaptation)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Scientific Decisions
*(This section is dedicated to talking about the scientific decisions that were made in the development of the build to help others when making their own analyses or builds)*

Nextstrain builds are designed for specific purposes and not all types of builds for a particular pathogen will answer the same questions. The following are critical decisions that were made during the development of this build that should be kept in mind when analyzing the data and using this build. *Subsampling, root selection, and reference selection must be included at minimum.*

- **Subsampling**: [Describe subsampling strategy, focusing on regions, priorities, etc...]
- **Root selection**: [Describe the root selected for the build that mutations are called against]
- **Reference selection**: [Describe the reference selected for the build that was used in alignment]
- **Inclusion/Exclusion**: [Explain why certain sequences may or may not be included/excluded]
- **Other adjustments**: [Explain any other important adjustments]

## Getting Started
*(Provide any context new users should know before using this project.) Some high-level features and capabilities specific to this build include:*

- [Feature 1: Feature 1 is helpful because it allows for X]
- [Feature 2: Feature 2 is helpful because it allows for X]

### Data Sources & Inputs
*(Provide any information on data sources and the inputs needed to run the build)*
This build relies on publicly available data sourced from [data sources].

- **Sequence Data**: [Data sources]
- **Metadata**: [Metadata sources]
- **Expected Inputs**:
    - `[data_location]/sequences.fasta` (containing viral genome sequences)
    - `[data_location]/metadata.xls` (with relevant sample information)
- **Private data, if applicable**:

### Setup & Dependencies
#### Installation
Ensure that you have [Nextstrain](https://docs.nextstrain.org/en/latest/install.html) installed.

To check that Nextstrain is installed:
```
nextstrain check-setup
```

#### Clone the repository:

```
git clone https://github.com/[your-github-repo].git
cd [your-github-repo]
```

## Run the Build
*(Explain how to run the build with test data. Example text on how this might be explained is below)*

To test the pipeline with the provided example data located in `[data_location]/` make sure you are located in the build folder `[your-github-repo]` before running the build command:

```
nextstrain build .
```

When you run the build using `nextstrain build .`, Nextstrain uses Snakemake as the workflow manager to automate genomic analyses. The Snakefile in a Nextstrain build defines how raw input data (sequences and metadata) are processed step-by-step in an automated way. Nextstrain builds are powered by Augur (for phylogenetics) and Auspice (for visualization) and Snakemake is used to automate the execution of these steps using Augur and Auspice based on file dependencies.

### Test Data
For builds that do not programmatically pull data from NCBI or another source, include a `test_data/` folder containing a minimal working example of test data that can be successfully executed by the build.

## Repository File Structure Overview
*(This section outlines the high-level file structure of the repo to help folks navigate the repo. If the build follows the pathogen template repo feel free to make this section brief and link to the pathogen template repo resource)*

Example text below:

This Nextstrain build follows the structure detailed in the [Pathogen Repo Guide](https://github.com/nextstrain/pathogen-repo-guide).
Mainly, this build contains [number] workflows for the analysis of [pathogen] virus data:
- ingest/ [link to ingest workflow] Download data from [source], clean, format, curate it, and assign clades.
- phylogenetic/ [link to phylogenetic workflow] Subsample data and make phylogenetic trees for use in nextstrain.

OR

The file structure of the repository is as follows with `*`" folders denoting folders that are the build's expected outputs.

```
.
├── README.md
├── Snakefile
├── auspice*
├── clade-labeling
├── config
├── new_data
├── results*
└── scripts
```

- `Snakefile`: Snakefile description
- `config/`: contains what
- `new_data/`: contains What
- `scripts/`: contains what
- `clade-labeling`: contains what

## Expected Outputs
*(Outline the expected outputs and in which folders to locate them)*

After successfully running the build there will be two output folders containing the build results.

- `auspice/` folder contains: a .json file
- `results/` folder contains:


## Customization for Local Adaptation
 *[Brief overview on how to adapt this build for another jurisdiction, such as a state, city, county, or country. Including links to Readmes in other sections that contain detailed instructions on what and how to modify the files]*
This build can be customized for use by other demes, including as states, cities, counties, or countries.

## Contributing
For any questions please submit them to our [Discussions](insert link here) page otherwise software issues and requests can be logged as a Git [Issue](insert link here).

## License
This project is licensed under a modified GPL-3.0 License.
You may use, modify, and distribute this work, but commercial use is strictly prohibited without prior written permission.

## Acknowledgements

*[add acknowledgements to those who have contributed to this work]*

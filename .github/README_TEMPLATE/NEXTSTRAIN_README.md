# [Title]

## Build Overview
- **Build Name**: [Build Name]
- **Pathogen/Strain**: [Pathogen/Strain Name]
- **Scope**: [Scope or targeted region/gene segments]
- **Purpose**: This repository contains the Nextstrain build for [briefly describe the purpose of the build]
- **Nextstrain Build/s Location/s**: [Insert the URL for the Nextstrain build on Nextstrain Groups] [Insert another URL for instances when more than one Nextstrain build exists]

## Table of Contents
- [Getting Started](#getting-started)
  - [Data Sources & Inputs](#data-sources--inputs)
  - [Setup & Dependencies](#setup--dependencies)
    - [Installation](#installation)
    - [Clone the repository](#clone-the-repository)
- [Run the Build with Test Data](#run-the-build-with-test-data)
- [Repository File Structure Overview](#repository-file-structure-overview)
- [Expected Outputs](#expected-outputs)
- [Scientific Decisions](#scientific-decisions)
- [Customization for Local Adaptation](#customization-for-local-adaptation)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

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

## Run the Build with Test Data
*(Explain how to run the build with test data. Example text on how this might be explained is below)*

To test the pipeline with the provided example data located in `[data_location]/` make sure you are located in the build folder `[your-github-repo]` before running the build command:

```
nextstrain build .
```

When you run the build using `nextstrain build .`, Nextstrain uses Snakemake as the workflow manager to automate genomic analyses. The Snakefile in a Nextstrain build defines how raw input data (sequences and metadata) are processed step-by-step in an automated way. Nextstrain builds are powered by Augur (for phylogenetics) and Auspice (for visualization) and Snakemake is used to automate the execution of these steps using Augur and Auspice based on file dependencies.

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

## Scientific Decisions
*(This section is dedicated to talking about the scientific decisions that were made in the development of the build to help others when making their own analyses or builds)*

The following are critical decisions that were made during the development this build that should be kept in mind when analyzing the data.

- **Tiered subsampling**: [Describe subsampling strategy, focusing on regions, priorities, etc...]
- **Root selection**: [Describe the root selected for the build that mutations are called against]
- **Inclusion/Exclusion**: [Explain why certain sequences may or may not be included/excluded]
- **Other adjustments**: [Explain any other important adjustments]


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

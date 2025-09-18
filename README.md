# Introduction

This repository contains scripts and data used to aid the development of the [Medications Data Interoperability Project (MDIP)](https://mdip.eu/en), funded by the European Union via NGI Sargasso, Horizon Europe - Grant Agreement number 101092887.

# Data folder

This folder contains the **final** version of all drug catalogs under the European Union (excluding Germany and Greece as these regulators do not provide complete datasets). Some of the files provided by the regulators needed some standardization or conversion in order to be ingested by MDIP parsers.

# Data Scripts

As mentioned before, some of the files provided by the regulators needed some form of standardization or conversion. The scripts present under the data_scripts folder display the changes needed to be done on those files. Some of the scripts transform data spread across multiple files into a single processable file, while others enrich the data with ATC codes. Since the file with the full ATC collection is proprietary, we have omitted it from this repository.

# Auto Match

We have matched all drug catalogs against a set of pharmacogenomic drugs, provided by [Pillcheck](https://www.pillcheck.ca/medications/). We matched them using their ATC codes. In case there were no ATC codes, we matched them by name, using the active substance of the drugs. 

In the auto_match folder we have the resulting matches plus the matcher script. 
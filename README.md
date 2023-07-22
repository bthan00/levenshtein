# Levenshtein Distances for Primary key mapping

In this exercise, we will use [Ontario Data Catalog](https://data.ontario.ca/dataset/energy-use-and-greenhouse-gas-emissions-for-the-broader-public-sector), Broader Public Sector energy consumption data.

This dataset consists of multi-year excel files with no primary keys to uniquely identify each property. There exists a challenge in which property names may change over each reporting year. We will use Levenshtein distances to calculate the closest matching UUID's for a new year of reporting.

## Installation

`pip install -r requirements`

## Usage

Accepts two csv files (df1 UUID mapped, df2 unmapped). For the first reporting year, you will have to assign each year a UUID. We will then concatenate the `Operation Name`, `Address`, and `Operation Type` for each record and perform levenshtein distances for each record.

## Statistics

Compared to a manual 2 week business mapping for the 2017 School board sector, this script correctly mapped 77.7% of the properties in under two minutes. 

## Next Steps

The script to partition datasets is coming soon. It was originally written in Julia.
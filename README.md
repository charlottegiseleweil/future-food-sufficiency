# Future food sufficiency

## Getting Started

### Prerequisites

This code can be run using a working version of **Python 3.8** and **Jupyter notebook** but we recommend using the provided virtual environment with the **Anaconda** distribution.

If you do not have **Anaconda** installed, you can download the Python 3 version here: https://www.anaconda.com/distribution/


### Install the environment

A virtual environment that contains all the necessary libraries to run the code is provided to spare the user from having to install them one by one.


Install the **food_sufficiency** environment using:

```
conda env create -f food_sufficiency.yml
```

To activate the environment:

```
conda activate food_sufficiency
```

## Download the data

You can download the data from **Zenodo** following this link https://zenodo.org/record/3643209#.Xj2PkBNKjOR

## Contents

#### **Sufficiency.ipynb** 
Computes caloric sufficiency (global and country-scale) 


* Inputs:
  * data/outputs/with_irrig/compare/*: used to get calorie production 
  * data/inputs/Diet/*: used to get diet information


* Outputs:
  * data/outputs/with_irrig/sufficiency/country_sufficiencies_new.csv: the current and predicted sufficiency for each SSP at country scale
  * data/outputs/with_irrig/sufficiency/suff_map_new.csv: a file with country sufficiency used to create maps with QGIS

#### **CtryCalSuff_in_perspective.ipynb** 

Explores the country sufficiencies into perspective by adding related datasets: import independency, malnutrition, water security, GFSI and GNP per capita.

* Inputs:
  * data/outputs/related_datasets/sufficiencies_input.csv: a copy of the previously created country sufficiency file used as a baseline here
  * data/outputs/related_datasets/Food_security/*: GFSI by country data
  * data/outputs/related_datasets/Food_security/GNP_WorldBank_2018/*: GNP per capita data
  * data/outputs/related_datasets/import_independency/Matti_Kummu_2019/shp_trade_dep.gpkg: import independency data
  * data/outputs/related_datasets/Malnutrition/API_SH.STA.MALN.ZS_DS2_en_csv_v2_49604.csv: malnutrition data
  * data/outputs/related_datasets/Water_Security/GlobalWaterScarcity/*: water security data

* Outputs :
  * data/outputs/related_datasets/sufficiencies_added_data.csv: the country sufficiencies with the added external data
  * data/outputs/related_datasets/sufficiencies_full.csv: the country sufficiencies with extra data, results and corresponding category

## License

This code is under The MIT License (MIT)
Copyright (c) 2020 Charlotte Weil & Romain Caristan

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

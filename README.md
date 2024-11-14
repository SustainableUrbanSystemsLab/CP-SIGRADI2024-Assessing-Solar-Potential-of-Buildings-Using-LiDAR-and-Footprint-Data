# A Computational Framework for Assessing Solar Photovoltaic Potential of Buildings Based on LiDAR and Building Footprint Data

<p align="center"><img src="https://github.com/SustainableUrbanSystemsLab/Assessing-Solar-Potential-of-Buildings-Using-LiDAR-and-Footprint-Data/blob/main/Resources/methods%20overview.jpg" width="500px"></p>


## Abstract

The mass adoption of building-integrated photovoltaics (BIPV) emerges as a promising solution for reducing global greenhouse gas (GHG) emissions. However, using such systems to achieve net zero operational energy at the urban scale requires evaluating the solar potential of thousands of buildings which poses many challenges concerning data availability, quality, and privacy. To address these issues, we present an automated end-to-end framework for querying, combining, and processing publicly available aerial Light Detection and Ranging (LiDAR) and Building Footprint data. Using open-source algorithms for geometry reconstruction and solar radiation analysis, we show how to estimate the maximum annual direct current (DC) electricity yield per building. This framework is designed to enable urban planners, developers, and architects to assess the solar potential of neighborhoods and cities in an accessible way. By enabling effective communication of results, it can help optimize resource allocation and benefit solar adoption initiatives.

## Keywords

`BIPV, Performance-based design, Photovoltaic potential, Spatial data processing, Renewable energy, Urban planning`

## Author

- Name: [Silvia Vangelova](mailto:vangelova@ibi.baug.ethz.ch)
- LinkedIn: [Link](https://www.linkedin.com/in/silvia-vangelova-5ba9a4163/)
- Institution: Georgia Institute of Technology
- Program: M.S. Analytics (OMSA)
- Advisor: Dr. Patrick Kastner

## Repository Structure

- `Code/`: Directory containing the code, scripts, or notebooks used in the research.
  - `Grasshopper/`: Directory containing the grasshopper definition
    - `data/`: Directory containing data for the grasshoper script
  - `Notebooks/`: Directory containing notebooks
    - `images/`: Directory containing images produces from running the Notebooks
    - `data/`: Directory for storing data produced from running the Notebooks
- `Resources/`: Directory containing images used in this README.md file.
- `README.md`: This file, providing an overview of the thesis and repository.

## Instructions for reconstructing mesh geometry in Jupyter Notebook 

Environment set-up:
  - python -m venv env  
  - env\Scripts\activate
  - pip install -r requirements.txt

## Running the Solar Potential Analysis script in Grasshopper instructions

<p align="center"><img src="https://github.com/SustainableUrbanSystemsLab/Assessing-Solar-Potential-of-Buildings-Using-LiDAR-and-Footprint-Data/blob/main/Resources/Grasshopper%20canvas%20guide.png" height="400px"></p>

The grasshopper definition is developed in Rhino 8 SR10 (8.10.24228.13001, 2024-08-15) on Windows. For this version, there are certain issues when importing pandas (see forum discussion [here](https://discourse.mcneel.com/t/rhino-8-i-cant-import-pandas-in-rhinos-scripteditor/168547/32))

1. Before starting Grasshopper make, sure to **open** the *ScriptEditor* and **run** the following script to import *numpy*, *pandas*, and *laspy*:
   
    <img src="https://github.com/SustainableUrbanSystemsLab/Assessing-Solar-Potential-of-Buildings-Using-LiDAR-and-Footprint-Data/blob/main/Resources/select script editor.PNG" height="200px">

    <img src="https://github.com/SustainableUrbanSystemsLab/Assessing-Solar-Potential-of-Buildings-Using-LiDAR-and-Footprint-Data/blob/main/Resources/run script in editor.PNG" height="200px">

    Code snippet:

    ```python
    import locale
    import numpy
    locale.setlocale(locale.LC_ALL, 'en_US.UTF-8')
    import pandas as pd
    import laspy
    ```

3. To install Python packages in Rhino 8 you can either install them from the Terminal or use the ```# r: %package name%``` notation
   
   Using Terminal
      1. Open command prompt
      2. Navigate to script environment, e.g. run: ```cd "C:\Users\%UserName%\.rhinocode\py39-rh8\Scripts"```
      3. Instal packages, e.g. run ```pip install pandas```
   
   Using the ```# r: %package name%``` notation:
            
   <img src="https://github.com/SustainableUrbanSystemsLab/Assessing-Solar-Potential-of-Buildings-Using-LiDAR-and-Footprint-Data/blob/main/Resources/install and import package Rhino 8.PNG" width="300px">
       


    See also this [tutorial](https://developer.rhino3d.com/guides/scripting/scripting-command/#using-packages) for using packages in Rhino 8

5. To run the script make sure the following packages are installed and can be imported properly:
    ```python
    rasterio
    laspy
    lazrs
    laszip
    geopy
    scikit-learn
    scipy
    cgal
    requests
    rasterio
    geopandas
    osmnx
   ```


## Citation

```bibtex
@inproceedings{vangelova2024sigradi,
  title = {A Computational Framework for Assessing Solar Photovoltaic Potential of Buildings Based on LiDAR and Building Footprint Data},
  author = {Vangelova, Silvia and Kastner, Patrick},
  year = {2024},
  booktitle = {Proceedings of SIGRADI 2024},
  institution = {Georgia Institute of Technology},
  bibtex_show = {true},
  preview = {SIGRADI2024.png},
  isbn = 978-9915-9635-2-5
}
```

## Source

[Link](https://github.com/SustainableUrbanSystemsLab/Assessing-Solar-Potential-of-Buildings-Using-LiDAR-and-Footprint-Data) to this repository.

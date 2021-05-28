# plotProps

A MATLAB class to track the plot preferences.

## Requirements
Please check 'requirements.txt' for the software's dependencies.

## Installation
1. Download the software by clicking the dropdown menu 'Code' and click 'Download ZIP'.
2. Unpack the zip file and move the folder to your desired location.
3. Go to 'requirements.txt' and move the dependencies to the folder LifetimeAnalysis/bin/external
4. Open MATLAB and add the folder ("Add with subfolders") to your MATLAB path.

![image](https://user-images.githubusercontent.com/77492856/119955717-99be7300-bfa0-11eb-8c8a-0a6765b572dc.png)

The software is now ready to use.

## Usage

The plotProps class is meant as a superclass that provides functionality for plotting. The functionality so far is very limited. Declare plotProps as a superclass
```
classdef myCLass < plotProps
```
. The code can also be used stand-alone but has limited use here:
```
pl = plotProps();
```
check the default colormap
```
pl.colormap
```
and get 10 RGB values of the current colormap
```
cmap = pl.getColormap(10);
```
.

## Documentation

Type
```
doc plotProps
```
for the documentation or
```
help plotProps.getColormap
```
for the documentation of a specific function, which is the 'getColormap' function in this example.

If the plotProps class is a superclass of myClass, then use the 'getColormap' as follows
```
cmap = myClass.getColormap(10)
```
this is will result in the 10 RGB pairs of the colormap defined in 
```
myClass.colormap
```
.

## Project organization
- PG = project-generated
- HW = human-writable
- RO = read only
```
.
├── .gitignore
├── CITATION.md
├── LICENSE.md
├── README.md
├── requirements.txt
├── bin                <- Compiled and external code, ignored by git (PG)
│   └── external       <- Any external source code, ignored by git (RO)
├── config             <- Configuration files (HW)
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── src                <- Source code for this project (HW)

```


## License

This project is licensed under the terms of the [MIT License](/LICENSE.md)

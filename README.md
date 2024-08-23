# multi-gpr-soil

## Multi-target Gaussian Process Regression for Three-Dimensional Mapping: a geology test case in Seattle, WA

The purpose of this project is to develop a multi-target Gaussian Process Regression (GPR) model to predict engineering soil classification and soil layering in three dimensions. We will use a dataset of past subsurface investigations from Seattle, WA, to train and test the model. The project offers opportunities to explore gaussian processes, multi-target regression, machine learning model training and evaluation, two- and three-dimensional geospatial data management and visualization, Dask parallelization, and more. Enthusiastic team members of all experience and skill levels are welcome to join this project! 

### Collaborators

| Name | Personal goals | Can help with | Role |
| ------------- | ------------- | ------------- | ------------- |
| Morgan S. | I want to work towards three-dimensional ML predictions  | I can help with understanding our dataset, methods, programming in python  | Project Lead |
| Mansa K. | I want to learn and gain more experience with Gaussian Process Regression. | I can help with Python programming, version control (git), and general machine learning techniques | Hackweek Helper |
| Steven P. | I want to learn about Gaussian Process Regression and about Seattle subsurface geology! | I can help with git and python | Team Member |
| Brendan M. | I would like some exposure to ML techniques | I can help with vibes and training and standardizing the model | Team Member | 
| Hailey S. | I want to learn about Gaussian processes and how to migrate workflows to the cloud. | I can help with raster data and general machine learning theories. | Team Member |

### The problem

Subsurface geological data is essential for a variety of engineering and environmental applications, including site characterization, geotechnical engineering, and groundwater modeling. In dense urban areas, such as Seattle, many subsurface investigations have been performed in past projects that could be leveraged to inform conceptual infrastructure design, urban planning, augment modern subsurface investigations, and more. Traditional methods for site soil classification and layering in three dimensions involve manual interpretation of borehole logs and other available surface and subsurface data. Machine learning methods, such as Gaussian Process Regression, offer a way to automate this process and provide predictions at a higher resolution than traditional methods. In this project, we will develop a multi-target Gaussian Process Regression model to predict engineering soil classification and soil layering in three dimensions.

## Data and Methods

### Data

The Washington State Department of Natural Resources (DNR) maintains a databse of various geologic data for the state, including geology maps, lidar surveys, subsurface investigations, and more. This data is accessible through an interactive web application called the [Geologic Information Portal](https://www.dnr.wa.gov/geologyportal) and is available for [download](https://www.dnr.wa.gov/programs-and-services/geology/publications-and-data/gis-data-and-databases). For this project, we will focus on the borehole logs within the subsurface investigations dataset. The borehole logs contain information about the soil layers and engineering soil classification at various depths, and we will be using the USCS soil classification data to train and test our model. Depending on time and computing restraints, we may limit model implementation to a small region around the University of Washington.

![image](/figures/screenshots/dnr_ui.png)  

### Existing methods

Traditional methods for predicting soil classification and layering in three dimensions involve manual interpretation of borehole logs and geophysical surveys. Machine learning methods, such as Gaussian Process Regression, offer a way to automate this process and provide predictions at a higher resolution than traditional methods. Gaussian Process Regression is a non-parametric method that can be used for regression and classification tasks, and it is particularly useful for modeling spatial data. In this project, we will use a multi-target Gaussian Process Regression model to predict soil classification and layering in three dimensions.

### Proposed methods/tools

We will train a [multi-target Gaussian Process Regression model](https://link.springer.com/article/10.1007/s10994-022-06170-3) for the city of Seattle, and publish the model in a way so that it can be used by others.  

We will create a [model card](model-card.md) for the machine learning model used in this project in accordance with the [Hugging Face model card standard](https://huggingface.co/model-cards).

### Optional exploratory and background information for reference

As time and interest allow, you may explore the following resources in preparation for (and/or during) the hackweek:
1. Familiarize yourself with the available subsurface investigation data via the [Geologic Information Portal](https://www.dnr.wa.gov/geologyportal).
2. Use the `1-data-access.ipynb` notebook to download and explore the subsurface investigation data.
3. Introduce yourself to [Gaussian Process Regression](https://scikit-learn.org/stable/modules/gaussian_process.html#gaussian-process-regression-gpr) and explore using [visualization tools](http://www.infinitecuriosity.org/vizgp/).
4. Explore [2D GPR in sci-kit learn](https://jamesbrind.uk/posts/2d-gaussian-process-regression/). 
5. Learn about multi-target regression and [multi-output Gaussian Process Regression](https://link.springer.com/article/10.1007/s10994-022-06170-3).

## Project goals and tasks

### Project goals

**TBD!!**

### Tasks

* Monday:
  * GitHub (edit README table of team members)
  * run notebook 1 (data access)
* Tuesday & Wednesday:
  * re-run notebook 1 and notebook 2 (data access and predictor sampling)
  * GPR Tutorial (Mansa)
  * sci-kit learn GPR (on small toy dataset of UW campus area)
    * notebook 2: sample predictors
    * notebook 3: sci-kit GPR
      * notebook 3.1: classify-soil
      * notebook 3.2: regress-thickness
  * pytorch GPR - notebook 4
    * for multi-output, 2D
  * custom loss function for classifier
* Thursday & Friday:
  * dask parallelization (of pytorch?)
  * improve model performance?
    * additional predictors (e.g. geomorphon, VS30)
    * hyperparameter tuning
    * cross-validation
    * class imbalance
  * custom loss function implementation
  * Seattle-scale implementation / visualization 

## Project Results

**TBD!!**

## Files and folders in this project repository

* **`contributors/`**
<br> Each team member can create their own folder under contributors, within which they can work on their own scripts, notebooks, and other files. Having a dedicated folder for each person helps to prevent conflicts when merging with the main branch. This is a good place for team members to start off exploring data and methods for the project.
* **`notebooks/`**
<br> Notebooks that are considered delivered results for the project should go in here.
* **`scripts/`**
<br> Code that is shared by the team should go in here (e.g. functions or subroutines). These will be files other than Jupyter Notebooks such as Python scripts (.py).
* `.gitignore`
<br> This file sets the files that will be globally ignored by `git` for the project. (e.g. you may want git to ignore temporary files or large data files, [read more about ignoring files here](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files))
* `environment.yml`
<br> `conda` environment description needed to run this project.
* `README.md`
<br> Description of the project (see suggested headings below)
* `model-card.md`
<br> Description (following a metadata standard) of any machine learning models used in the project

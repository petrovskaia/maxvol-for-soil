# maxvol-for-soil-sampling
Repository for paper "Optimal soil sampling design based on the maxvol algorithm".

You can find an example on Kursk site in Google Collab 

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Qqcpmo09lSwbpfpox2o0QZi4ATBllFyH?usp=sharing)

If you want to use maxvol soil sampling in your project, visit the main repository

https://github.com/EDSEL-skoltech/maxvol_soil_sampling

### How to start with `maxvol` for  soil sampling

1) clone this repo
 
`git clone https://github.com/petrovskaia/maxvol-for-soil-sampling.git`

2) create new `conda env` from `yml` file 

`conda env create -f py3_maxvol_soil.yml`

3) activate it 

`conda activate maxvol_soil_sampling`

4) select points from command line

`python maxvol_points_selection.py --max_n_pnts MAXIMUM_NUMBER_OF_POINTS --min_n_pnts MINIMUM_NUMBER_OF_POINTS --wd WORKING_DIRECTORY`

!!Working directory must contain folder named 'features'.

If directory of dem is not specified, working directory must contain digital elevation model named 'dem.tif'.

#### Optional arguments:

--dem_dir Directory of DEM 

--data_m Mode for data preparation[0,1,2,3]:

            0 - raw data
            
            1 - normed data
            
            2 - unnormed data with coordinates as features
            
            3 - normed data with coordinates as feature 
            
 --dist_pts Distance between points[0.0 - 1.0]
 
 --dist_brd Distance from borders[0.0 - 1.0]

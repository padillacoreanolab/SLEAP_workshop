# Creating H5 File from a .slp file
1. open sleap GUI
2. download BOTH (1) sleap dataset file (.slp) and (2) original video (.mp4) into the parent folder of your SLEAP env
3. go to File > Open project... > and click the .slp file you wish to work with
4. if you did not work on this project previously, SLEAP will look for the video using the same pathway that the previous person who worked on this project used. This will not be the pathway you need so this will throw on error. Double click on the pathway in the pop up window, find the .mp4 file with the video that you want to work on that you saved into your SLEAP folder, and the video should open with labeled skeleton in the SLEAP gui. 
5. PROOFREAD the tracking before moving forward: go frame by frame to make sure tracks (identities) don't switch and extra tracks are not added 
6. Give each track a descriptive names (i.e. mouse IDs such as 2.4) if they do not already have by doulbe clicking the track name (colored text under "Track" in the right menu
7. click File > Save
8. Convert the .slp file with corrected tracking and discriptive names to an h5 file by clicking File > Export Analysis HDF5... and save the h5 file where you want it

# Getting Ready to Analyse 
1. using the terminal window, create a new virtual environment for your anaylsis using the code below

# installing 
```
conda deactivate
conda create -p ./_python python=3.9 -y
conda activate ./_python/
# Jupiter Notebooks
conda install -c conda-forge notebook -y
# binary format library for h5 files
conda install -c conda-forge h5py -y
# numpy 
conda install -c conda-forge numpy -y
# scipy 
conda install -c conda-forge scipy -y
# matplotlib
conda install -c conda-forge matplotlib -y
# pandas
conda install -c conda-forge pandas -y
# seaborn
conda install -c conda-forge seaborn -y
```

6. open up a new jupyter file in the folder you are working on, make sure you are connected to the right kernel (kernel that references the python in conda, version of python should match the version you have in the conda environment and reference anaconda3 in the pathway) and also connected to jupyter notebook's remote server (using the terminal activate conda environment you just created, and then type jupyter notebook, bottom in the blue ribbon it should say jupyter servor: remote)
refer to https://sleap.ai/notebooks/Analysis_examples.html 
7. copy and paste code from the website and insert filename for the h5 anaylsis file you created (full pathway)


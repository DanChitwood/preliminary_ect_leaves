# preliminary_ect_leaves
a repository for preliminary analysis of leaf shape using ect (Euler characteristic transform)

leaf shape data, modified to be ordered contour data and saved as `.npy` files, here: https://figshare.com/articles/dataset/Modified_leaf_shape_contour_data/25435936/1

plant family metadata associated with the Leafsnap and Transect datasets can be found at the following link: https://figshare.com/articles/dataset/LeafMorphospace/4985561/1?file=8392724. the specific file used here to retrieve plant family data is `./LeafMorphospace/Analysis/2.PHYLO_analysis_Figure4/PHYL_sha_desc.txt` and will need to be added to the home directory.

note: there are two different functions explored for calculating distances between ECTs, one is at the end of the notebook

the calcultion of the ect and using a cnn is from this tutorial: https://github.com/MunchLab/ECT-Leaf-CNN/blob/main/leaf-example-tutorial/Tutorial-ECT_for_example_dataset.ipynb

### for analysis by groups
create the following folder structure within the home directory, a folder for the ect analysis and sub-folders for outline inputs and ect outputs.

+--group_ect_analysis  
|    +--outline_input  
|    +--ect_output  

additionally, add dataloaders.py, models.py, and utils.py scripts from the github [repository](https://github.com/MunchLab/ECT-Leaf-CNN/tree/main/leaf-example-tutorial)

Within the dataloaders.py file, change the image_path in the create_datasets() function:
- from '/example_data/ect_output/'
- to '/group_ect_analysis/ect_output/'

### for analysis by plant family
create the following folder structure within the home directory, a folder for the ect analysis and sub-folders for outline inputs and ect outputs.

+--phylo_ect_analysis  
|    +--outline_input  
|    +--ect_output  

additionally, add dataloaders.py, models.py, and utils.py scripts from the github [repository](https://github.com/MunchLab/ECT-Leaf-CNN/tree/main/leaf-example-tutorial)

Within the dataloaders.py file, change the image_path in the create_datasets() function:
- from '/example_data/ect_output/'
- to '/phylo_ect_analysis/ect_output/'

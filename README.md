# Dsprite Color Dataloader
## Basic Information
This dataset is the extension of the [dsprite]("https://github.com/deepmind/dsprites-dataset"). It contain all the image in previous dataset, but with the addition of the color.
### Detail
- image shape: (64, 64, 3)
- color label: red green blue
- shape label: circle heart square 

## Useage
First download the dsprite data from [here](""), and put the dataset in the same folder as this script.    
Then run the script with the following command:
```
data_loader=dsprite_color(balance_matrix=np.ones((3,3)))
```
`balance_matrix` is a 3x3 matrix, each row represents the ratio of usage in each class. The first dimension is the color and second is the shape. The value should be between 0 and 1. (1 means use all the data and 0 means use none.) User can define the ratio of each class.  
`return` The data loader object return 3 tensors: `image`, `shape`, `color`



Assignment Score: [0.029835257391146116, 0.9916]

Group Members:
Pranav Piyush - https://github.com/fatsoengineer/EIP_Week_1


## Convolution:
 
 Convolution is the process or method by which we try to project or extract the features or information of multiple pixels onto one pixel which can be also called as receptive field on the pretext that one pixel contains the the information of the multiple pixels the convolution was applied on, using which they could possibly extract edges and gradients to define distinct features, which in turn helps the neural network to define the combination of edges and textures required to define an object. It combines the image matrix (values ranging between 0-1 after standardization) and the kernel matrix (randomly initialized).


 ## Filters/Kernels
Filters/Kernels is a N*N matrix which contains information of a particular features/edges/textures/parts/ objects. They distinguish and filter out distinct edges and features. They are randomly initialised and updated after every epoch.


## Epochs
Epoch is the number of times the entire training set is used to update the weights of the kernel. After every epoch, the loss is calculated and back-propogation is done to reduce the loss, update the weight and refine the model.


## 1*1 Convolution

1x1 matrix is used to reduce/increase the no of channels of an NxNxM matrix, where M is the no of channels. It mainly focuses on one pixel rather than the surrounding pixel to reduce the number of channels, hence providing more accurate features.


## 3*3 Convolution

3x3 Convolution is an operation which extracts the features or information of 3x3 pixels onto 1x1 pixel which can be also called as receptive field on the pretext that one pixel contains the the information of the multiple pixels the convolution was applied on, using which they could possibly extract edges and gradients to define distinct features.


## Feature Maps

Feature maps are the end-result of filters to an input or intermediate images which helps us to identify the distinct features the neural network has detected after certain layer.


## Activation Function

Activation function clips the outlier weights to normalise it within certain range and then adds a bias to the weight.

## Receptive Field

Receptive Field is the culmination of information/features of N*N kernel matrix. Global Receptive Field of the last layer must atleast be equal to the size of the object. Also, the Local Receptive Field is equal to the size of the kernel. For every 3x3 Convolutional Layer, the Global Receptive Field increases by 2 (3x3 -> 5x5 -> 7x7 -> 9x9 and so on) while the Local receptive field remains constant at (3x3).

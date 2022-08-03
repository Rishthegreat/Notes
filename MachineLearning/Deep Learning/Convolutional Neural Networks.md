**Convolutional Neural Networks**

- To the CNN, a black and white image that is 2 x 2 is a 2d array with each value being $0\le$ pixel value $\le255$
	- Then the computer is able to work with the image
- To the CNN, a colored image that is 2 x 2 is a 3d array because of rgb
- ![[Pasted image 20220803180534.png]]
	- Convolutional operation
- ![[Pasted image 20220803180859.png]]
	- You take the Feature Detector aka Kernel aka Filter and apply it to the image
		- Usually the Filter is 3 x 3 but some use 5 x 5, etc
	- You match the 3 by 3 sqaure to the filter to see if the pixels match
		- The number of pixels that match up is the nuber you put in the feature map aka convulved feature aka activation map
	- The stride is the number of pixels that you move then you take the next set of pixels to compare
	- The goal of this step is to make the image smaller to make the processing faster and also to detect certain features
	- We create multiple feature maps to obtain our first convolutional layer
		- ![[Pasted image 20220803182134.png]]
	- A ReLU Layer is applying the rectfier function to the pixels in the feature map. This gets rid of all the negative values and increases non-linearity

- Max Pooling
	- The neural network should be able to find features even if they are distorted. Eg - A cheetah looking in a different direc




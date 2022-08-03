**Convolutional Neural Networks**

- To the CNN, a black and white image that is 2 x 2 is a 2d array with each value being $0\le$ pixel value $\le255$
	- Then the computer is able to work with the image
- To the CNN, a colored image that is 2 x 2 is a 3d array because of rgb
- ![[Pasted image 20220803180534.png]]
	- Convolutional operation
	- Below is the intuitive way to look at this equation
- ![[Pasted image 20220803180859.png]]
	- You take the Feature Detector aka Kernel aka Filter and apply it to the image
		- Usually the Filter is 3 x 3 but some use 5 x 5, etc
	- You match the 3 by 3 sqaure to the filter to see if the pixels match
		- The number of pixels that match up is the nuber you put in the feature map aka convulved feature aka activation map
	- The stride is the number of pixels that you move then you take the next set of pixels to compare
		- Usually the stride is set to 2
	- The goal of this step is to make the image smaller to make the processing faster and also to detect certain features
	- We create multiple feature maps to obtain our first convolutional layer
		- ![[Pasted image 20220803182134.png]]
	- A ReLU Layer is applying the rectfier function to the pixels in the feature map. This gets rid of all the negative values and increases non-linearity. Not everything can be modelled linearly, so we need to intorduce non-linearity. Mathematically, if all we use is linear functions, then the neural network is basically just 1 linear equation which is useless in complex applications.


- Pooling aka downsampling
	- The neural network should be able to find features even if they are distorted. Eg - A cheetah looking in a different direction, under different lighting and in a different part of the image
	- Max Pooling (One type of Pooling)
		- ![[Pasted image 20220803190215.png]]
		- We take the feature map and select a box size such as 2 x 2 and a stride and then you look at the pixels in the box, select the maximum value, record it and then move on according to the stride
		- We are getting rid of information that we do not need (Features that do not show up in the feature map)
			- By taking the maximum, we are also taking into account of distortion
				- In the Cheetah example, if the feature in another cheetah is slightly positioned to the right, we still detect it
			- We are reducing the chances of overfitting in the neural network
	- ![[Pasted image 20220803190618.png]]
		- This is what we have done so far

- ![[Pasted image 20220803191153.png]]
	- The 




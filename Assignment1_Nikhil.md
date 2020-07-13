
Just as complex organisms  like us are collection of single cells which combined together to do complex functions like lying on bed all day, day dreaming about getting 6 pacs, drunk calling your ex

 Let me dig down into drunk calling, you need to open your poison using hands, drink it using mouth, stomach for digesting it (or for throwing out, weaklings :P) and heart to pump that purified blood all the way to brain (Go CORONA) which helps us making these smart decisions. 
 
 **Channels**
There are different organs involved in this above action, each organ has a purpose. Similarly each channel is mapped to a particular feature.
Eg: In an english text there can be 52 different channels. (26 to detect lowercase rest for upper)
Feature: A organ is a group of cell working towards a particular function. Similarly a basic feature can be lines, curves, edges and gradients

Channels are collection of feature, just as shown in the images below an eye is a feature, and a collection of eye is channel

**Kernels**
Kernels also known as filters, feature detectors helps to identify whether the feature channel is looking out for is present in the data or not. In my channel is looking out for feature eyes, and when it finds an image has eyes, it sends out a high value otherwise a low value. Hence the name feature detector.

An interesting mathematical concept is two numbers when multiplied with each other gives maximum value when they are closer to each other and minimum value when farthest from each other when their sum is same.
To prove my point
(9 x 9 = 81) and  (9 + 9 = 18) **Closest**
(10 x 8 = 80) and (10 + 8 = 18)
(17 x 1 = 17) and (17 +1 = 18) **Farthest**

Matrix Dot product is done with channels and their kernels, if the value comes out to be higher, the feature is belived to be present in data.



**How are kernels initialized?**

Machine learning works on principle **Make mistakes to correct them**, in case of supervised learning, we always initialize our kernel with random values, and then we compare this result with the actual value to calculate the error.
As the values are initialized randomly, we are bound to do some errors. Hence we make small yet significant changes in those errors until we found the model to be making less mistakes.

**What happens during the training of a DNN?**

Lets suppose we are training a DNN  for image classification, our goal is to classify these images lets say Cats vs Dogs, we have labelled images as our dataset. Now we work on the above principal, **Make mistakes to correct them**

- First we need to convert our images into the forms our models can understand i.e. array of numbers.
- So these images are then passed into our model, a neural network architecture is shown below. The nodes in hidden layers are also called channels. Each channel as explained the is expert on a specific task 
- Initial layers would idenfity edges, gradients, patters, the deep layers would detect parts of objects (eyelashes, nails, whiskers) and objects (Face, legs, torso). Hence the channel looking our for that feature, and it it finds it the node gets activated.
- Final layer sums up all the information (activation of previous nodes) collected by the earlier layers and gives a prediction. 
 Eg:
	(2 eyes, nose, 4 legs, whiskers, pointy ears, mean AF --> Cat)
	(2 eyes, pointy nose, 4 legs, ears, Loving AF --> Dog)
	

- When initialized with random values, the nodes are bound to make errors, . But then comes the part where we correct these mistakes. 
- The error is then propogated backwards into the model to minimize them in small yet significant steps also known as backprop. 

**Why should we (nearly) always use 3x3 kernels?**
Applying a 3x3 kernel is preferred a 1x1 filter is like reading each pixel and no downscaling in the convolution process, each pixel returns as it is, hence it could be too computation heavy.

Applying a 5X5 filter, this means we have too many parameters to deal with (5 X 5 = 25), and too much information might be lost in the convolution process.
Hence 3 X 3 sits in the middle and to eliminate the problems to eliminate the above issues.

**How many times to we need to perform 3x3 convolutions operations to reach close to 1x1 from 199x199 (type each layer output like 199x199 > 197x197...)**

We have to perform the computation 100 times, every time when 3*3 computlation is performed as explained above, 
(199 x 199) > (197 x 197) > (195 x 195) > (193 x 193) > (191 x 191) > (189 x 189) > (187 x 187) > (185 x 185) > (183 x 183) > (181 x 181) > (179 x 179) > (177 x 177) > (175 x 175) > (173 x 173) > (171 x 171) > (169 x 169) > (167 x 167) > (165 x 165) > (163 x 163) > (161 x 161) > (159 x 159) > (157 x 157) > (155 x 155) > (153 x 153) > (151 x 151) > (149 x 149) > (147 x 147) > (145 x 145) > (143 x 143) > (141 x 141) > (139 x 139) > (137 x 137) > (135 x 135) > (133 x 133) > (131 x 131) > (129 x 129) > (127 x 127) > (125 x 125) > (123 x 123) > (121 x 121) > (119 x 119) > (117 x 117) > (115 x 115) > (113 x 113) > (111 x 111) > (109 x 109) > (107 x 107) > (105 x 105) > (103 x 103) > (101 x 101) > (99 x 99) > (97 x 97) > (95 x 95) > (93 x 93) > (91 x 91) > (89 x 89) > (87 x 87) > (85 x 85) > (83 x 83) > (81 x 81) > (79 x 79) > (77 x 77) > (75 x 75) > (73 x 73) > (71 x 71) > (69 x 69) > (67 x 67) > (65 x 65) > (63 x 63) > (61 x 61) > (59 x 59) > (57 x 57) > (55 x 55) > (53 x 53) > (51 x 51) > (49 x 49) > (47 x 47) > (45 x 45) > (43 x 43) > (41 x 41) > (39 x 39) > (37 x 37) > (35 x 35) > (33 x 33) > (31 x 31) > (29 x 29) > (27 x 27) > (25 x 25) > (23 x 23) > (21 x 21) > (19 x 19) > (17 x 17) > (15 x 15) > (13 x 13) > (11 x 11) > (9 x 9) > (7 x 7) > (5 x 5) > (3 x 3) > (1 x 1)




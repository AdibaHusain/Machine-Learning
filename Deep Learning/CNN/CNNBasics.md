**WHY WE USE CNN FOR IMAGES RATHER THAN ANN?**

If we try to process images through ANN then each pixel will be considered as an input and there are thousands and lakhs of pixels of image.

so these 2d matrix pixels in converted into 1D matrix for the sequential input.

suppose there is 32x32 matrix, so total of 1024 inputs and suppose there are 100 neurons then there would be 102400 weights at the first layer itself.

that's why we don't use it:

1. high computational power
2. spatial arrangement is missing(hume pta nhi rhta har  dsure element ke beech ka ky diff hai)
3. Overfitting





**WOKRING OF CONVOLUTIONAL LAYER:**

1. Convolutional Layer:

A filter is created which is like fixed size window that slide over the image and extract the major features from the image. It can be edges, textures.

Har type ki edges ko identify krne ke liye alag a;ag filters hote hain.

ISSE FEATURE CREATE HOTE HAIN



2\. Pooling Layer:

here we view the the same image from previous step on a bigger scale not every tiny pixel but collectively watching things.

tod ke ek tareke element ko separate krta hai

remove faltu ki cheeze



yh dono layers multiple times aati hain for better detailing.



3.Fully Connected Layer:

collectively cheezo ko dekh ke predict krte hain what is image all about.



We have 2 scales:

1. **Grey Scale:**

White and black ka combination hota no other colors.

**2. RGB Scale:**

isi ke combo se sare colors bnte.



cnn inhi colors ke strong points Jha dikhata voh edge maani jaati hai.





**WHY WE NEEDED PADDING?**

Understand one more thing, when you apply one pair of convolutional layer the quality of image decreases, like image of 5x5 and filer of 3x3 then the resultant image would be of 3x3.

and also the and the first and the last row don't comes under filter more oftenly as compared to other rows.

we make the image as (n-m+1).



**STRIDES:**

Stride batata hai ki filter/kernel ek step me kitne pixels move karega.

| Stride | Effect                                                |

| ------ | ----------------------------------------------------- |

| 1      | More detailed features capture hoti hain              |

| 2      | Output size reduce hoti hai, computation kam hoti hai |

| 3+     | Bahut information skip ho sakti hai                   |



&#x20; 



**MORE ABOUT POOLING:**

The feature map that we get after applying filter is reduces here in pooling, because after every filter multiple features will be generated with larger size and there will be storage issue that's why pooling is used.

Yaha we decide our size

aur stride (move after every pixel)

and the type of pooling:

1 MAX (select max element from specific size, dominant features captured)

2 MIN (select min element from specific size)

3 AVG (select avg element from specific size)




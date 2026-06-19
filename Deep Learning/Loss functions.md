**1. Loss Function**

Ek single training example (data point) ke liye error measure karti hai.

Batati hai ki model ka prediction actual value se kitna galat hai.



Example:



Actual value = 10

Predicted value = 8

Mean Squared Error (MSE) loss:



Loss=(10−8)

2

=4

Yeh sirf ek sample ka loss hai.





**2. Cost Function**

Puri dataset ke losses ka aggregate (usually average) hoti hai.

Training ke dauran optimizer isi cost ko minimize karne ki koshish karta hai.

Agar losses hain:

4, 9, 1, 16



To cost:



Cost=

4+9+1+16/4

=7.5

Yeh overall model performance dikhati hai.





AB EK CHEEZ DEKHO

JAB EPOCH CHLTE HAIN TOH JAISE 100 ROWS HAIN TOH 1 EPOCH ME HAR ROW FORWARD AUR BACKWARD DONO CHLEGA



BATCH SIZE USE HOTA HAI MATLAB EK GO ME KITNE ROWS TUM BHEJ SKTE ISSE TOH PROCESS THODA FAST HO JAAYEGA



**REGRESSION LOSS FUNCTIONS**

**MSE:**

MSE=1/N​∑(ytrue​−ypred​)^2

Training ke liye bahut commonly use hota hai

Neural networks mein optimize karna easy hota hai

Outliers se bahut affect hota hai

Unit square ho jati hai (people², meter² etc.), interpretation difficult



**MAE:**

Yaani actual aur predicted value ka difference lo, uska absolute value lo, aur average nikal do.

Easy to understand

Original unit mein hota hai

Outliers se kam affect hota hai



**Huber Loss:**

Use both MSE and MAE

Small error: MSE

Large error: MAE



**CLASSIFICATION LOSS FUNCTION**



**Binary Cross Entropy:**
If you use sigmoid as a activation function in output layer then you use this function kyuki sigmoid gives values between 0 anf 1 and binary corss entropy is also binary based



&#x20;**Categorical Cross Entropy:**

When you use softmax function as activation function and the output is not binary like you have options like cat,dog,bird. so softmax give values either 0 or 1, to decide the class for the output.

Yahan label one-hot encoded form mein hota hai.



**Sparse Categorical Cross Entropy:**

Yahan label ko one-hot banane ki zarurat nahi.





# Fake human face generator using GANs

This little personnal project is about using GANs to generate fake human faces. \
I have previously generated fake handwritten digits using the MNIST dataset, and in this project I learned how to generate images in color
(the digits were in grayscale), and how to deal with resolution.
# 
I used for this project the CelebA dataset, which contains 202,599 faces images. I did not use any of the annotations 
provided, since the discriminator only determines if an image is fake or real. \
I used a function to rescale the images and to store the resulting array in a .npy file, in order to import it afterwards on Google Colab.\
First, I tried using 64x64 pictures, but the file was too big and my neural network used too much RAM on Colab, so I had 
to use 32x32.
#
After using 32x32 images and training my GAN for 20,000 epochs, I was not satisfied with the results (resolution too low and poor results), 
so I went back to 64x64, training (took about 1hr) this time my GAN for 2,000 epochs, after tuning the hyperparameters (I tried several learning rates for 
the optimizer, and I also compared the results between RMSProp and Adam).\
Here is a preview of what the rescaled data lookes like:
<a href="https://ibb.co/JqNwHVJ"><img src="https://i.ibb.co/pQgBdcF/download.png" alt="download" border="0"></a>


## Results

Here are the fake faces generated for 2,000 epochs:
\
![alt-text](https://github.com/dalilr/face_generator_gan/blob/master/visages_generes.gif)

#
I am quite satisfied with the results, which look good after the 1100th epoch, considering this is only the second time I implement 
a generative adversarial network, and with (very) limited computational resources.

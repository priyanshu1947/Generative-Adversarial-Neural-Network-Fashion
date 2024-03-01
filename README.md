# Generative-Adversarial-Neural-Network-Fashion

![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/6f8a8670-d421-4bfd-9c67-958f2ff7ed9b)


## Project Overview

 Generative Adversarial Networks (GANs) are a class of deep learning models that have revolutionized the field of artificial intelligence. They consist of two neural networks—the generator and the discriminator—that engage in a fierce battle to create and distinguish realistic data. In our case, we’ll use GANs to generate fashionable clothing items like shoes, T-shirts, and bags.

**Libraries and Dependencies**

    TensorFlow: Our trusty deep learning framework.
    Keras: A high-level API for building neural networks.
    Matplotlib: For visualizing our results.
    NumPy: To handle numerical operations.
    Fashion MNIST Dataset: Our source of fashion images.

**Data Description**

Fashion-MNIST is a dataset of Zalando’s article images. It comprises a training set with 60,000 examples and a test set with 10,000 examples. Each image is a 28x28 grayscale representation associated with a label from 10 classes. The dataset serves as a benchmark for evaluating machine learning algorithms in the context of fashion image classification.

## Steps Involved: 

**1. Load the Data**
We’ll start by using the Fashion MNIST dataset. This dataset contains grayscale images of various clothing items, each represented as a 28x28-pixel image. TensorFlow’s dataset APIs (TFDS) make loading the data a breeze.
![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/a8469dc1-5980-4d62-bde8-ae9a93317da7)
![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/f454a9af-5056-4080-974e-079f99adf073)



**2. Build the Generator**
The generator is like an artistic painter. It takes random noise (usually 128-dimensional vectors) and transforms it into a fashionable masterpiece. Here’s how we construct it:

* **Input Layer:** A dense layer reshapes the random noise into an initial image representation (e.g., 7x7x128).
* **Upsampling Layers:** Gradually increase the resolution of the image using upsampling techniques.
* **Convolutional Layers:** Enhance features and add complexity to the generated image.
  ![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/b0822d1f-db7c-4593-b67a-911ba9d74e0b)
  ![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/2317d157-43b0-490d-adb1-5766f20ff621)


**3. Build the Discriminator**
The discriminator plays the role of a fashion critic. It evaluates both real and generated images and assigns a probability score (ranging from 0 to 1) to each. Here’s how we construct it:

* **Input Layer:** Accepts images (real or generated).
* **Convolutional Layers:** Extract features from the images.
* **Flatten Layer:** Converts the 2D feature maps into a 1D vector.
* **Dense Layer:** Produces the final probability score.

![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/7f9c5436-f723-4a2f-816c-9dddaaa1932b)
  
**4. Training Loop**

* **Training the Discriminator:** Teach it to distinguish real from fake images effectively.
* **Training the Generator:** The generator aims to fool the discriminator by generating realistic images.
![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/ebd47119-8c2d-4e23-8eef-bafa1c343ebc)

**5. Test the Generator**
After training, we unleash our generator. It takes 128 random variables and produces an image.
![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/6d30a3c2-89b0-46fe-858d-d3692b48620d)
![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/5e194118-b3a3-4b99-903f-47cf0ef2b045)



## Results
Our GAN will learn to create stunning fashion pieces—shoes, T-shirts, bags, and more. The generated images will be eerily realistic, showcasing the power of adversarial training.

![image](https://github.com/priyanshu1947/Generative-Adversarial-Neural-Network-Fashion/assets/70458921/b6132731-18cd-4701-bac5-7edaf790db3b)

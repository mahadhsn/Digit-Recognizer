# Digit-Recognizer
### Project Description
In this project, I decided to utilize the `mnist` dataset to create a `Convolutional Neural Network` (CNN) with 8 layers leading to a `99.3%` accuracy in recognizing digits ranging from `0-9`. For <b> data visualization </b>, I implemented `Matplotlib`.

As my first ever AI program, I would say it was a success as it gave me a good understanding of how to use <b> Tensorflow, Matplotlib </b> and much more.

### Libraries
- <b>`Tensorflow`</b>: To create the <b> 8 layered CNN </b>
- <b>`Numpy`</b>: Mainly to M <b> manipulate the mnist dataset </b> and make it easy to work with
- <b>`Matplotlib`</b>: For <b> data visualization </b>
- <b>`Random`</b>: To display random results from our testing set

### Code Structure
Since this program was written in <b> Jupyter Notebook </b>, no classes were used. However, the code is divided in an organized manner allowing for ease of use. (Most of the code is also commented making it very easy to understand.)

- <b> `AI` </b>: This program uses `Tensorflow` as its AI library allowing it to create an 8 layered CNN which trains and tests the dataset. The way it does this is surprisingly simple:

   Firstly, we should understand the structure of the MNIST dataset. It is an array of numbers ranging from 0-255 (0 being black and 255 being white) (as seen in the second cell). The first thing we do is divide the MNIST dataset by 255 which is what we call `normalizing` the data. This transforms all the data into a range of float numbers between 0-1 (e.x. 0.478). 

   Once the data is ready for training and testing, we start creating the actual CNN. Going line by line, we have 
    - 3 <b> Conv2D </b> layers : Convolutional layers simply use math and filters to make certain parts of an image stand out more than other parts.
        - (convolution is very cool, watch this video to learn more: https://youtu.be/KuXjwB4LzSA?si=Z3aS5IROneAmAO2U)

    - 2 <b> MaxPooling2D </b> layers : These layers cut down the size of an image allowing the NN to use less compute
    - 1 <b> Flatter </b> layer : This just turns the 2D vector into a 1D
    - 2 <b> Dense </b> layers : This compresses the output resulting in just the 10 numbers we need which are the probabilities for the image being each numebr from 0-9

    Next, we actually <b> compile </b> the model by training it on the dataset using multiple `Epochs`. (Epochs are the amount of runs the models goes through before completing its training). Once this is done, we get a final accuracy report of the model and we can see how accurate it is based on the `10,000` test images and `60,000` train images.

- <b> `Data Visualization` </b>: This part of the program uses `Matplotlib's PyPlot` to display our results in the form of a bar graph showing the models exact thought process. 

    The bar graph is created using the `plot_value_array()` function and the actual number is displayed using `plot_image()`. Cell 14 is a very easy way to see any of the model's guesses. Cell 15 displays 9 different guesses at once.

### Reflection
This project was a milestone for me as I stepped foot into the actual AI world for the first time. It gave me a very good understanding of how Tensorflow uses statistics and ALOT of math to create an AI that can guess what a number is ranging from 0-9. Fun fact: ChatGPT can't actually <I> think </I> of anything as it basically just guesses what it should say and goes with the best guess. Learn more here: https://youtu.be/-4Oso9-9KTQ?si=-jrjyqMdGsBYsg5N

It also gave me a very good understanding of data visualization and processing. The MNIST dataset has a total of `80,000` images which were not easy to handle as a first timer. Learning about `Tensors` and `CNNs` was not easy either but that's what life is all about. Take a challenge, then spend a month learning and mastering it. 

### Future Plans
I would love to learn SQL next and work on a password manager with python and SQL but I was having trouble finding a reasonable GUI so that's still up for debate. I also really want to create a CNN WITHOUT any form of AI libraries. Just using pure python, numpy, and hopes and dreams. There are many sources online to learn more about these so hopefully that won't be an issue. Lastly, I really want to make a portfolio website for myself. This would require me to advance my JavaScript skills and learn about network and how websites actually work which is a long task but I am hopeful that I will have most of these done within a month or two.

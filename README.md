# COMP5405 Project Manual
Designed by Hengzhi Chen, Xiaochen Tang, and Xinyao Tian

Written by Xinyao Tian

## Change Detection in Remote Sensing

### Project Overview
This project is a component of the entire COMP5405 course.

The purpose of this project is to develop and implement a method which could detecting changes between
two remote sensing images. By implementing GANs and entangled networks, we finally achieved a decent result
in the evaluation dataset.

### Dataset
The dataset we are using is called LEVIR-CD, 
which contains several 1024 times 1024 image pairs, 
and all the changes have been labeled by binary images. 
For the convenience of processing, 
we reduce the size of images 16 times lower, which is currently 256 times 256.

The dataset could be found through this link:
https://justchenhao.github.io/LEVIR/

### How to run our application?

#### Environment Setup

Following the steps below can guarantee the success of running our project: 

1. Firstly, please open the CiLD.ipynb in the CiLD/ folder

2. Then, find the "Runtime" item in the toolbar, and select "Change Runtime Type" in the pull-down menu to "GPU"

3. (Please mention that there's when mounting the project path to the Google Colab Environment, it's need to use your Authen Code)

4. After doing that, run each code block until the final one

#### Training the Change Detection Model

If you would like to run the whole stuffs of the training process, 
please run the bottom command.

```bash
!cd /content/drive/MyDrive/CiLD/ && python train.py

```

#### Get the detected result

You could follow the next steps to get a binary image of the detected changes of two images

1. Put the two images you want to detect changes 
into CiLD/data/test/A and CiLD/data/test/B separately. You should give them the a same name.

2. Run the crop_image.py through Google Colab to convert the images from 1024x1024 to 256x256

3. Change the command in the Notebook to the below one and run it:

```bash
!cd /content/drive/MyDrive/CiLD/ && python train.py

```

4. Go to CiLD/data/test/Evaluation to see the result. 
The name of the result should be same to the images you named.

#### Further Improvement

In the future we plan to design a GUI for our application to let the real users get better usage. 

### The End
That's the end of our Application Manual. 
We know that it's now very intuitive to show this application in a Notebook format,
But since we need to leverage GPU from Google Colab, we have to do this.

Hope you would like our Project, sincerely.














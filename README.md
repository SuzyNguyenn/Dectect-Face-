# Facial Detection
</p>

<p align="center">
  <h3 align="center">Team facial Detection</h3>
  <p align="center">
    The app can detect the face of members of my group
    <br />
    <a href="https://raw.githubusercontent.com/SuzyNguyenn/Dectect-Face-/main/main.py"><strong>The Streamlit app</strong></a>
    <br />
    <br />
    <a href="https://github.com/SuzyNguyenn/Dectect-Face-/blob/main/training%20mobilenet.ipynb">Jupyter Notebooks</a>
    ·
    <a href="https://github.com/CHP2108/Dectect-Face-/tree/main/Data">Dataset</a>
    ·
  </p>
</p>

<img src="https://raw.githubusercontent.com/SuzyNguyenn/Banknotes_VND/main/ezgif.com-gif-maker.gif">

<p align="center">Check out more demo below :)</p>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary><h2 style="display: inline-block">Table of Contents</h2></summary>
  <ol>
    <li><a href="#dataset">Dataset</a></li>
    <li><a href="#project-description">Project Description</a></li>
    <li><a href="#outline">Outline</a></li>
      <ul><li><a href="#i-Connect application to webcam">Connect your application to webcam</a></li></ul>
      <ul><li><a href="#ii-Detect face area with YOLO">Detect face area with YOLO</a></li></ul>
      <ul><li><a href="#iii-Detect face area with YOLO">Detect face area with YOLO</a></li></ul>
    <li><a href="#key-takeaways">Key TakeAways</a></li>
    <li><a href="#future-work">Future Work</a></li>
    <li><a href="#thank-you">Thank You</a></li>
  </ol>
</details>


## DATASET
The dataset used for Banknotes project originates half from [CoderSchools] and half from myself. This data contains >5000 pictures in diverse angles ranging from 1,000 VND to 500,000 VND

## PROJECT DESCRIPTION    
   - [Training Model.ipynb](https://github.com/SuzyNguyenn/Banknotes_VND/blob/main/Training.ipynb)
    
   - [app.py](https://github.com/SuzyNguyenn/Banknotes_VND/blob/main/streamlit_app.py): Streamlit web app

## OUTLINE
### Connect application to webcam
- **GOAL: Running *main.py* will open a window and display a real-time webcam.**

🥸 TIPS: I found it more stable to write the code in VSCode, save it. Then run the script in Terminal.

Follow the below tutorial to connect to the webcam. *main.py.*
<a href="https://colab.research.google.com/drive/13r-kErvZuHaLDEFalIHPVN4HcfJTcJt0"> main.py </a>

### Detect face area with YOLO

🗝  **GOAL: Draw a bounding box around faces captured by webcam.**

👀  **TIP:** It's recommended to do the next steps on the notebook *misc.ipynb* or a testing notebook on Google Colab with a sample image first. Then, migrate all the code to the main.py after you are done debugging. 

✅  **TASK:**

- To use the pre-trained YOLO model, we have to download the model and its weight [**HERE**](https://drive.google.com/drive/folders/1QO9ydq_cUHlfpKK78DSUymHii5aix2jf?usp=sharing).
- Create a folder name ***yolo*** in the working folder and move downloaded files into it.
- Create a folder name ***sample*** in the working folder and download some sample images for testing.
- We can load the YOLOv3 model by using the below code snippet. **OpenCV** has a module called ***dnn*** dedicated for the use of Deep Learning. See more at [Official documentation](https://docs.opencv.org/3.4/d6/d0f/group__dnn.html), [Tutorial](https://docs.opencv.org/master/d2/d58/tutorial_table_of_content_dnn.html), [Complete Guide](https://bleedai.com/deep-learning-with-opencv-dnn-module-a-comprehensive-guide/)
    
    This deep learning module provides users the use many pre-trained networks, including ones in Tensorflow, Caffe, and PyTorch. In this project, we will employ this module to **load and use the pre-trained YOLO model.**

✅  TASK: When using cv2.dnn, the network will be loaded and return as a net object (a specific object in OpenCV with a specific syntax library for modeling)

Unlike our familiar process, the **net** object only allow data to come in as a **blob.** To convert original images into blob, we use ***[cv2.blobFromImages](https://www.pyimagesearch.com/2017/11/06/deep-learning-opencvs-blobfromimage-works/)***. 

### Detect face area with YOLO
Now that your application is already able to detect faces. It's time to recognize whose the face is.
<a href="https://raw.githubusercontent.com/SuzyNguyenn/Dectect-Face-/main/streamlit_app.py"><strong>The Streamlit app</strong></a>

## KEY TAKEAWAYS
- The project tried both basic Machine Learning model KNN and Deep Learning model MobileNetV3. However ML model like KNN was not effective like Deep Learning model in recognizing face.


## FUTURE WORK
  - The dataset is not big so model tended to be overfit with the dataset
  - Add more feature to detect the person who not in the group


## THANK YOU

  Words cannot express my gratitude enough to the people who helped me make this project a success. This project was a part of **CoderSchool 2021 Machine Learning bootcamp** that I took part in and was presented at the weekly project
  
  The bootcamp that lasted 4 months was taught by the dedicated and amazing Instructors (anh Quân, anh Nhân, anh Chinh) and Teaching Assistants (Minh, Nathan, Ngọc) whom I greatly appreciate. It also introduced me to people who have been very supportive throughout the course and that are now my good friends.
  
  Thank you again to all of the wonderful people whom I met at CoderSchool. Wish you all Good luck!
  
 -----------------
 If you like my work, please give this repository a star so I can keep improving and work on more projects :)


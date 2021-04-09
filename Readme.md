Social Distancing - Drone  

The purpose is to inspect whether the people in a public place maintain social distancing or not. It also checks whether every individual is wearing face mask or not. If both are not done, the drone sends alarm signal to nearby police station and also give alarm to the public. In addition, it also carries masks and drop them to the needed people. Nearby, traffic police will also be identified and deliver water packet and mask to them if needed. The proposed system uses an automated drone which is used to perform the inspection process. First, the drone is being constructed by considering the parameters such as components selection, payload calculation and then assembling the drone components and connecting the drone with the mission planner software for calibrating the drone for its stability. The trained yolov3 algorithm with the custom dataset is being embedded in the drone camera. The drone camera runs the yolov3 algorithm and detects the social distance is maintained or not and whether the people in public is wearing masks or not. This process is carried out by the drone automatically. The proposed system delivers masks to people who are not wearing masks and tells importance of masks and social distancing. Thus, this proposed system would work in an efficient manner after the lockdown period ends and helps in easy social distance inspection in an automatic manner. The algorithm can be embedded in public cameras and then details can be fetched to the camera unit same as the drone unit which receives details from the drone location details and store it in database. Thus, the proposed system favours the society by saving time and helps in lowering the spread of corona virus.



ADVANTAGES OF THE PROPOSED SYSTEM:

1) Can be used by police,government in order to monitor people in public place.

2) Can also be used during night time, if replaced with high night resolution camera.

3) By fixing a box to the drone the masks can be stored and also can be picked by people if they don’t have one.

4) Used in post lockdown period or post pandemic period,during unlock 1.0 it can be used for inspection process.

5) Helps reduce the stress of police people who are involved in inspection process.

FUTURE ENHANCEMENT OF THE PROPOSED SYSTEM:

1) In addition to it, the model would be made to chase the people if they do not follow the rules even after the warning voice note from the drone.

2) The future scope in this proposed system is  to design an drone along with a small hollow box
and drone should be able to lift the box.

3) The payload of the drone is calcualted along with the box weight and then constructed
accordingly.

4) To design the drone with Artificial Intelligence in order to predict decisions by learning from
the environment.

5) To implement augumented reality technology to visually show the effect of not maintaining
social distance as well as not wearing masks.\

6)To use an more efficient algorithm for object detection such as tiny-yolo which has faster
computing rate.

7)To implement and give the project to government for the post pandemic period so that it would
benefit government as well as police people and the public people.

APPLICATIONS:

1) This project can be implemented during post lockdown period unlock 1.0 and can be used to
inspect social distance and masks.

2) The algorithm can be embedded within CCTV cameras and can able to detect social distance.

3) This system can be implemented in shopping malls, railway station, crowded places, public
places, marriage halls, etc.

4) It can be applied anywhere as it is deployed in the IBM cloud

5) Can be implemented in schools,theatres etc.

6)Can be used by government as well as police for the inspection of social distance.


WORKING OF PROJECT :

Collecting Images for project:
The project is related to social distancing and hence to make the algorithm recognise whether people maintain social distance or not as well as wear masks,the images are collected based on 

1) public people who maintain social distance
2) public people who does not maintain social distance
3) public people who wears masks
4) public people who does not wear masks
5) Combination of 1 and 3 
6) Combination of 2 and 4
7) Combination of 2 and 3
8) Combination of 1 and 4
9) Combination of 1,2,3 and 4.


Dataset Creation-Microsoft VOTT Labelling Tool:
The other way of creating the dataset for deep learning algorithm is to use an labelling tool to label the images manually. 

Step1: Download the Microsoft VOTT tool from the link.Download Vott tool link

Step2: Create a new project named Annotations, Create a two folders in local system in which one would act as source folder and other one as destination folder.

Step3: The source folder consists of the images dataset which are to be labelled and the destination folder will consist of the labelled images with annotations stored in .csv file.

Step4: Select Source connection as local file system,click create,give a name for the source and click save.Repeat the same procedure for destination connection.

Step5: Select the source name and destination name, add the classification tag names and save the project.

Step6: Change the export settings of the project.Change the export format from json to excel(.csv) format.Click save.

Step7: The page to label the images appears.A square is drawn on the object which is to be detected and tag name is added.

Step8: Once the labelling is completed,the project is exported into the destination folders as Anotations-export-csv file.

Step9: The folder consists of the labelled images with an csv file named Annotations.csv. The csv file consists of 4 coordinates values such as xmin,ymin,xlabel,ylabel.

Step10:The dataset is now ready for the yolo algorithm. 


The Microsoft Vott tool is downloaded from the github link vott download and is setup in the local file system.
https://github.com/microsoft/VoTT


Creating Custom Dataset:

The creation of custom dataset is done by using the second method which is labelling the images manually using Microsoft Visual Object Detection Tool (VOTT).

Step1: Download the social distancing images for the dataset form google images.Create a folder called Input Images and store the images in the folder.Create OutputFolder as destination folder.

Step2: Create new project called Annotations and give the source and destination folders,then give the tag name as mask,non-mask,social distance,no social distance and save the project.

Step3: Label the images based on the category and give the appropriate tag name for each image.

Step4: Before exporting,change the project setting as export file as .csv and then export the project.

Step5: The labelled images are stored inside a folder called Annotations-export folder with Annotations.csv file.

Step6: The custom dataset is ready for training the yolo algorithm.


Commands in Colab

Google colab has its own commands in order to execute the python code and various other algorithms.

Some of the commands are:

1) !git clone  "github link" - cloning github repository
2) !pip install "package-name"- installing python package
3) !rm -rf "folder name"- removing a folder
4) !wget "link"- getting the contents from provided link
5) !python "filename.py" - runs the python file
6) %cd - current working directory
7) %cd .. - changes one directory to other directory
8) from google.colab import drive - mounts notebook with google drive
    drive.mount('/content/drive')
     
These are some of the commands used in google colab.

https://www.marktechpost.com/2019/06/07/how-to-connect-google-colab-with-google-drive/

Setting up packages

The required python packages to be setup before training the deep learning algorithm are being installed in the notebook.

Before installing the packages,the notebook is created and then mount to the google drive.The Notebook settings is set to GPU and then saved.

Package Installation

The required python packages for this project is installed in the notebook after setting up the notebook settings.

The packages are 
setuptools>=41.0.0
pip>=19.0.0
absl-py==0.7.1
astor==0.8.0
attrs==19.1.0
backcall==0.1.0
bleach==3.1.4
certifi==2019.6.16
chardet==3.0.4
cycler==0.10.0
decorator==4.4.0
defusedxml==0.6.0
progressbar2==3.46.1
entrypoints==0.3
gast==0.2.2
google-pasta==0.1.7
grpcio==1.22.0
h5py==2.9.0
idna==2.8
ipykernel==5.1.1
ipython==7.6.1
ipython-genutils==0.2.0
ipywidgets==7.5.0
jedi==0.14.0
Jinja2==2.10.1
joblib==0.13.2
jsonschema==3.0.1
jupyter==1.0.0
jupyter-client==5.3.0
jupyter-console==6.0.0
jupyter-core==4.5.0
Keras==2.2.4
Keras-Applications==1.0.8
Keras-Preprocessing==1.1.0
kiwisolver==1.1.0
Markdown==3.1.1
MarkupSafe==1.1.1
matplotlib==3.0.3
mistune==0.8.4
mpmath==1.1.0
nbconvert==5.5.0
nbformat==4.4.0
notebook==5.7.8
numpy==1.16.4
opencv-python==4.1.0.25
pandas==0.24.2
pandocfilters==1.4.2
parso==0.5.0
pexpect==4.7.0
pickleshare==0.7.5
Pillow==6.2.1
prometheus-client==0.7.1
prompt-toolkit==2.0.9
protobuf==3.8.0
ptyprocess==0.6.0
Pygments==2.4.2
pyparsing==2.4.0
pyrsistent==0.15.3
python-dateutil==2.8.0
pytz==2019.1
PyYAML==5.1.1
pyzmq==18.0.2
qtconsole==4.5.1
requests==2.22.0
scikit-learn==0.21.2
scipy==1.3.0
Send2Trash==1.5.0
six==1.12.0
sklearn==0.0
sympy==1.4
tensorboard==1.15.0
tensorflow==1.15.2
tensorflow-estimator==1.15.0
termcolor==1.1.0
terminado==0.8.2
testpath==0.4.2
tornado==6.0.3
traitlets==4.3.2
urllib3==1.25.3
wcwidth==0.1.7
webencodings==0.5.1
Werkzeug==0.15.4
widgetsnbextension==3.5.0
wrapt==1.11.2
https://github.com/AntonMu/TrainYourOwnYOLO/blob/master/requirements.txt






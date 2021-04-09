C19 - SPECTOR

The purpose is to inspect whether the people in a public place maintain social distancing or not. It also checks whether every individual is wearing face mask or not. If both are not done, the drone sends alarm signal to nearby police station and also give alarm to the public. In addition, it also carries masks and drop them to the needed people. Nearby, traffic police will also be identified and deliver water packet and mask to them if needed. The proposed system uses an automated drone which is used to perform the inspection process. First, the drone is being constructed by considering the parameters such as components selection, payload calculation and then assembling the drone components and connecting the drone with the mission planner software for calibrating the drone for its stability. The trained yolov3 algorithm with the custom dataset is being embedded in the drone camera. The drone camera runs the yolov3 algorithm and detects the social distance is maintained or not and whether the people in public is wearing masks or not. This process is carried out by the drone automatically. The proposed system delivers masks to people who are not wearing masks and tells importance of masks and social distancing. Thus, this proposed system would work in an efficient manner after the lockdown period ends and helps in easy social distance inspection in an automatic manner. The algorithm can be embedded in public cameras and then details can be fetched to the camera unit same as the drone unit which receives details from the drone location details and store it in database. Thus, the proposed system favours the society by saving time and helps in lowering the spread of corona virus.


WORKING OF PROJECT :

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

Step10:The dataset is ready for training.


The Implementation of this particular inspection process has to 
be carried out hierarchically and legally

So, we use Pega Platform for building an application for this project 
This is the case life cycle of our application

It has 3 stages namely Schedule Inspection, Approve Inspection, Perform Inspection

Schedule Inspection will schedule the inspection, 
Schedule will be approved/rejected by the higher authority

If approved by the authority, the inspection process 
is carried out and all the details are stored in database

There are 3 people involved in this inspection process, 
They are Scheduler, Higher Authority, Inspector

Each role have their own login, 

so this is the application portal which we have designed for this project

First, the scheduler will login with his id & password and 
will be directed to scheduler portal

The scheduler can schedule the inspection by clicking the image

Here, the schedule details are collected such as type of drone,schedule time
schedule date, country,state , city details

Then the scheduler details are collected and after submitting,again the details
will be displayed for review purpose

After submitting, the case proceeds to approval stage
where higher authority will approve the schedule

Now im logging out and logging in as the higher authority

The authority enters login id and password 
and is directed to manager portal

They get an email approval where they review schedule details 
They can either approve/reject the schedule

If approved, the case is routed to inspector for inspection process
If rejected, the case resolves with reason for rejection and mail is sent 

Now im logging out and logging in as the inspector

The inspector enters login id and password 
and is directed to inspector portal

He picks the latest case id and by clicking the simulation link

It will be redirected to drone portal where they can perform
the inspection process

Once the inspection process is over, after submitting
the inspector has to enter inspection details

such as duration of flight, number of masks given , how many
times drone reached to person? , after entering these details

the details are reviewed by the inspector and then the case resolves
by sending the inspection details to authority by email

Now we login to authority portal for seeing reports
there are 3 reports Schedule report, Graphical representation'

of number of masks given per day, and the third report is 
inspection details report based on schedule date

Now ill show the datas stored while entering the respective details

In this inspection details are stored and then scheduler details
then schedule details are getting stored into the database 

Another casetype is used for maintenance of drones

The Scheduler will schedule maintenance by collecting technician details such as  technician name , email id, phone number will be collected.

Then drone details will be collected by entering drone's model number, drone's serial number,drones's name, drone's weight and 
particular date of maintenance will be recorded. The particular service can be selected for maintenance of drone

Then, this maintenance schedule will be directed to higher authority who can either approbve/reject the schedule.

The Authority logs in to his portal and he views maintenance schedule, So they either approve/reject the schedule, 
if they reject the schedule an rejection mail will be sent to scheduler.

If approved, then the case proceeds to perform maintenance stage







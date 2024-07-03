2024-07-03 16:52

Status: 

Tags: 

# Soccer Analyst

**Definition:** This is a [[Personal Projects]] which I am working on during this summer. This aims to be a project which implements machine learning and the specific field of machine learning is [[Computer Vision]].

### Goal of the Project
- I aim to put this on my resume and land a [[Software Engineer]] role
- Learn more about [[Computer Vision]] and how to do [[Machine Learning]] in general 
- Create something which people can use to analyze their soccer games
### Steps to Implement 
This is the general plan I have for what I want the model to do and how I would make the model 
- Create a machine learning model using computer vision
	- The model will be able to analyze player movements and the ball 
	- Use that data to calculate things like passes and export that data into a spreadsheet
	- This data would then be able to be used to create things like pass maps, movement maps and other advanced metrics

To create the model I need to prepare the data for training 
- First I need to gather all the videos I need 
- Take individual frames and draw bounding boxes on them, highlighting each player, the ball and the referee
- Assign a numeric value to each bounding box of the xy attributes

Now I can send this data for training and to train the model I need to split my data into 2 groups, training and testing 


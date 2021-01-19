# Traffic Flow Prediction
My ideal goal is to build a service which asks the user to select two points as source and destination on the map and my
service can inform the user how long it takes him to travel from source to destination. This job has so many subtasks 
but the hardest and most important one is traffic flow prediction.

# This Is Done Before!!!
Yes, there are apps like google map and more that do the same thing, but after talking to Sina Bakhtiary (routing tech 
specialist at snapp) I was assured that it's still one the most valuable jobs to do and can run a business. 

# How Is The Job Done At The Moment?
This will take a long time to explain it with details but this is the idea, there are two subsections , first, so many 
people have the app on their cellphones and with the access to their GPSs the traffic flow in a certain street can be 
estimated periodically, as you can guess this will turn into a time series problem. Second, by remembering the traffic 
flow at the same street at the same day and time in previous weeks the app has a historical model that can be used.

# What is the improvement?
My approach is completely different, I'm going to use deep learning to forecast the traffic. In my opinion the best model
is hybrid of smaller ones, some models work better for short-term travels like 15 minutes, and some do better for 
long-term travels like 60 minutes.

# Prerequisites

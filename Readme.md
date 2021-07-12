# Traffic Prediction
This project contains my studies and codes for my B.S proposal at Amirkabir University of tech<br/>
I have a more detailed explanation about what I did in my proposal which you can take a look at in the assets 
of this repo. However, I'm going to write a summary about it in here too.

## What is the idea to predict the traffic?
We are going to use both **temporal** and **spatial** data in order to predict the traffic in some specific places, so we
have simply two kinds of data, first, we are looking at the problem as a graph which we like to estimate the speed of 
traffic in its nodes so obviously we need a file which contains the weight matrix of the graph, in this project we simply
think the closer the nodes are to each other the larger the weight between those nodes are (which is not always the case)
and then we need a dataset which tell us about the traffic speed in the nodes of this graph over time (we have a time 
interval like 5 minutes and measure the traffic each 5 minutes and add it as a record to the dataset). To find out 
how the traffic changes over time we use 2D Convolution on time axis and to find out how the traffic at one node can
affect others we apply convolution directly on the graph.(This calculation has the complexity O(n^2), and we use **chebyshev 
polynomials** estimation to reduce the order of complexity)

## What was my dataset?
You can access the dataset in this repo. I used this site to get data [http://pems.dot.ca.gov/?dnode=Clearinghouse.How]() 
Type: Station 5-minute;<br/>
District: 7;<br/>
Time Period: Weekdays of May and June of 2012.<br/>

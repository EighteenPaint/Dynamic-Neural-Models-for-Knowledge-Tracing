# Dynamic-Neural-Models-for-Knowledge-Tracing
Student Performance Prediction Using Dynamic Neural Models


We  address  the  problem  of  predicting  the  correctness  of the student’s response on the next exam question based on their  previous  interactions  in  the  course  of  their  learning and evaluation process.  We model the student performance as a dynamic problem and compare the two major classes of dynamic neural architectures for its solution, namely the finite-memory  Time  Delay  Neural  Networks  (TDNN)  and the potentially infinite-memory Recurrent Neural Networks(RNN). Since the next response is a function of the knowledge state of the student and this, in turn, is a function of their previous responses and the skills associated with th eprevious questions, we propose a two-part network architecture.  The first part employs a dynamic neural network (either TDNN or RNN) to trace the student knowledge state.The second part applies on top of the dynamic part and it is  a  multi-layer  feed-forward  network  which  completes  the classification task of predicting the student response based on our estimate of the student knowledge state.

We tested our models on five open-access datasets.
The Dataset folder contains all the necessary files. For each dataset, there are five train-validation sets for the cross-validation experiments,  a train-test set for the evaluation of the results, a file with skill names and pre-trained embeddings files that represent the skill names with Word2Vec ( vectors of 100dim  and 300dim) and FastText (vectors of 300dim) methods. 

The data is in the following format:
24

8,5,5,5,10,5,12,35,12,13,41,12,13,41,12,13,41,12,35,9,5,8,9,8

0,0,1,0,0,0,0,0,0,0,0,1,1,1,1,1,1,1,1,1,0,1,0,0


The first line shows the number of student interactions.
The 2nd line contains the skill IDs to which the student answers.
The 3rd line contains the student's answers, 1 for the correct answer or 0 for the wrong answer.

A detailed description of our models is given in the article submitted and accepted at the 
EDM 2021: the 14th International Conference on Educational Data Mining 
Paris, France, June 29—July 2, 2021 
"Student Performance Prediction Using Dynamic Neural Models"
Marina Delianidi, Konstantinos Diamantaras, George Chrysogonidis and Vasileios Nikiforidis

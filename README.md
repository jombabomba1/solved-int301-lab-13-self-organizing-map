Download Link: https://assignmentchef.com/product/solved-int301-lab-13-self-organizing-map
<br>
<span class="kksr-muted">Rate this product</span>




Clustering Problem using a Self-Organizing Map (demo.m)

close all, clear all, clc, format compactload simplecluster_dataset;% a 2×1000 matrix of 1000 two-element vectors. x = simpleclusterInputs;% plot clustersfigure, plot(x(1,:),x(2,:),’g.’);hold ongrid on

% Create a Self-Organizing Map dim1 = 10;dim2 = 10;net = selforgmap([dim1 dim2]); % Train the Network

[net,tr] = train(net,x);

% View the Network view(net)% Plotsfigure, plotsomtop(net) figure, plotsomnc(net) figure, plotsomnd(net) figure, plotsomplanes(net) figure, plotsomhits(net,x) figure, plotsompos(net,x)

Exercise:

1. Define 4 clusters of input data with the following piece of code, and plot input data using your own codes;

% number of samples of each cluster K = 200;% offset of classesq = 1.1;

% define 4 clusters of input dataP = [rand(1,K)-q rand(1,K)+q rand(1,K)+q rand(1,K)-q; rand(1,K)+q rand(1,K)+q rand(1,K)-q rand(1,K)-q];

%% Your own codes

2. Create and train 2D-SOM with the following parameters using your own codes, and plot the 2D-SOM results with the following functions (you can also change the parameters accordingly).

% SOM parameters dimensions = [10 10];

%% Your own codes

% plot input data and SOM weight positions figure, plotsompos(net, P); grid on% plot SOM neighbor distancesfigure, plotsomnd(net)
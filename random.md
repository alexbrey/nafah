# Evaluating Network Metrics using Random Networks

What you'll need
-Cytoscape
-

## Metrics in isolation
Evaluating metrics in isolation is hard. Let's say the highest eigenvector centrality for a node in our network is .5139. On its own, this number doesn't tell us much. As we saw in the exercises last week, we can start to make sense of this number when we compare it to the metrics of other nodes in our network. If most nodes have an eigenvector centrality of .000034, then by comparison we see that our node of interest is highly central. While we can compare this number to centrality metrics of other nodes in our network, we might also want to know whether this is higher or lower than we find in other networks. 

So how can determine if node's metric is high or low? The first solution that might come to mind is to directly compare this value with node metrics from other networks that we've analyzed. This is easy to do, but it's a bit like comparing apples to oranges. Those networks represent different types of interactions, and they may have many more or fewer nodes, or very different structures. As a consequence, direct comparisons of both node-level and network-level metrics are basically meaningless. What we need is a solution that lets us compare apples to apples.

## Apples to Apples
To produce a meaningful comparison, we need a network that has the same number of nodes and edges as our network. It should also have a structure similar to our network. In our observed network, these properties emerge from a specific set of socio-economic forces. An economy can only support so many master painters and painting students, and a master painter can only teach so many students. Some teachers will be especially popular and teach as many students as they can, while others will only teach a few. 

Data preprocessing:
Watch out! Although CSV parsers aren't supposed to look inside of quoted strings, Cytoscape doesn't always handle enquoted commas very well. Either remove commas in your node identifiers using replace all, or convert your file to a tab-separated values (.tsv) document.

## Step 1: Import your network into cytoscape
Upon opening, Cytoscape will prompt you to start a new session.

Click "From Network File," navigate to your network data in the filebrowser, then click "Open".
Make sure that Cytoscape accurately identifies the source, target, and type columns. At this point, you can double-check that it recognizes the correct delimiter by click on "Advanced Options..." and noting whether the selection box for comma or tab is checked. Change it if necessary, and click "OK" to close the advanced options menu. Then click "OK" in the "Import Network From Table" menu to finish the import.

## Step 2: Calculuate network metrics for the observed network
We'll use a Cytoscape App called CentiScaPe to calculate a bunch of node-level and network-level metrics about this network all at once. If you haven't already installed CentiScaPe, you can install it by clicking "Apps" in the main Cytoscape application menu, and select "App Manager". In the App Manager window search bar, type "Centiscape", select the Centiscape app, and click "Install".

Once you have CentiScaPe installed, click on "Apps" again and then select "CentiScaPe". CentiScaPe will open a new tab on the Control Menu with settings and options for calculating different metrics. Under "Implemented Centralities", click "Select All" 

## Step 3: Create a Random Network Using NetworkRandomizer

## Step 4: Calculate network metrics for random network

## Step 5: Compare the metrics from your real and random network

## Step 6: Interpret your comparison

# Naive Speech Imitator

## What it does - Overview

This program imports a list of texts from a person and generate a new sentence by imitating the style of the imported sample text. 

## How the algorithm works

This algorithm first imports a series of texts from an external file. It then model the data and uses the network propagation model to generate the imitated text. 


## A little more detail on the algorithm: 

The imported file is suppose to contain a list of texts from the individual that you want the algorithm to imitate. 

### The Network
Each unique word in the imported file is a node. An edge is created between two nodes if two words occur next to each other in the same sentence. 
The occurance of such adjacency would be used to weight the edge. 

### The Start Word List
The algorithm maintains a dictionary that will be used to pick the starting word of the imitated sentence. Each word has a weight proportionary

### The Network Propagation Model
The model first pick a start word from the start word list, then it propogates from the node with that start word to other nodes based on all adjacent weighted edges. The propagation ends once it reaches a node with ".", "!", or "?". 

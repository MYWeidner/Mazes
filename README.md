# Mazes
Using opencv and Dijkstra's algorithm

#### Solving Image Maze - Algorithms course assignment

Given a maze as an image with a start and end point, I wrote code to solve the maze.

An image is a 2D matrix of pixels of a particular size that depends on its resolution. Each pixel has a color which is given by its Red, Green and Blue (RGB) values.

An image is viewed as a graph where each pixel of the image is a vertex and edges connect a pixel to its neighbor. The weight of an edge should be very small if the pixel colors are similar (i.e, the differences between r, g and b values are close to zero) and correspondingly large as the pixel colors diverge.

Next, given a source pixel and destination pixel, I found the shortest weight path from source to destination using Dijkstra's algorithm.

I modified Dijkstra's algorithm in two ways:

* It can exit as soon as the destination is reached.
* A 1000 x 1000 pixel image gives rise to a graph with a million vertices. Storing such a graph as an adjacency list is going to be very memory intensive. Instead, my goal was to generate the vertices and edges on-the-fly.

I used opencv library, a popular computer vision library to load, and manipulate images of mazes.

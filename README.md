###  Parallel and Concurrent Programming Course
#### 3rd Assignment


Floyd-Warshall algorithm
The Floyd–Warshall algorithm is an algorithm for finding all shortest paths in a positively weighted graph. While Dijkstra or A* compute the path between two nodes, or in some extensions between one node and all other nodes, the Floyd-Warshall computes all possible shortest paths at once.

The algorithm receives as input a distance matrix M where M[i,j] represents the distance between nodes i and j.

The algorithm can be written in Python as:

for k in range(0, N):
  for i in range(0, N):
    for j in range(0, N):
      M[i][j] = min(M[i][j], M[i][k] + M[k][j])

The Task
Write a sequential CPU and a parallel GPU version. You can use any language as long as it will execute the algorithm on the GPU.

You should submit a zip file with your code and a PDF or txt report.

The report is as important as the working code — This is a Masters-level course after all! — and will be evaluated as such. Your report should include the following:

A description of the necessary modifications for GPU-execution
The rationale of the choice of parameters for GPU-execution (blocks, threads) and memory usage or transfers.
An explanation of whether your program suffer from thread divergence or not.

Grade: 12,5/20
[N-puzzle](https://en.wikipedia.org/wiki/15_puzzle) problem is one of the well-known classical problems in artificial intelligence for modelling algorithm using heuristic.  
  
Problem description is as follows :  
* Given a k x k grid with k<sup>2</sup>-1 (=n) blocks each labeled with 1 through n and a blank one.  
Our goal is to rearrange the blocks so that they are in order, using fewest number of moves possible.  
A move can be either a horizontal or vertical sliding of block. 
    
This C++ implementation uses A* search to solve this problem using heuristic. The success of this approach largely depends on the choice of heuristic.  
  
  
Here three heuristics have been considered.  
    
* **Hamming Distance** : The number of blocks in the wrong position (excluding the blank)
  
* **Manhattan distance**: The sum of the Manhattan distances (sum of the vertical and
horizontal distance) from the blocks to their goal positions.  
  
* **Linear Conflict**: Two tiles t<sub>j</sub> and t<sub>k</sub> are in a linear conflict if t<sub>j</sub> and t<sub>k</sub> are the same line, the
goal positions of t<sub>j</sub> and t<sub>k</sub> are both in that line,t<sub>j</sub> is to the right of t<sub>k</sub> , and goal position of t<sub>j</sub>
is to the left of the goal position of t<sub>k</sub> . Here line indicated both rows and columns. The
linear conflict heuristic is calculated as Manhattan distance + 2*(Linear conflicts).
  
**Hamming distance heuristic may require a lot of memory even over 5GB for solutions having significant number of steps. Better not to run hamming distance heuristic for 4x4 or larger boards.  
You can change this in "main.cpp".**
  
  
Procedure to run this Implementation:  
  
**Step 1**:  
  
    Input format:(in "in.txt")  
    
    Line 1 : n  
    Next put initial k X k board configuration with numbers from 1 to n and a single 0 that denotes blank
  
>An input:  
>> 3  
>> 1 5 0  
>> 7 6 4  
>> 2 3 8  
    

**Step 2**:  
  
    Compile "main.cpp" and then run the executable    
    or  
    You can open the whole folder as a CLion Project.  
  
**Step 3**:  
  
    You will find the output in "out.txt".  
  
  
Some sample inputs have been provided in "in.txt"  
  
**This implementation requires minimum C++11**
  
    
    
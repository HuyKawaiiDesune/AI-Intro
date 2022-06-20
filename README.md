AI plays snake.

How to run ?

   Install Python3.
   
   Install these modules:
   
      pip install pygame
      pip install matplotlib
      
   Run play.py file.

Files/Directories

   setting.py: contains game settings and global variables
   
   snake.py: contains Snake and Square classes
   
   play.py: contain code for running the project

How the AI works?
1. The snake use a searching algorithm to find a path from its head to the food (from now referred as path 1). Move to step 4 if path 1 is not available.
2. Create a virtual snake identical to the original snake and let it follow path 1. Then, check if there a path is available from the virtual snake's head to its tail (from now refereed as path 2). If path 2 not available go to step 4.
3. If both path 1 and 2 are available, let the snake follow path 1
4. If path 1 or path 2 is not available, let the snake follow its tail.

note: all these steps are repeated for each move of the snake

addendum: in play.py there are 3 line of code, by default only the first one is used, it runs the game normally (you can left click to change searching algorithm), you can comment the first line and run any other line you want, the second line runs the game without UI interface to get results faster, the third evaluates n number of runs with a parameter to defide algorithm use (0 for BFS, 1 for DFS, 2 for A*) the number of runs n can be changed in getdata.py 

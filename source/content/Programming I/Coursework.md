|   |   |
|---|---|
|**Issue Date**|**23rd October 2025**|
|**Last Release Date**|**23rd October 2025**|
|**Submission Deadline**|**16:00, 12th December 2025**|

[Coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") is the continuously assessed part of the examination and is a required part of the degree assessment. Assessed work must be submitted as specified below. You are reminded to read all of the following instructions carefully.

Please note: Any alterations to the [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") will be posted to the [Coursework section on Moodle](https://moodle.ecs.soton.ac.uk/course/view.php?id=479#section-7). If issues are found with the specification it will be revised if necessary. The [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") specification will contain the change log. If questions arise as to how certain aspects might be implemented then suggestions of approaches may be made but these will be suggestions only and not defined parts of the specification.

Late submissions will be penalised at **10% per day**. No work can be accepted after feedback has been given. You should expect to spend up to 25 hours on this [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework"). **This [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") is to be completed individually**. Please note the University regulations regarding [academic responsibility and conduct](https://www.southampton.ac.uk/quality/assessment/academic_integrity.page).

### Release Notes

|   |   |   |
|---|---|---|
|**Date**|**Version**|**Description**|
|23/10/2025|1.0|Initial version|
|27/10/2025|1.1|Added "B" movement|
|17/10/2025|1.2|- **Part 4**: Clarify that all the code developed **in this part** will be in `maze_runner.py`. Emphasise that "You must ONLY use the the `runner.explore()` function to gain information about the maze."<br>- **Part 5**: Fixed a typo in `if __name__ == "__main__":`|
|4/12/2025|1.3|- Added clarification to **Part 4** regarding starting orientation|
|7/12/2025|1.4|- Added clarification on the output of the `explore()` function|
|9/12/2025|1.5|- Fix typos in **Part 2** and **Part 3**<br>- Clarification to implement the left-hug algorithm|

### [Coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") Aims

This [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") allows you to demonstrate that you:

- understand how to construct simple modules and implement methods,
- are able to take simple pseudo-code descriptions and construct working Python code from them,
- can write a working program to perform a complex task,
- have an understanding of procedure programming,
- can correctly use exceptions and I/O,
- can write code that is understandable and confirms good coding practice.

### Contacts

General programming queries should be made to your demonstrator in the timetabled [labs](https://moodle.ecs.soton.ac.uk/course/section.php?id=5775 "Labs") or (better) to the dedicated Discord channel. Queries about the [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") specification should be made to the same Discord channel. Any issues that may affect your ability to complete the [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") should be made known to [Heather Packer](mailto:hsp2m10@soton.ac.uk), ideally before the submission deadline.

### Specification

This [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") aims to construct a virtual representation of a maze-solving game. This game will consist of several entities, e.g., the maze, and the runner. Based on this concept of a maze runner, we will create a simple simulation called "ECS Maze Runner”.

You are not required to have any knowledge of maze solving or experience in similar games to complete this [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework").

The  ECS Maze Runner may bear some similarities to a real maze but is very simplified and in some cases likely to be quite different to how a real maze might work. Your task is to implement the specification as written.

In some cases, specific names are defined or specific properties are given for modules. This is mainly to ensure that we can easily read your code, and find the parts that are most relevant to the marking scheme. You will not gain marks for deviating from the specification in order to increase the realism of the simulation. In fact, it may cost you marks and make it harder to assess what you have written. In some cases, we wish to know that you can use specific Python constructs, so if it specifies a `dict` data structure then we want to see you use a `dict` data structure. There might be other ways of implementing the same feature but we are trying to assess your ability to use specific constructs. Where the specification is less explicit in the way something is implemented (for example, by omitting what data types to use) you are free to make your own choices but will be assessed on how sensible those choices are. Comments in your code should explain the choices you have made.

### How the ECS Maze Runner Works

For this [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework"), you are expected to follow the specification as set out below. This may not correspond exactly to a maze and the runner in reality but we have chosen particular aspects for you to model that help you to demonstrate your Python programming skill.

There are several entities relevant to model a maze runner. For our purposes, these include:

- **Maze** --- The maze with walls to restrict the runner's movement within the maze  
- **Runner** --- The runner explores the maze to gather the information in order to find a path from a starting position to a target position.

The main purpose of the ECS Maze Runner is to have the runner explore the maze to get from a starting position to a predefined target position. Once the runner gathers sufficient information, they can make a decision to stop and compute the best path to reach the target position from the initial starting point.

The next sections will take you through the construction of the various entities. You are requested to follow this sequence of development as it will allow you to slowly add more functionality and complexity to your system. The [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") has the basic parts (Parts 1 to 6) and an extension part. For the basic parts, you can assume that the mazes are basic and connected (and can be solved using the left-hug algorithm). For the extension part, the mazes will require advanced algorithms to solve.

### Part 1 - Modelling the Runners

_"The number one Runner rule: 'Never. Stop. Running'”_  
_― James Dashner, The Maze Runner_

![The runners](https://moodle.ecs.soton.ac.uk/pluginfile.php/47415/mod_page/content/73/1da94f37-6a6c-48fc-a303-d1149fc7bfe1.png)

_(Source of runners figure: easy-peasy.ai)_

We start by modelling the runners moving in a grid. The grid will have (x, y) coordinates, where the x-axis indicates the horizontal position and the y-axis indicates the vertical position. The figure below illustrates this coordinate system. In the example, the runner is at position (5, 2). The directions of movement are `N`, `E`, `W`, `S` (stands for North, East, West, and South, respectively). The runner can only turn (either left or right) and move forward in this grid system.

![](https://moodle.ecs.soton.ac.uk/pluginfile.php/47415/mod_page/content/73/coordinate%20%281%29.png)

#### Your Tasks

Please follow the steps below to model the runners in the system.

- Create file `runner.py`.
- For each runner, you need to have the information about their position (i.e., the (x, y)-coordinate), and their orientation (i.e., which direction they are facing). Think about the appropriate data type that you are going to represent the runner and implement the following functions.
    - `create_runner(x: int, y: int, orientation: str)` -- _creates a runner corresponding to the input parameters_. The types for the arguments are given as type hints. You should set the default values for the parameters such that the runner will start from the `(0, 0)` coordinate and face North by default. You do not need to check the validity of the input for now. In particular, you can assume that the `orientation` is one of the 4 given directions, i.e., `"N"`, `"E"`, `"W"`, `"S"`.
    - `get_x(runner)` -- _returns the x-coordinate for the input runner_. Here the input runner is the same type you use for the output of the `create_runner()` function.
    - `get_y(runner)` -- _returns the y-coordinate for the input runner_. Here the input runner is the same type you use for the output of the `create_runner()` function.
    - `get_orientation(runner)` -- returns the orientation for the input runner. Here the input runner is the same type you use for the output of the `create_runner()` function.
    - `turn(runner, direction: str)` -- turn the runner to either `"Left"` or `"Right"`, the function _will return the runner after the turn_. The runner's position should not change, but the runner's orientation will change according to the direction of the turn. For example, if the `runner` is currently facing north (`"N"`), `turn(runner, "Left")` must return a runner at the same position and facing west (`"W"`).
    - `forward(runner)` - move the runner forward 1 cell, _the function will return the runner after the move_. The runner's orientation will be the same, but the position will change according to the runner's orientation. For example, if the runner (at position `(5, 2)`) in the figure above is facing "N" and moving forward, they will be in position `(5, 3)`.

**_You can have any additional variables, functions, and modules for your implementation you wish._**

**BY THIS STAGE** you should have a module named `runner.py` containing the above functions. You can create some validate your implementation by creating a runner, calling the movement functions (i.e., `turn(runner)` and `forward(runner)`) and checking their position and orientation (with `get_x(runner)`, `get_y(runner)`, and `get_orientation(runner)`).

We provide a test harness for this part. Information about how to download and use the test harness is at [comp1312/2526-Coursework-Tests](https://git.soton.ac.uk/comp1312/2526-Coursework-Tests). **You are expected to extend this to build your own test suits.**

### Part 2 - Modelling the Maze

_"‘Out there’s the Maze,’ Newt whispered, eyes wide as if in a trance.   
‘Everything we do—our whole life, Greenie—revolves around the Maze. ...'__”_  
_― James Dashner, The Maze Runner_

![](https://moodle.ecs.soton.ac.uk/pluginfile.php/47415/mod_page/content/73/maze.jpg)In this part, we will look at how to model the maze. The maze has dimensions represented by its width and height. The maze is enclosed by the _external_ (surrounding) walls and contains _internal_ walls lined up _horizontally_ or _vertically_. The following figure indicates how the external walls and some internal walls for an 11-(width)-by-5-(height) maze. 

![](https://moodle.ecs.soton.ac.uk/pluginfile.php/47415/mod_page/content/73/walls.png)

We will use the following colour convention for illustrating the wall: the external walls are blue, the internal horizontal walls are red, and the internal vertical walls are green. Notice for an m-(width)-by-n-(height) maze, there are (m-1) vertical walls and (n-1) horizontal walls.

To specify the wall, we use the following convention.

- A horizontal wall is specified by an x-coordinate and a horizontal line number ("hline" in the figure). For example, the red horizontal wall in the figure is specified by the x-coordinate of 5 and the horizontal line number of 2.
- Similarly, a vertical wall is specified by a y-coordinate and a vertical line number ("vline" in the figure). For example, the green vertical wall in the figure is specified by the y-coordinate of 2 and the vertical line number of 4.

#### Your tasks

Please complete the following tasks for this part.

- Create a module called `maze.py`. All your code will be in this module.
- Implement the function called `create_maze`. The function has two parameters representing the width and the height of the maze, both parameters have a default value of `5`. The function returns the newly created maze, with the external walls but no internal walls. You will need to think about the data structure representing the maze, including its dimensions and the walls.
- Implement the function called `add_horizontal_wall(maze, x_coordinate, horizontal_line)`, where "`maze`" represents the maze where the horizontal wall is added. The position of the wall is specified by the parameters "`x_coordinate`" and "`horizontal_line`", as explained above. The function returns the maze with the added wall at the specified position.
- Implement the function called `add_vertical_wall(maze, y_coordinate, vertical_line)`, where "`maze`" represents the maze where the horizontal wall is added. The position of the wall is specified by the parameters "`y_coordinate`" and "`vertical_line`", as explained above. The function returns the maze with the added wall at the specified position.
- Implement the function called `get_dimensions(maze) -> Tuple[int, int]` to return the dimensions of the maze, in the form of a tuple (width, height).
- Implement the function called `get_walls(maze, x_coordinate: int, y_coordinate: int) -> Tuple[bool, bool, bool, bool]` to return the information about the walls at a particular (x, y)-coordinate of the maze. The output tuple represents whether or not there is a wall in the directions of North, East, South, and West. For example, consider the maze in the above figure, we will have:

`get_walls(maze, 4, 2) = (False, False, False, True)`  
`get_walls(maze, 5, 2) = (False, False, True, False)`

- You will not need to handle any input errors at this point.

**_You can have any additional variables, functions, and modules for your implementation you wish._**

**BY THIS STAGE** you should have a new module named `maze.py` containing the above functions. You can create some validate your implementation by creating a maze, calling the set walls functions (i.e., `add_horizontal_wall()` and `add_vertical_wall()`) and checking the maze (with `get_dimensions()` and `get_walls()`). Use the figure above of the maze as the starting point for your testing. You might find that you will need to use a debugger to debug your program at this point.

We provide a test harness for this part. Information about how to download and use the test harness is at [comp1312/2526-Coursework-Tests](https://git.soton.ac.uk/comp1312/2526-Coursework-Tests). **You are expected to extend this to build your own test suits.**

### Part 3 - The Age of Exploration

_"'Every lovin’ second of every lovin’ day we spend in honor of the Maze, tryin’_   
_to solve somethin’ that’s not shown us it has a bloody solution, ya know? ...’”_  
_― James Dashner, The Maze Runner_

![The maze runner](https://moodle.ecs.soton.ac.uk/pluginfile.php/47415/mod_page/content/73/maze_runner.png)

In this part, we will model how the runner explores the maze. You will implement some helper functions to model how the runner gets information about the maze, moves safely within the maze, and finally explores the maze to get to the target location. We will use the following figure to illustrate the movement of the runner within the maze. In the figure, the runner is currently facing East and will move to the left (i.e., turn left and go straight North) as indicated by the purple arrow.

![](https://moodle.ecs.soton.ac.uk/pluginfile.php/47415/mod_page/content/73/runner_move.png)

#### Your Tasks

Please follow the instructions below to extend `runner.py`. 

- Implement the `sense_walls(runner, maze) -> Tuple[bool, bool, bool]` function for the runner to sense the information at the current position about the maze. The function returns a tuple of three Booleans, about whether or not there is a wall on the Left, the Front, and the Right of the runner. For example, consider the `runner` and the `maze` as in the figure above. As the runner is facing East, we have

`sense_walls(runner, maze) = (False, False, True)`

- Implement the `go_straight(runner, maze)` function for the runner to go forward to the new position, but also raise a "`ValueError`" if there is a wall in front of the runner. The function will return the updated runner after the move.
- Implement the `move(runner, maze)` function for the runner to move to a neighbouring position (only move 1 cell on the grid). Essentially, this function is the "brain" of the runner to decide which direction to move. There are different algorithms for solving mazes (see the video below).  
    
    ![](https://img.youtube.com/vi/ZMQbHMgK2rw/maxresdefault.jpg)
    
    Play Video
    
      
    However, basic mazes (where the target is along the external walls and the internal walls are connected to external walls) can be solved by a simple "left-hug" algorithm. The runner prioritises the directions to move according to the following order: go left, go straight, go right, go back. For example, the runner will go to the left if no walls prevent them. Similarly, the runner will go to the right if no walls are present on the right and some walls prevent them from going to the left and going straight. The function returns a tuple of two elements as follows.
    - The first element represents the updated runner.
    - The second element represents the sequence of actions that the runner took to get to their new position. We will use a letter for each action: "`L`" for turning left, "`F`" for going forward, and "`R`" for turning right. For example, to move to the left, the runner must turn left and then go forward. In this case, the sequence of actions is encoded as "`LF`". When you hit a deadend, use "B" to turnaround and go to back, instead of "LLF" or "RRF".

See the test harness for examples of how to test the `move` function.

- Implement the `explore(runner, maze, goal : Optional[Tuple[int, int]]) -> List[Tuple[int, int, str]]` function to allow the input runner to explore the input maze to reach the target position indicates by the input `goal`. If the input `goal` is `None`, the target position is the top-right corner of the input `maze`. Otherwise, the target get position is represented by a tuple indicating the x-coordinate and y-coordinate of the target. The output of this function is a list of tuples where each tuple consists of the x and y position of the runner and the sequence of actions (see the explanation above for "`move(runner, maze)`"). The x and y position is taken **before** the actions. The list of movements will get the runner from its initial position to the target position. The first entry in the list will be the starting coordinates with the first move to make. The final entry in the list will be the coordinates of the position **adjacent** to the goal position and the move to make to get to the goal. The final entry in the list is **not** the goal position.

**_You can have any additional variables, functions, and modules for your implementation you wish._**

**BY THIS STAGE** you should have extended `runner.py` containing the above functions. _Congratulations, you achieved a major milestone in solving the maze_. You can create some scenarios to validate your implementation by creating a maze, calling the set walls functions (i.e., `add_horizontal_wall()` and `add_vertical_wall()`), create some runners and check the functionality of  `sense_walls(),` `go_straight(),` `move()`, and `explore()`). You might find it useful to use the render utility function that we have provided in the test harness to print the maze and the runners to the screen. For example, you can use `print(render(maze, runner))` which will show the following corresponding to the figure above.

```

```
#######################
#.....................#
#.#.#.#.#.#.#.#.#.#.#.#
#.....................#
#.#.#.#.#.#.#.#.#.#.#.#
#.......#..>..........#
#.#.#.#.#.###.#.#.#.#.#
#.....................#
#.#.#.#.#.#.#.#.#.#.#.#
#.....................#
#######################

Here the walls are represented by `"#`", the path is represented by "`.`". (This will also be the format for the input file in Part 5). The runner is represented by either "`^`", "`>`", "`v`", or "`<`" depending on their facing direction.

We provide a test harness for this part as well as the render utility. Information about how to download and use the test harness is at [comp1312/2526-Coursework-Tests](https://git.soton.ac.uk/comp1312/2526-Coursework-Tests). **You are expected to extend this to build your own test suits.**

**Note: You must implement the left-hug algorithm for this part. You can explore other maze-solving algorithms in the extension task for this [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework").**

### Part 4. The Age of Discovery

_“'Bread crumbs,' Minho replied. 'I'm Hansel, you're Gretel.'"  
__― James Dashner, The Maze Runner_

In this part, we will implement how the runner discovers the shortest path according to the information they have gathered from exploration.

#### Your Tasks

Please complete the following tasks for this part.

- Create a module called `maze_runner.py`. All your code _developed in this part_ will be in this module.
- Implement the `shortest_path(maze, starting: Optional[Tuple[int, int]], goal: Optional[Tuple[int, int]]) -> List[Tuple[int, int, str]]` function to find the shortest path from the `starting`position to the `goal` position of the input `maze`. By default, the `starting` and `goal` positions are `None`. In the case when the input `starting` is `None`, the starting position will be the bottom left of the maze, i.e., `(0, 0)`. **Always set the initial orientation to North**. Similarly, if the input `goal` is `None`, the goal position is the top-right corner of the input `maze`. The output is a list of positions representing the path, with the following constraints:
    - the path must begin from the `starting` position,
    - the path must end at the `goal` position,
    - the path must be _minimal_, i.e., there should be no repetitive positions in the list,
    - the path must not go through any walls or have gaps between positions,
    - the path does not include the final goal position.

_Notice that the path return is not necessarily the actual shortest path between the starting position and the goal position. In general, this will depend on the maze and the algorithm for exploration._

For example, consider the example of the maze and the runner in Part 3, the following path might be the result of the `shortest_path(maze, (5, 2), (10, 4))` function: `[(5, 2, "F"), (5, 3, "F"), (5, 4, "RF"), (6, 4, "F"), (7, 4, "F"), (8, 4, "F"), (9, 4, "F")]`. However, the path `[(5, 2, "F"), (5, 3, "F"), (5, 4, "F"), (6, 4, "B"), (5, 4, "B"), (6, 4, "F"), (7, 4, "F"), (8, 4, "F"), (9, 4, "F")]` is invalid because of repetitions. Similarly, the path `[(5, 2, "F"), (5, 3, "F"), (5, 4, "F"), (7, 4, "F"), (8, 4, "F"), (9, 4, "F")]` is invalid because of gaps.

Think about an algorithm for you to do this. You must ONLY use the the `runner.explore()` function to gain information about the maze. _Any attempts to gain information of the maze through other means will be considered to be INVALID._ You might decide to store additional information while the runner is exploring the maze, or you can construct the path based on the information that the runner got _after_ the exploration.

**_You can have any additional variables, functions, and modules for your implementation you wish._**

**BY THIS STAGE** you should have implemented the `shortest_path()` function in `maze_runner.py`. _Congratulations, you have solved the maze_. You can create some scenarios to validate your implementation by creating a maze, calling the set walls functions (i.e., `add_horizontal_wall()` and `add_vertical_wall()`), and try to call the `shortest_path()` function to find the paths that the runner found.

We provide a test harness for this part. Information about how to download and use the test harness is at [comp1312/2526-Coursework-Tests](https://git.soton.ac.uk/comp1312/2526-Coursework-Tests). **You are expected to extend this to build your own test suits.**

### Part 5. A Maze Creator

_"Tonight we’re taking the fight back to the Creators, no matter what we have to go through to get there."_  
_― James Dashner, The Maze Runner_

Creating the maze "manually" from `add_horizontal_wall()` and `add_vertical_wall()` is cumbersome, especially for large mazes. In this part, we will create mazes by reading from files in the format suggested in Part 3. For example, the following represents a 9 (width) by 5 (height) maze. 

###### `###################`  
`#.................#`  
`#.#.#.#.#.#.#.#.#.#`  
`#.................#`  
`#.#.#.#.#.#.#.#.#.#`  
`#.....#...........#`  
`#.#.#.#.###.#.#.#.#`  
`#.................#`  
`#.#.#.#.#.#.#.#.#.#`  
`#.................#`  
`###################`

The format of the maze is as follows.

- Each line represents either a horizontal line or the row corresponding to a y-coordinate. For example, the 1st line corresponds to the horizontal line 5. the 2nd line corresponds to the row for the y-coordinate of `4`. The following shows the horizontal line and vertical line numbers.  
    
    ```markup
    5 ###################
      #.................#
    4 #.#.#.#.#.#.#.#.#.#
      #.................#
    3 #.#.#.#.#.#.#.#.#.#
      #.....#...........#
    2 #.#.#.#.###.#.#.#.#
      #.................#
    1 #.#.#.#.#.#.#.#.#.#
      #.................#
    0 ###################
      0 1 2 3 4 5 6 7 8 9
    ```
    

Similarly, the following shows the x and y coordinates for the runner's positions within the maze.

```markup
  ###################
4 #.................#
  #.#.#.#.#.#.#.#.#.#
3 #.................#
  #.#.#.#.#.#.#.#.#.#
2 #.....#...........#
  #.#.#.#.###.#.#.#.#
1 #.................#
  #.#.#.#.#.#.#.#.#.#
0 #.................#
  ###################
   0 1 2 3 4 5 6 7 8
```

- The intersections between a horizontal line and a vertical line are always '`#`' (i.e., a single hash symbol).
- The walls (either horizontal or vertical) must be a '`#`'. 
- The path inside the maze must be a dot, i.e., '`.`' (i.e., either there are no walls on the horizontal or vertical lines, or inside a grid cell).
- The external walls must fully enclose the maze (i.e., there are no gaps on the external walls).

Putting this together, vertical walls are at the intersection of the indicated rows and columns in the diagram below. And similarly for the horizontal walls. The diagram also shows the **maze** coordinates.

```markup
+---+-+-+-+-+-+-+-+-+-+ Vertical walls
|   | | | | | | | | | | 
|   v v v v v v v v v v
|   ################### 5 <-+
+-> #.................# 4   |
|   #.#.#.#.#.#.#.#.#.# 4 <-+
+-> #.................# 3   |
|   #.#.#.#.#.#.#.#.#.# 3 <-+
+-> #.....#...........# 2   |
|   #.#.#.#.###.#.#.#.# 2 <-+
+-> #.................# 1   |
|   #.#.#.#.#.#.#.#.#.# 1 <-+
+-> #.................# 0   |
    ################### 0 <-+
    0011223344556677889     |
     ^ ^ ^ ^ ^ ^ ^ ^ ^      |
     | | | | | | | | |      |
     +-+-+-+-+-+-+-+-+------+ Horizontal walls
```

#### Your Tasks

Please complete the following tasks for this part.

- Implement the `maze_reader(maze_file: str)` function in `maze_runner.py`. The input of the function is the name of the input file. The function returns the maze that is constructed from the information of the input files. In particular, you must raise the following errors:
    - Raise an `IOError` when there are problems reading from the input file.
    - Raise a ValueError when the content of the file does not form a proper maze.
- Create a main function, i.e., `if __name__ == "__main__":` use `argparse` to allow `maze_runner.py` to take input from the command line. The description of the command line arguments can be seen below. when running with the `-h` (i.e., help) option.

```markup
usage: maze_runner.py [-h] [--starting STARTING] [--goal GOAL] maze

ECS Maze Runner

positional arguments:
  maze                 The name of the maze file, e.g., maze1.mz

options:
  -h, --help           show this help message and exit
  --starting STARTING  The starting position, e.g., "2, 1"
  --goal GOAL          The goal position, e.g., "4, 5"
```

- - There is one positional argument representing the name of the file containing the maze.
    - There are two optional arguments
        - `starting` to represent the starting position, in the format of `2`, `1`, where `2` is the x-coordinate and `1` is the y-coordinate.
        - goal to represent the goal position, in the same format, e.g., `4, 5` representing the position where `4` is the x-coordinate and `5` is the y-coordinate.
    - Your program MUST handle any errors from the input: errors while reading the maze file, the starting and the goal positions are incorrect (format or out of the dimensions of the maze). In particular, we expect there will be no unhandled exceptions from your program when there are errors in the input.

**_You can have any additional variables, functions, and modules for your implementation you wish._**

**BY THIS STAGE** you should have implemented the `maze_reader()` function in `maze_runner.py`. Moreover, you also created a main function that can take arguments from the command line. _You can then test your maze reader by running the `shortest_path()` function for the maze._ We provide a simple test harness for this part. Information about how to download and use the test harness is at [comp1312/2526-Coursework-Tests](https://git.soton.ac.uk/comp1312/2526-Coursework-Tests). **You are expected to extend this to build your own test suits.**

**Sample Mazes.** We have prepared some sample mazes in the Git repository. We also created a page on the [ECS Student Wiki](https://secure.ecs.soton.ac.uk/student/wiki/w/ECSMazeRunner) for the maze samples.

_**For Maze Developers.** The Wiki page is editable. If you want to share some mazes and provide interesting challenges for your fellow students, please edit the page directly._ 

### Part 6. The Scribe

_"When those doors open, they run the maze, mapping it, memorizing it, trying to find a way out."_  
_― James Dashner, The Maze Runner_

In this part, we will scribe the exploration journey of the runner and the statistics for maze solving. You will need to change your code yourself at this point, but make sure that the APIs mentioned previously do not break. For example, you can add arguments to a function with a default value (so that the tests from the previous part do not break). Your program in `maze_runner.py` will need to write the following two files.

- `exploration.csv` - This file will store the log of the exploration. It is a `csv` file with 4 columns: `Step`, `x-coordinate`, `y-coordinate`, `Actions`. For each entry, step is the sequence number for the step, starting from `1`. The x-coordinate and y-coordinate specify the position of the runner. The last column `Actions` specifies the sequence of actions that take the runner to the next position. The following example has some entries for a run for a tiny (2x2) maze.

```markup
#####
#.#.#
#.#.#
#...#
#####
```

```markup
Step,x-coordinate,y-coordinate,Actions
1,0,0,F
2,0,1,B
3,0,0,LF
4,1,0,LF
```

Note that the list stop just before the runner get to the target position `(1, 1)` (the last actions "LF" will take the runner there).

- `statistics.txt` - This text file contain 5 lines with some statistics.
    1. Line 1: The name of the input file.
    2. Line 2: The score for solving the maze. The formula to compute the score is as follows.   
        `score = exploration_steps / 4 + path_length`  
        where `exploration_steps` is the number of steps used in exploration and `path_length` is the length of the returned shortest path found. For example, in the case of the tiny maze above, the runner uses 4 steps for exploration and (for example) returns the following path `[(0, 0), (1, 0), (1, 1)]` (of length 3). The score for the runner therefore is `4.0`.
    3. Line 3: The number of steps for exploration.
    4. Line 4: The shortest path found.
    5. Line 5: The length of the shortest path found.

**_You can have any additional variables, functions, and modules for your implementation you wish._**

**BY THIS STAGE** you should have implemented the functionality for a complete maze solving, including writing the exploration log and the statistics to files. _You can then test your maze reader by running your program on the sample mazes._ **There are no tests for this part.**

### Finished the Basic Part

Congratulations. You have completed the basic part of the [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework"). Instructions on how to submit our [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") will be below. The deadline is **Friday 12th December 2025 at 16:00**. Note that only **85 out of 100**marks are allocated for the basic part. The other **15** marks are allocated for the extensions.  **You should archive the basic part of your [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") before continuing with the extensions.**

### Extensions

The algorithm you implemented in Part 3 is the left-hug algorithm which for simply connected mazes will always find the solution to the maze but not always in the most efficient way. Can you solve the maze doing less exploration? Implement a different algorithm and get a better maze score (lower scores are better).

**15** marks are available for the implementation of an extension. You only need to implement one algorithm in order to gain these marks. Make sure to document your code and explain the algorithm when you submit the code. You new solution should still use the maze_runner.py command from the basic part.

### [Space Cadets](https://moodle.ecs.soton.ac.uk/course/section.php?id=5778 "Space Cadets")

So far, we have only considered simply connected mazes but other sorts of mazes exist, mazes with loops for example. Implement algorithms that can solve these sorts of mazes. You could also  add a GUI or an animation to visualise the game. We will invite people to a show-and-tell session in the new year to talk about their GUI. **No marks are available for this optional task**. We put the suggestion forward simply for the challenge of it, although you can reasonably expect praise and glory for your efforts.

### Submitting your [Coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework")

You will be submitting your [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") as a zip file. The zip file must be have the following structure:

```markup
basic/
  maze.py
  maze_runner.py
  runner.py
  any other python files for your solution to the basic part
extension/
  maze.py
  maze_runner.py
  runner.py
  any other python files for your solution to the extension part, if you implemented it
cadets/
   your code for space cadets, if you tackled it
```

Only include the extension and cadets directory if you have attempted these parts of the [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework").

Instructions on submitting the zip file will follow.

The deadline for submitting your [coursework](https://moodle.ecs.soton.ac.uk/course/section.php?id=5777 "Coursework") is **Friday 12th December 2025 at 16:00**.

### Relevant Learning Outcomes

1. Basic programming constructs including sequence, selection and iteration, the use of identifiers, variables and expressions, and a range of data types.
2. Good programming style in Python
3. Analyse a problem in a systematic manner
4. Design, implement, debug and test simple programs in Python

### Marking Scheme

|   |   |   |   |
|---|---|---|---|
|**Criterion**|**Description**|Learning Outcomes|Marks|
|Specification|The application meets the specification properly|1, 3, 4|75|
|Style|Good coding style|2|10|
|Extensions|Completion of the extensions|1, 3, 4|15|
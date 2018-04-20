# Implement Search algorithms with Pacman

## Synopsis

In this project, your Pacman agent will find paths through his maze world, both to reach a particular location and to collect food efficiently. You will build general search algorithms and apply them to Pacman scenarios.

You only need to modify search.py and searchAgents.py, and you only need to run autograder.py to complete the exercise. Full instructions are avialable here: http://ai.berkeley.edu/search.html

You can run all of the test cases on your code by opening a terminal and executing the command:


    $ python autograder.py


You can also run individual test cases by executing the command (you can replace "q1" with any of the choices q1-q8):


    $ python autograder.py -q q1


## Instructions

you should be able to play a game of Pacman by typing the following at the command line:


    $ python pacman.py


Pacman lives in a shiny blue world of twisting corridors and tasty round treats. Navigating this world efficiently will be Pacman's first step in mastering his domain.

The simplest agent in searchAgents.py is called the GoWestAgent, which always goes West (a trivial reflex agent). This agent can occasionally win:


    $ python pacman.py --layout testMaze --pacman GoWestAgent


But, things get ugly for this agent when turning is required:


    $ python pacman.py --layout tinyMaze --pacman GoWestAgent


If Pacman gets stuck, you can exit the game by typing CTRL-c into your terminal.

Soon, your agent will solve not only tinyMaze, but any maze you want.

Note that pacman.py supports a number of options that can each be expressed in a long way (e.g., --layout) or a short way (e.g., -l). You can see the list of all options and their default values via:

    
    $ python pacman.py -h


Also, all of the commands that appear in this project also appear in commands.txt, for easy copying and pasting. In UNIX/Mac OS X, you can even run all these commands in order with bash commands.txt.
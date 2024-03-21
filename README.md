## Bounded-NxM-tile-puzzle
#implement a search engine that supports a number of search algorithms to solve the NxM Bounded puzzle game.
In the game there is a board of size NxM containing -1NxM blocks numbered from 1 to -1NxM and an empty block. Some of the blocks are painted
in white and part painted in red. In addition, on each white block is written how many moves can be made with it. The blocks are arranged in a given starting order
any, and the goal is to find the cheapest number of operations from the initial arrangement to the final state. In the final state all the blocks
arranged from 1 to 1NxM from left to right and from top to bottom (regardless of their color), with the empty block in the right corner
bottom For example, if the board is 4x3 then the final state is:
1 2 3 4
5 6 7 8
9 10 11 " "

Note that the color of each block and the amount of allowed moves of the white blocks are part of the definition of the initial state.
the actions
Suitable for the normal puzzle-tile game, where each move counts as one step, in this game there are different rules and different costs.
which depend on the color of the block. Moving a white block costs 1, we want to move it to the empty block only if we have not exceeded the number of moves
allowed for him. Moving a block to the empty block costs 30, and there is no limit to the amount of moves that can be made with it. For example, if
The board is in this state, when blocks 7 and 11 are red, and block 6 is white with a move limit of: 1
We can move 6 to the left and then we can't move it anymore. Then we can move 7 up and 11 to the left, to reach the position
the final The cost of the described route will be 62=30 + 1+30
1 2 3 4
5 6 8
9 10 7 11


The program will read all its input from a single file - txt.input. The first line in the file will determine which algorithm to use:
DFID,* A,* IDA, or DFBnB. The second line in the file will determine whether to print the running time (time with) or not (time no).
The third line will determine whether to print the open list to the screen at each stage of the search algorithm run (open with) or not (no)
open). The fourth line will contain the size of the board in the following format: NxM, a board containing N rows and M columns. In the fifth line
It will be written: White and then a list of the numbers of the white blocks with the limit of each of them. For example, if block 7 is white with
A move limit of 2, and block 2 is also white with a move limit of 3, the list will look like this: (7,2),(2,3):White. If there is none
White blocks The row will only contain the word: White. All other blocks that are not white are red.
After that the arrangement will appear
The beginning of the board by lines, when there are commas between the block numbers. The empty block will be marked as "_". It can be assumed that the input file is valid.


there are added input and output files for example.

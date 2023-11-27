# OSGroupProject
This project uses two programs for the shell program. The first program uses fork to create a child process to execute the user's input (command), wait for the child to terminate and ended terminated the code. The second program uses pthread_create to execute the user's command using threads instead of children.

## What to expect
Test


#### Commands
lookupPath() returns the absolute path of where the command is found
parseCommand() parses the user's command into the name (1st element in the array) and an array argv (command arguments). 
parsePath() parses the system's PATH environment into its individual directories (this helps with searching) the directories for the library where the command may be located)
printPrompt() dynamically prints the user's LOGNAME as the prompt
readCommand() reads the stdin command entered by the user. On the first program we used fork to create a child process to execute the user's input (command), waited for the child to terminate and ended terminated the code

Concurrency vs. Parallelism: Understand the distinction between concurrency and parallelism. Concurrency refers to the ability of a system to handle multiple tasks at the same time, often through interleaved execution, while parallelism involves executing tasks simultaneously using multiple processors or cores. fork() creates separate processes, enabling concurrency, whereas pthread_create() spawns threads within the same process, enabling parallelism.

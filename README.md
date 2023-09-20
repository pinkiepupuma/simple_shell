Creating a simple shell, often referred to as a command-line shell or terminal shell, is a challenging but rewarding project in systems programming. It allows you to understand the fundamentals of how shells work and how they interact with the operating system. Below is an outline of the steps involved in creating a simple shell in C, meeting the project requirements you provided.

Project Overview:

The goal is to create a basic shell program in C that can execute user commands and display their output. The shell should support interactive mode, where the user can enter commands one by one, and non-interactive mode, where it reads commands from standard input or a script file.

Project Structure:

Main Shell Program (hsh.c): This is the main program that handles user input and executes commands. It reads user commands, parses them, and executes them. It also handles interactive and non-interactive modes.

Command Execution (execute_command.c): This module contains functions to execute commands. It handles built-in commands (e.g., exit, cd) and external commands (programs located in /bin, /usr/bin, etc.).

Input Parsing (parse_input.c): This module parses user input, tokenizes it into individual command arguments, and prepares it for execution.

Built-in Commands (builtins.c): This module defines functions for built-in shell commands like exit and cd.

Error Handling (error_handler.c): This module handles error messages and exits gracefully when necessary.

Interactive Mode (interactive.c): This module contains functions to handle the interactive shell mode, where the user interacts with the shell through the terminal.

Non-Interactive Mode (non_interactive.c): This module contains functions to handle the non-interactive shell mode, where the shell reads commands from standard input or script files.

Steps to Implement the Shell:

Read User Input: In interactive mode, use functions like getline to read user input from the terminal. In non-interactive mode, read commands from standard input or a script file.

Parse User Input: Tokenize the user input to separate command arguments and handle special characters like pipes (|), redirection (>, <), and background execution (&).

Execute Commands: Determine if the command is built-in (e.g., exit, cd) or an external command (e.g., /bin/ls). Use fork and execve to execute external commands.

Built-in Command Handling: Implement functions to handle built-in commands like exit and cd. These commands should not be executed using fork and execve.

Error Handling: Handle errors gracefully, such as command not found, permission denied, or invalid input.

Interactive Mode: Implement interactive mode by continuously reading user input and executing commands until the user exits.

Non-Interactive Mode: Implement non-interactive mode by reading commands from standard input or a script file and executing them.

Memory Management: Use dynamic memory allocation functions like malloc and free to manage memory for tokens and other data structures.

Signal Handling: Handle signals like Ctrl+C (SIGINT) gracefully to prevent the shell from exiting unexpectedly.

Cleanup: Ensure that the shell exits gracefully, freeing allocated memory and closing files when the user chooses to exit.

Testing:

Test your shell with a variety of commands, including built-in commands, external commands, and commands with pipes and redirection. Test both interactive and non-interactive modes.

Compilation:

Compile your shell using the provided compilation command, ensuring that it follows the specified options and uses the allowed functions and system calls.

Documentation:

Create a README.md file that describes your project, how to compile and run your shell, and any additional features or design choices you made. Include any collaborators in an AUTHORS file.

Style and Formatting:

Ensure that your code adheres to the Betty style and formatting guidelines, and run the provided betty-style.pl and betty-doc.pl scripts for validation.



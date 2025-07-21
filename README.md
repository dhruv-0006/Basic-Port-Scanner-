# Basic-Port-Scanner-
This project involves developing a Basic Network Security Scanner using Bash scripting. The purpose of this tool is to help identify open and potentially vulnerable ports on a target system (IP or domain). 

________________________________________________________________________________________________________________________________________________________________________________________________________________
Echo defination:- The echo command in Bash (and other Unix shells) is used to display a line of text or a variable value to the terminal or standard output.
Basic Syntax:- 
                echo [option] [string]
            
Example:- echo "Hello, world!"
Prints: Hello, world! 

name="Raju"
echo "My name is $name"
Prints: My name is Raju 

Common options 
| Option | Description                                                           |
| ------ | --------------------------------------------------------------------- |
| `-n`   | Do **not** add a newline at the end.                                  |
| `-e`   | Enables interpretation of **backslash escapes** like `\n`, `\t`, etc. |
| `-E`   | Disables escape interpretation (default behavior).                    |

________________________________________________________________________________________________________________________________________________________________________________________________________________
Read defination:- The read command in Bash is used to take input from the user (or from standard input) and store it in a variable.
Basic Syntax:- read [options] variable_name
Example:- 
          read name
          echo "Hello, $name!"
          
>Prompts the user to type something (e.g., Alice)
>Output: Hello, Alice!

Common options:- 
| Option | Description                                                           |
| ------ | --------------------------------------------------------------------- |
| `-p`   | Prompt the user with a message.                                       |
| `-s`   | Silent mode (useful for passwords; input is hidden).                  |
| `-t`   | Timeout after specified number of seconds.                            |
| `-n`   | Read only **n characters** of input.                                  |
| `-r`   | Raw input mode (does **not** treat backslashes as escape characters). |

________________________________________________________________________________________________________________________________________________________________________________________________________________
Loop defination:- In Bash, a loop is a control structure that allows you to repeat a block of code multiple times — either a fixed number of times or based on a condition.

For Loop:- Used to iterate over a list or a range of values.
For Loop Syntax:- 
         for (( i=1; i<=5; i++ ))
         do
           echo "Iteration $i"
         done

Loop control statement:- 
| Statement  | Description                                                  |
| ---------- | ------------------------------------------------------------ |
| `break`    | Exit the loop immediately                                    |
| `continue` | Skip the rest of the loop block and go to the next iteration |

Example:-
        for i in {1..10}
        do
          if [ $i -eq 5 ]; then
            break
          fi
          echo "Number: $i"
        done

________________________________________________________________________________________________________________________________________________________________________________________________________________
Timeout defination:- The timeout command in Bash is used to run a command with a time limit. If the command runs longer than the specified time, it is automatically terminated.
Basic syntax:-
            timeout [DURATION] [COMMAND] [ARGUMENTS...]
            
>DURATION: How long to wait before stopping the command (e.g., 5, 10s, 2m, 1h)
>COMMAND: The command you want to run
>ARGUMENTS: Any arguments passed to the command

Example:- timeout 3 ping google.com
This will run ping google.com for 3 seconds, then stop it.

Common options:-
| Option              | Description                                                   |
| ------------------- | ------------------------------------------------------------- |
| `--preserve-status` | Exit with the command’s status, even if it times out          |
| `--signal=SIG`      | Send a specific signal when timing out (default is `SIGTERM`) |
| `--kill-after=TIME` | Forcefully kill if it doesn’t stop after timeout              |

Exit codes:-
| Code  | Meaning                          |
| ----- | -------------------------------- |
| `124` | Command timed out                |
| `125` | Timeout itself failed to run     |
| `126` | Command found but cannot execute |
| `127` | Command not found                |
| `0`   | Command completed successfully   |


If else statement defination:- The if-else statement in Bash is used for conditional execution. It allows your script to make decisions based on whether a condition is true or false.
Basic Syntax:- 
             if [ condition ]; then
                 # Commands if condition is true
             else
                 # Commands if condition is false
             fi

Example:- 
read -p "Enter a number: " num

if [ $num -gt 0 ]; then
    echo "Positive number"
else
    echo "Zero or negative number"
fi

Common comparrision operator 
| Operator | Meaning               | Example            |
| -------- | --------------------- | ------------------ |
| `-eq`    | Equal to              | `[ $a -eq $b ]`    |
| `-ne`    | Not equal to          | `[ $a -ne $b ]`    |
| `-gt`    | Greater than          | `[ $a -gt $b ]`    |
| `-lt`    | Less than             | `[ $a -lt $b ]`    |
| `-ge`    | Greater than or equal | `[ $a -ge $b ]`    |
| `-le`    | Less than or equal    | `[ $a -le $b ]`    |
| `==`     | String equality       | `[ "$a" == "$b" ]` |
| `!=`     | String inequality     | `[ "$a" != "$b" ]` |

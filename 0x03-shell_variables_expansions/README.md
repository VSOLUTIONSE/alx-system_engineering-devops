Requirements
A README.md file, at the root of the folder of the project, describing what each script is
.............................................................................
cd alx-system_engineering-devops/
cd 0x03-shell_variables_expansions/
touch README.md
-------------------------------------------------------------------------------------

Tasks
0. <o>
mandatory
Create a script that creates an alias.

Name: ls
Value: rm *

Answer:

#!/bin/bash
alias ls="rm *"


chmod u+x 0-alias
----------------------------------------------------------------------------------------------

1. Hello you
mandatory
Create a script that prints hello user, where user is the current Linux user.

Answer:

#!/bin/bash
echo "hello" $USER

chmod u+x 1-hello_you
-----------------------------------------------------------------------------------------

2. The path to success is to take massive, determined action
mandatory
Add /action to the PATH. /action should be the last directory the shell looks into when looking for a program.

Answer:

#!/bin/bash
export PATH="$PATH:/action"

chmod u+x 2-path
---------------------------------------------------------------------------------------------

3. If the path be beautiful, let us not ask where it leads
mandatory
Create a script that counts the number of directories in the PATH.

Answer:

#!/bin/bash
echo $PATH | tr -s ":" "\n" | wc -l

chmod u+x 3-paths
-----------------------------------------------------------------------------------------

4. Global variables
mandatory
Create a script that lists environment variables.

Answer:

#!/bin/bash
printenv

chmod u+x 4-global_variables
-------------------------------------------------------------------------------------------

5. Local variables
mandatory
Create a script that lists all local variables and environment variables, and functions.

Answer:

#!/bin/bash
set

chmod u+x 5-local_variables
-----------------------------------------------------------------------------------------

6. Local variable
mandatory
Create a script that creates a new local variable.

Name: BEST
Value: School

Answer:

#!/bin/bash
BEST="School"

chmod u+x 6-create_local_variable
-----------------------------------------------------------------------------------------------

7. Global variable
mandatory
Create a script that creates a new global variable.

Name: BEST
Value: School

Answer:

#!/bin/bash
export BEST="School"

chmod u+x 7-create_global_variable
---------------------------------------------------------------------------------------------
8. Every addition to true knowledge is an addition to human power
mandatory
Write a script that prints the result of the addition of 128 with the value stored in the environment variable TRUEKNOWLEDGE, followed by a new line.

Answer:

#!/bin/bash
echo -e $((128 + TRUEKNOWLEDGE))

chmod u+x 8-true_knowledge
------------------------------------------------------------------------------------------------------------

9. Divide and rule
mandatory
Write a script that prints the result of POWER divided by DIVIDE, followed by a new line.

POWER and DIVIDE are environment variables

Answer:

#!/bin/bash
echo $((POWER / DIVIDE))

chmod u+x 9-divide_and_rule
-------------------------------------------------------------------------------------------------------------

10. Love is anterior to life, posterior to death, initial of creation, and the exponent of breath
mandatory
Write a script that displays the result of BREATH to the power LOVE

BREATH and LOVE are environment variables
The script should display the result, followed by a new line

Answer:

#!/bin/bash
echo $((BREATH ** LOVE))

chmod u+x 10-love_exponent_breath
--------------------------------------------------------------------------------------------------------------

11. There are 10 types of people in the world -- Those who understand binary, and those who don't
mandatory
Write a script that converts a number from base 2 to base 10.

The number in base 2 is stored in the environment variable BINARY
The script should display the number in base 10, followed by a new line

Answer:

#!/bin/bash
echo $((2#$BINARY))

chmod u+x 11-binary_to_decimal
---------------------------------------------------------------------------------------------------------------

12. Combination
mandatory
Create a script that prints all possible combinations of two letters, except oo.

Letters are lower cases, from a to z
One combination per line
The output should be alpha ordered, starting with aa
Do not print oo
Your script file should contain maximum 64 characters

Answer:

#!/bin/bash
printf "%s\n" {a..z}{a..z} | grep -v "oo"

chmod u+x 12-combinations
-------------------------------------------------------------------------------------------------------------

13. Floats
mandatory
Write a script that prints a number with two decimal places, followed by a new line.

The number will be stored in the environment variable NUM.

Answer:

#!/bin/bash
printf "%0.2f\n" $NUM

chmod u+x 13-print_float
----------------------------------------------------------------------------------------------------

14. Decimal to Hexadecimal
#advanced
Write a script that converts a number from base 10 to base 16.

The number in base 10 is stored in the environment variable DECIMAL
The script should display the number in base 16, followed by a new line

Answer:

#!/bin/bash
printf '%x\n' $DECIMAL

chmod u+x 100-decimal_to_hexadecimal
---------------------------------------------------------------------------------------------------------

15. Everyone is a proponent of strong encryption
#advanced
Write a script that encodes and decodes text using the rot13 encryption. Assume ASCII.

Answer:

#!/bin/bash
tr '[A-Za-z]' '[N-ZA-Mn-za-m]'

chmod u+x 101-rot13
--------------------------------------------------------------------------------------------------------

16. The eggs of the brood need to be an odd number
#advanced
Write a script that prints every other line from the input, starting with the first line.

Answer:

#!/bin/bash
paste - - | cut -f 1

chmod u+x 102-odd
----------------------------------------------------------------------------------------------------------------

17. I'm an instant star. Just add water and stir.
#advanced
Write a shell script that adds the two numbers stored in the environment variables WATER and STIR and prints the result.

WATER is in base water
STIR is in base stir.
The result should be in base bestchol

Answer:

#!/bin/bash
printf "%o\n" $((5#$(echo $WATER | tr 'water' '01234') + 5#$(echo $STIR | tr 'stir.' '01234'))) | tr '01234567' 'bestchol'

chmod u+x 103-water_and_stir


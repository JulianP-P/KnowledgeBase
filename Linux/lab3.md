### 1
tac lab3.txt | grep "a"
### 4
ls catText.sh file1 2> >(nl >  error)
https://www.gnu.org/software/bash/manual/html_node/Process-Substitution.html

{ ls catText.sh file1 2>&1 1>&3 | nl > error; } 3>&1


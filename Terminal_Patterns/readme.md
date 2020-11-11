# Patterns in macOS Terminal

Shortest one-line version for Bash:

````yes 'c=(╱ ╲);printf ${c[RANDOM%2]}'|bash````

````c=($'—' $'|'); n=${#c[@]}; clear; while :; do printf -- "${c[RANDOM%n]}"; done;````
outputs:

````c=($'  ' $'  ' $'  '); n=${#c[@]}; clear; while :; do printf -- "${c[RANDOM%n]}"; done;````

````c=($'n' $'s'); n=${#c[@]}; clear; while :; do say -r400 "${c[RANDOM%n]}"; done;````
````say -r400                                ````

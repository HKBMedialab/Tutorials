# Patterns in macOS Terminal

Shortest one-line version for Bash:

````yes 'c=(╱ ╲);printf ${c[RANDOM%2]}'|bash````

<img src="./img/10_print_bash.jpg">
<hr>

````c=($'—' $'|'); n=${#c[@]}; clear; while :; do printf -- "${c[RANDOM%n]}"; done;````

<img src="./img/10_print_bash.jpg">
<hr>

````c=($'🌴' $'🌲' $'🌳'); n=${#c[@]}; clear; while :; do printf -- "${c[RANDOM%n]}"; done;````

<img src="./img/10_print_bash.jpg">
<hr>

````c=($'n' $'s'); n=${#c[@]}; clear; while :; do say -r400 "${c[RANDOM%n]}"; done;````

<hr>

````say -r600 🌲🌲🌳🌳🌲🌳🌲🌲🌴🌳🌲🌳🌴🌳🌴🌳🌴````



## Windows PowerShell

Definitely not as funny on Windows as on Mac because PowerShell lacks displaying Emojis and text-to-speech is not preinstalled.

Shortest one-line version of "10 Print Chr$(..." for PowerShell:

````for(){Write-Host(Random("\","/"))-N}````

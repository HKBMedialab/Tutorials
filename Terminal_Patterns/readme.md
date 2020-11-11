# Patterns in macOS Terminal

Shortest one-line version for Bash:

````yes 'c=(╱ ╲);printf ${c[RANDOM%2]}'|bash````

![10_print_in_bash](/img/10_print_bash.png)
***

````c=($’⫸’ $’⫷’); n=${#c[@]}; clear; while :; do printf -- "${c[RANDOM%n]}"; done;;````

![arrow_pattern_bash](/img/arrow_bash.png)
***

````c=($'🌴' $'🌲' $'🌳'); n=${#c[@]}; clear; while :; do printf -- "${c[RANDOM%n]}"; done;````

![forest](/img/forest_bash.png)

***

>Change background color via File > Settings > Profiles > Background.
>Change font color, character spacing and line height via File > Settings > Profiles > Font/Typography.

***

````c=($'n' $'s'); n=${#c[@]}; clear; while :; do say -r400 "${c[RANDOM%n]}"; done;````

***

````say -r600 🌲🌲🌳🌳🌲🌳🌲🌲🌴🌳🌲🌳🌴🌳🌴🌳🌴````
***


## Windows PowerShell

Definitely not as funny on Windows as on Mac because PowerShell lacks displaying Emojis and text-to-speech is not preinstalled.

Shortest one-line version of "10 Print Chr$(..." for PowerShell:

````for(){Write-Host(Random("\","/"))-N}````

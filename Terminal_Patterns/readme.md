# Patterns in macOS Terminal

Shortest one-line version for Bash:

````yes 'c=(╱ ╲);printf ${c[RANDOM%2]}'|bash````

![10_print_in_bash](./img/10_print_bash.png)
***

````yes 'c=(⫸ ⫷);printf ${c[RANDOM%2]}'|bash````

![arrow_pattern_bash](./img/arrow_bash.png)
***

````yes 'c=(🌴 🌲 🌳);printf ${c[RANDOM%3]}'|bash````

![forest](./img/forest_bash.png)

***

## Usage

Replace emojis with any character you want, make spaces in between and set RANDOM% to number of used emojis.

````yes 'c=(1️⃣ 2️⃣ 3️⃣ 4️⃣ 5️⃣);printf ${c[RANDOM%5]}'|bash````

***

## Spaces and Newlines

Special characters and spaces can be used too.
– \t places a tab
– \b backspace, results in a single space
– \n new line
– \r goes back to start of current line
– \v vertical tab, results in a "wave"

````yes 'c=(😀 🐸 "\b" "\b" "\b");printf ${c[RANDOM%5]}'|bash````

***


>GOOD TO KNOW:  
>Change **background color** via File > Settings > Profiles > Background.  
>Change **font color**, **character spacing** and **line height** via File > Settings > Profiles > Font/Typography.

***
Text-to-speech output with `say` command. Use `-rXXX` to specify rate/speed.   
````c=($'n' $'s'); n=${#c[@]}; clear; while :; do say -r400 "${c[RANDOM%n]}"; done;````

***
Text-to-speech is even funnier with emojis. Just copy some lines from an output from above.  
````say -r600 🌲🌲🌳🌳🌲🌳🌲🌲🌴🌳🌲🌳🌴🌳🌴🌳🌴````
***
## Image to Audio
By using a spectrogram player like one of the following, you can listen to your patterns!  
- [Image to Audio, Spectrogram Player](https://nsspot.herokuapp.com/imagetoaudio/) (online)
- [Photosounder](https://www.photosounder.com/) (App, Mac & Win)
- [PixelSynth](https://ojack.xyz/PIXELSYNTH/) (online)

or let in analyze by AI:  
- [Imaginary Soundscape](http://www.imaginarysoundscape.net/) 


## Windows PowerShell

Definitely not as funny on Windows as on Mac because PowerShell lacks displaying emojis and text-to-speech is not preinstalled.

Shortest one-line version of "10 Print Chr$(..." for PowerShell:

````for(){Write-Host(Random("\","/"))-N}````

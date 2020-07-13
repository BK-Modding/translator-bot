# translator-bot
A discord bot that translates a given text repeatedly using Google Translate. For the keks and memes. Originally a Python script by SkullTech, made into a Python Discord bot by BKModding

## What is this and how is this useful?!
This script uses the advanced mind of Google Translate to figure out the hidden meanings behind ordinary english text.
Inspired by the following _meme_-videos.

- [Gucci Gang but it's been Google translated over 500 times](https://youtu.be/HMReGXCtTiM)
- [Pumped Up Kicks but it's been Google translated](https://youtu.be/ZMR395zmT1k)

## Usage

```
Translate text repeatedly using Google Translate. For the keks and memes. 
Originally by SkullTech. Made into a Discord bot by BK Modding

Usage: !translate [-h] [-n NUM] [-l LANGS [LANGS ...]] (-t TEXT)

Required arguments:
-t TEXT, Input text (in quotations)

Optional arguments:
-h HELP, Show this help message and exit
-n NUM,  Number of times to go through the languages.
-l LANGS [LANGS ...], ISO 639-1 codes of the languages to use.

NOTE: All optional arguments must come before the TEXT argument (-t)

The default values of the optional arguments are
    * NUM 10
    * LANGS ['de', 'ko', 'la', 'ja', 'eo']
    
NOTE: total number of translations is NUM * LANGS

Here's a short listing of all the ISO 639-1 codes available:
af sq am ar hy az eu be bn bs bg ca ceb ny zh-cn zh-tw co hr cs da nl en eo et 
tl fi fr fy gl ka de el gu ht ha haw he hi hmn hu is ig id ga it ja jw kn kk 
km ko ku ky lo la lv lt lb mk mg ms ml mt mi mr mn my ne no or ps fa pl pt pa 
ro ru sm gd sr st sn sd si sk sl so es su sw sv tg ta te th tr 
uk ur ug uz vi cy xh yi yo zu

A more detailed listing which includes the corresponding language names can be found here:
https://gist.github.com/BK-Modding/25e5a787486baaabec434bc6a1a96670
```

A detailed listing of the language names and codes can also be found via the googletrans module:
```Python
import googletrans
googletrans.LANGCODES
```

A simple use-case can be as follows
```Discord:
!translate -t "There's vomit on his sweater already, mom's spaghetti"

Output:
[*] "There's vo..." but translated 50 times!

Nikel-spaghete water (water spaghetti nickel) is solved.
```

A more involved use-case which uses all the available arguments.
```Discord
!translate -n 10 -l de ko hi -t "There's vomit on his sweater already, mom's spaghetti"

Output:
[*] "There's vo..." but translated 30 times!

Your sweater is already spaghetti to celebrate your mother.
```

## Requirements for development 
```
Python 3.8.3
discord.py
googletrans
```

## Running the bot
1. Create a `config.py` and add a discord bot token via a `TOKEN` variable
    ```
    TOKEN = "*token goes here*"
    ```
2. Start the bot by running `botscript.py`
    ```
    python3 botscript.py
    ```
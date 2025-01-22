Create a program that will randomly combine words from given text(s) to create unbreakable passwords

The file passgen.py is run in bash script using words.txt as a source of popular words.

By defaults, the program will generate 3 passwords. User will free to choose one of them

This program receives `-w` or `--num_words` as a parameter. Which means it combines 4 words from the source.

```
./passgen.py -w 4 words.txt
IndraBrandParePalaic
CapitoBudletIranicGimp
TunoFrozenMungaNextly
```
Another parameter is `-m` or `--min_word_len` will remove any words shorter than a specific number. This script generates results combine from all words not shorter than 5 characters:

```
./passgen.py -m 5 words.txt
RaggerJobbetTwirlFetter
PhoticLeathOrthisCroton
OddmanRideauToityDarky
```
If user want to generate a specific amount of passwords, the program accept `-n` and `--num` flag. This script returns 6 results: 
```
./passgen.py -n 6 words.txt
TwangyDucapeZapasNepote
PiskBahaySesmaPiper
CuletTalaRhesusNam
BrowstFootyAlumelRebop
TergalHalebiAchrasGuardo
BatedDewcupBesoulWhase
```
If the `--l33t` flag is called, the passwords will obfuscated by substitutions using this table

```
a => @
A => 4
o => 0
O => 0
t => +
e => 3
E => 3
I => 1
S => 5
```
For example, if user want to generate 2 passwords with encryption:

```
./passgen.py -n 2 --l33t words.txt
uNl4yB0rRelpr0XY5Hr1mP/
iNFr4Bo0d1eJ1ng4L3FFe+3!
```
Clearly the passwords will be way stronger: it includes both upper and lower case, numbers and special character, which is a good practice for security.

Password will be hard to remember. So I recommend storing it in a database using [KeePass](https://keepass.info/)
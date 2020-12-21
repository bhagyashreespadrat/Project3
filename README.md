# Project3
#Simple guessing word game in python
# Label program
# author:Bhagyashree
# Location:Pune
# Date:16/11/2020
#Simple guessing word game in python
#completed sucessfully


import random
#user take input
name = input("What is your name? ")
#print user input
print("Good Luck ! ", name)
#predefined word
words = ['rainbow', 'computer', 'science', 'programming',
         'python', 'mathematics', 'player', 'condition',
         'reverse', 'water', 'board', 'geeks']
word = random.choice(words)
print("Guess the characters")
guesses = ''
#how many turns you take
turns = 10
while turns > 0:
    failed = 0
    for char in word:
        if char in guesses:
            print(char)
        else:
            print("_")
            failed += 1

    if failed == 0:
        print("You Win")
        print("The word is: ", word)
        break

    guess = input("guess a character:")
    guesses += guess
    if guess not in word:
        turns -= 1
        print("Wrong")
        print("You have", + turns, 'more guesses')

        if turns == 0:
            print("You Loose")
'''#OUTPUT:What is your name? shankar
Good Luck !  shankar
Guess the characters
_
_
_
_
_
_
_
_
_
guess a character:m
Wrong
You have 11 more guesses
_
_
_
_
_
_
_
_
_
guess a character:p
Wrong
You have 10 more guesses
_
_
_
_
_
_
_
_
_
guess a character:r
Wrong
You have 9 more guesses
_
_
_
_
_
_
_
_
_
guess a character:s
Wrong
You have 8 more guesses
_
_
_
_
_
_
_
_
_
guess a character:p
Wrong
You have 7 more guesses
_
_
_
_
_
_
_
_
_
guess a character:c
c
_
_
_
_
_
_
_
_
guess a character:o
c
o
_
_
_
_
_
o
_
guess a character:n
c
o
n
_
_
_
_
o
n
guess a character:d
c
o
n
d
_
_
_
o
n
guess a character:i
c
o
n
d
i
_
i
o
n
guess a character:t
c
o
n
d
i
t
i
o
n
You Win
The word is:  condition'''

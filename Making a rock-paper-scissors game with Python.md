# Making a rock-paper-scissors game with Python
Items needed:

* Random library
* A variable for the number of game sets
* Two variables to calculate points

### How to install random library
We write in the terminal
```python
pip install random
```
---
## Start making the game
step one: import library
```python
import random
```

## Game sets
Taking the number of game sets from the user and pouring them into a variable
```python
Game_sets=int(input('how many rounds do you want play? '))
```
## Making a loop with the game set condition
We put the terms of the game inside the loop
```python
while Game_sets>0:
    your_choice=input('enter your choice: ')
    game=['sang','kaqaz','qeychi']
    computer=random.choice(game)
    computer_point=0
    you_point=0
    if your_choice=='Rock 'and computer=='Scissors':
        you_point+=1
    if your_choice=='Rock'and computer=='Paper':
        computer_point+=1
    if your_choice=='paper'and computer=='Rock':
        you_point+=1
    if your_choice=='paper'and computer=='Scissors':
        computer_point+=1
    if your_choice=='Scissors'and computer=='Rock':
        computer_point+=1
    if your_choice=='Scissors'and computer=='paper':
        you_point+=1
    print('you(',your_choice,')',  you_point,    'com(',computer,')', computer_point)
    Game_sets-=1
```
Each time this loop is executed, one set is subtracted from the game
## Choose the winner of the game
```python
if you_point>computer_point:
    print('you win')
if computer_point>you_point:
    print('you lose')
```

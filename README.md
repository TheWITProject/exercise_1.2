## Summary
You will be debugging some mini-programs on [repl.it](https://www.repl.it/). When you have fixed a problem, please copy and paste the solution into the codeblock below each question and briefly explain what was wrong.

Before you get started:
- clone this repo
- create and checkout a personal branch of this repo `git checkout -b <YOUR_NAME>_exercise_1.2`

When you are done:
- push up your personal branch `git push origin <YOUR_NAME>_exercise_1.2`
- open a PR for your branch


## Exercises

#### Syntax Errors
- [Address Book](https://repl.it/@Admin7/addressbookpy)
```python
friends = {
  'joe': {
    'address': '21 Higbie Lane',
  },
  'bill': {
    'address': '42953 Green Street',
  },
  'edie': {
    'address': '2134 Pennsylvania Avenue'
  },
}
ok = list(friends.get('edie').values())[0]
print(f'Their address is {ok}!')
```
If you want to access edie's address, you have to get the dictionary values under the key 'edie', and then turn it into a list so you can index it and print the address. You cannot access the keys & values by doing dict.key.value.

- [Alternative Facts](https://repl.it/@Admin7/alternativefactspy)
```python
def changeStatement():
    return  not truth
```
Because variable truth is already defined outside of the function, to change it you can return "not" truth to change the statement to False from True.

- [My Object](https://repl.it/@Admin7/myobject)
```python
my_object = {
    'wow': {
        'im great at python': True
    },
    'woohoo': { 'i get better everyday'},
    'my_skills': {
        'python': True,
        'HTML': True,
        'CSS': False
    }
}
```
The curly brackets must be in the correct locations, and a bracket cannot be used to close a dictionary (unless you used a beginning bracket to start a list).

- [Red Light](https://repl.it/@Admin7/redlight)
```python
STOP = 'STOP'
PROCEED = 'PROCEED'
CAUTION = 'CAUTION'
state = 'state'

red_light = {
  state: STOP,
}

def cycleStopLight (red_light):
  if red_light[state] == STOP:
    red_light[state] = PROCEED
  elif red_light[state] == PROCEED:
    red_light[state] = CAUTION
  else:
    red_light[state] = STOP
```
The variable state must be assigned to something before it can be used as a key, or you cannot create the dictionary. Dictionary keys also cannot be called by .key, they instead can be called by dict[key]. 

#### Let's Take It Further
<details>
<summary>This game of tic tac toe is really buggy. Can you figure out everything that's wrong? Only toggle this is you're not sure.</summary>


- Well, to start, users can overwrite each others' moves.
- It looks like the game might end early...
- The user isn't alternating, is it?

</details>

Try to use all of the skills you learned today to debug this game and make sure it's ready to use!


- [Tic Tac Toe](https://repl.it/@Admin7/tictactoe)
```python
theBoard = {'7': ' ' , '8': ' ' , '9': ' ' ,
            '4': ' ' , '5': ' ' , '6': ' ' ,
            '1': ' ' , '2': ' ' , '3': ' ' }

board_keys = []

for key in theBoard:
    board_keys.append(key)

def printBoard(board):
    print(board['7'] + '|' + board['8'] + '|' + board['9'])
    print('-+-+-')
    print(board['4'] + '|' + board['5'] + '|' + board['6'])
    print('-+-+-')
    print(board['1'] + '|' + board['2'] + '|' + board['3'])

def game():

    turn = 'X'
    count = 0

    for i in range(10):
        printBoard(theBoard)
        print("It's your turn, " + turn + ". Pick a place.")

        move = input()
        if theBoard[move] == ' ':        
          theBoard[move] = turn
        else:
          print("Oops, that spot is already taken! Pick another place.")
          move = input()
          theBoard[move] = turn

        if count%2 == 0:
          turn = 'X'
        else:
          turn = 'O'
        count += 1

        if count >= 5:
            if theBoard['7'] == theBoard['8'] == theBoard['9'] == 'X' or theBoard['7'] == theBoard['8'] == theBoard['9'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")                
                break
            elif theBoard['4'] == theBoard['5'] == theBoard['6'] == 'X' or theBoard['4'] == theBoard['5'] == theBoard['6'] == 'O': 
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break
            elif theBoard['1'] == theBoard['2'] == theBoard['3'] == 'X' or theBoard['1'] == theBoard['2'] == theBoard['3'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break
            elif theBoard['1'] == theBoard['4'] == theBoard['7'] == 'X' or theBoard['1'] == theBoard['4'] == theBoard['7'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break
            elif theBoard['2'] == theBoard['5'] == theBoard['8'] == 'X' or theBoard['2'] == theBoard['5'] == theBoard['8'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break
            elif theBoard['3'] == theBoard['6'] == theBoard['9'] == 'X' or theBoard['3'] == theBoard['6'] == theBoard['9'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break 
            elif theBoard['7'] == theBoard['5'] == theBoard['3'] == 'X' or theBoard['7'] == theBoard['5'] == theBoard['3'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break
            elif theBoard['1'] == theBoard['5'] == theBoard['9'] == 'X' or theBoard['1'] == theBoard['5'] == theBoard['9'] == 'O':
                printBoard(theBoard)
                print("\nGame Over.\n")                
                print(" **** " + turn + " won. ****")
                break 

        if count == 9:
            print("\nGame Over.\n")                
            print("It's a Tie!!")

        if turn == 'X':
            turn = 'O'
        else:
            turn = 'X'        
    
    restart = input("Do want to play Again?(y/n)")
    if restart == "y" or restart == "Y":  
        for key in board_keys:
            theBoard[key] = " "

        game()

if __name__ == "__main__":
    game()
```


## Done already?
Practice problems on [CodeWars](https://codewars.com).


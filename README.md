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
```
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

print('Their address is', friends['edie']['address'],'!')
```

- [Alternative Facts](https://repl.it/@Admin7/alternativefactspy)
```
truth = True
def changeStatement():
    truth = False
changeStatement()
```

- [My Object](https://repl.it/@Admin7/myobject)
```
my_object = {
    'wow': {
        'im great at python': True
    },
    'woohoo': 'i get better everyday',
    'my_skills': {
        'python': True,
        'HTML': True,
        'CSS': False
    }
}
```

- [Red Light](https://repl.it/@Admin7/redlight)
```
STOP = 'STOP'
PROCEED = 'PROCEED'
CAUTION = 'CAUTION'

red_light = {
  'state': STOP,
}

def cycleStopLight (red_light):
  if red_light['state'] == STOP:
    red_light['state'] = PROCEED
  elif red_light['state'] == PROCEED:
    red_light['state'] = CAUTION
  elif red_light['state'] == CAUTION:
    red_light['state'] = STOP

cycleStopLight(red_light)
print(red_light)

cycleStopLight(red_light)
print(red_light)

cycleStopLight(red_light)
print(red_light)
```


#### Let's Take It Further
<details>
<summary>This game of tic tac toe is really buggy. Can you figure out everything that's wrong? Only toggle this is you're not sure.</summary>


- Well, to start, users can overwrite each others' moves.
- It looks like the game might end early...
- The user isn't alternating, is it?

</details>

Try to use all of the skills you learned today to debug this game and make sure it's ready to use!


- [Tic Tac Toe](https://repl.it/@Admin7/tictactoe)
```
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
        print("It's your turn," + turn + ". Pick a place.")

        move = input()
        while(theBoard[move] == 'X'  or theBoard[move] == 'O'):
          print("That place is taken. Please choose another another move.")
          move = input()
        theBoard[move] = turn
        #turn = count
        
        # if turn =='X':
        #     turn = 'O'
        # else:
        #     turn = 'X' 
        count += 1

        if count >= 5:
          if theBoard['7'] == theBoard['8'] == theBoard['9'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")                
              break
          elif theBoard['4'] == theBoard['5'] == theBoard['6'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break
          elif theBoard['1'] == theBoard['2'] == theBoard['3'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break
          elif theBoard['1'] == theBoard['4'] == theBoard['7'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break
          elif theBoard['2'] == theBoard['5'] == theBoard['8'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break
          elif theBoard['3'] == theBoard['6'] == theBoard['9'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break 
          elif theBoard['7'] == theBoard['5'] == theBoard['3'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break
          elif theBoard['1'] == theBoard['5'] == theBoard['9'] != ' ': 
              printBoard(theBoard)
              print("\nGame Over.\n")                
              print(" **** " + turn + " won. ****")
              break
        elif count == 9:
            print("\nGame Over.\n")                
            print("It's a Tie!!")
            break
            
        # if count == 5:
        #     print("\nGame Over.\n")                
        #     print("It's a Tie!!")
        #     break

        if turn =='X':
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


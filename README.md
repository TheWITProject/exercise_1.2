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
print('Their address is ' + friends['edie']['address'] + '!')

# The problems here were:
  - The strings need to be separated by the calls to the dictionary with concatenation
  - Syntax for getting the value from the friends dictionary was wrong --> need brackets instead of periods
  - 'Edie' was mispelled
  - Need quotes around key names
```

- [Alternative Facts](https://repl.it/@Admin7/alternativefactspy)
```python
def changeStatement():
    return not truth
print(changeStatement())

# The problems here were:
  - Missing return statement
  - Missing print function
```

- [My Object](https://repl.it/@Admin7/myobject)
```python
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

# The problem here was:
  - Extra bracket
```

- [Red Light](https://repl.it/@Admin7/redlight)
```python
# copy & paste your solution here
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
```python
# copy & paste your solution here
```


## Done already?
Practice problems on [CodeWars](https://codewars.com).


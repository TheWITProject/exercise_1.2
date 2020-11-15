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
# copy & paste your solution here
```

- [My Object](https://repl.it/@Admin7/myobject)
```python
# copy & paste your solution here
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


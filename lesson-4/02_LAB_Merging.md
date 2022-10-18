# Instructions

We'll practise going through the 3 merging scenarios we've seen.

1. Create a new folder called beef-stew. Make a git repo out of it
2. Create a file called "ingredients.txt", and commit empty file.
3. Open the file, and commit in the following under the `main` branch:

```
olive oil
beef chuck
sweet onion
garlic
flour
tomato paste
salt + pepper
```

4. Your friend decides they're going to make a veg-heavy version. Make a new branch called `vegetables-heavy`
5. Commit in addition to the above:

```
carrots
celery
mushrooms
russet potato
frozen peas
```

6. Another friend wants to spice up the stew. Branch off `main` again and commit the following to a new branch `more-spices` in a new file called `more-spices.txt`:
```
Worcestershire sauce
dry red wine
thyme
bay leaves
parsley
smoked paprika
herbes de Provence
cloves
```

**Feel free to try the various merges to check whether you are correct!**

Q1. If merging branches, where would you expect a fast-forward merge to occur?

a) `vegetables-heavy` onto `main`<br>
b) `vegetables-heavy` onto `more-spices`<br>
c) `more-spices` onto `main`<br>
c) a and b only<br>
d) b and c only<br>
e) a and c only <br>
f) a, b, and c<br>
g) none of the above<br>

Q2. If merging branches, where would you expect a conflict to occur?

a) `vegetables-heavy` onto `main`<br>
b) `vegetables-heavy` onto `more-spices` <br>
c) `more-spices` onto `main`<br>
d) a and b only<br>
e) b and c only<br>
f) a and c only<br>
g) a, b, and c<br>
h) none of the above<br>

7. You realise you forgot to add a key ingredient in the `main` branch's ingredient file. Circle back and commit in ingredients.txt:

```
beef stock
```

Q3. If merging branches now, where would you expect a no-conflict merge(s) to occur?

a) `vegetables-heavy` onto `main`<br>
b) `vegetables-heavy` onto `more-spices`<br>
c) `more-spices` onto `main`<br>
d) a and b only<br>
e) b and c only<br>
f) a and c only<br>
g) a, b, and c<br>
h) none of the above <br>

Q4. If merging branches now, where would you expect a merge commit with conflict(s) to occur?

a) `vegetables-heavy` onto `main`<br>
b) `vegetables-heavy` onto `more-spices`<br>
c) `more-spices` onto `main`<br>
d) a and b only<br>
e) b and c only<br>
f) a and c only<br>
g) a, b, and c <br>
h) none of the above<br>


8. Merge  `more-spices` to `main` and resolve conflicts if necessary.
9. Merge `vegetables-heavy` to `main` and resolve conflicts if necessary.
10. Run a command to see commit logs across all branches (BONUS, if you do a graph!)
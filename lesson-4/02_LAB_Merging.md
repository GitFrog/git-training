# Instructions

We'll practise going through the 3 merging scenarios we've seen.

1. Create a new folder called beef-stew. Make a git repo out of it
2. Create a file called "ingredients.txt"
3. Commit in the following under the `main` branch:

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
carrrots
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

Q1. If merging branches, where would you expect a fast-forward merge to occur?
a) `vegetables-heavy` onto `main`
b) `vegetables-heavy` onto `more-spices`
c) `more-spices` onto `main`
d) a and b only
e) b and c only
f) a and c only 

Q2. If merging branches, where would you expect a merge commit to occur?
a) `vegetables-heavy` onto `main`
b) `vegetables-heavy` onto `more-spices` 
c) `more-spices` onto `main`
d) a and b only
e) b and c only
f) a and c only


7. You realise you forgot to add a key ingredient in the `main` branch's ingredient file. Circle back and commit in ingredients.txt:

```
beef stock
```

Q3. If merging branches now, where would you expect a no-conflict merge(s) to occur?
a) `vegetables-heavy` onto `main`
b) `vegetables-heavy` onto `more-spices`
c) `more-spices` onto `main`
d) a and b only
e) b and c only 
f) a and c only

Q2. If merging branches now, where would you expect a merge commit with conflict(s) to occur?
a) `vegetables-heavy` onto `main`
b) `vegetables-heavy` onto `more-spices`
c) `more-spices` onto `main`
d) a and b only
e) b and c only
f) a and c only

8. Merge  `more-spices` and resolve conflicts as necessary.
9. Merge `vegetables-heavy` and resolve conflicts as necessary.

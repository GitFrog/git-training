# Instructions

1. Clone the following package https://github.com/salexir/countries from github . If you run into proxy issues, there's a zip file that can be exported. Ask whoever's teaching this.

2. Go into the folder and find the country-info.txt. You should see six commits that loosely corresponds to "countries".

3. Look back into the commit history to determine when changes were still based in reality (as in all the data was correct)

4. Once located, create a branch at that commit called "reality"

5. Switch back to the tip of the main line to ensure that data between the two are different.

6. You notice two errors in the Canada entry. Fix these in the main line (but not the other fantastical entries), and commit.

7. At this newest commit, commit another entry of your choice, but it has to be a fantastical world (feel free to add your own data elements/ignore the ones in there)

8. Create a new branch at this point called "fantasy"

9. Switch back to "reality", and delete the entries for Mexico, Canada, and the USA. Save, but don't commit.

10. Tricked you! #9 was an error. Using a git command, discard the latest changes you just made.


11. Now that that's fixed, delete the entry for antiga-and-barbuda, but commit this time...........

12. Tricked... again.  Using a git command, discard the latest changes you just made.

13. Switch to the `fantasy` branch. Delete all entries, and commit the result.

14. You start writing a fantastical entry having sworn you had started that file previously. You save, but don't commit. If you're running out of ideas, here's something to copy-paste:

```
    aiur:
        region: koprulu-sector
        capital: aiur
        official-language-1: khalani
        official-language-2: 
        driving-direction: probably-right..?

```


15.  Your inkling was correct! You had deleted the previous entries by... mistake! Undo the deletion, making sure that your new saved entry is not overwritten.

16. Add and commit the latest entry from 14.

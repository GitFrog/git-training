# Drafting the Magna Carta

In this lab, we'll go back to 1215 and pretend we're drafting up the Magna Carta!

![A meme on King John requiring a haircut](assets/magnacarta.jfif)
[Source](https://twitter.com/MarxMedia/status/1331357246975057921/photo/1)

Unfortunately, the various legislators -- while having access to computers and git -- did not
really understand how merging works.

The goal of this lab is to create merge all the clauses together into one document. There might be conflicts..!

# Set it up 

First, execute these commands to clone the `magna-carta` repo, and all the branches:

```bash

git clone https://github.com/salexir/magna-carta

cd magna-carta/


# apologies for not following DRY principles here :|

git switch legislator-1
git switch legislator-2
git switch legislator-3
git switch legislator-4
git switch legislator-5
git switch legislator-6
git switch final-copy


```

NOTE: a git log will show a new kind of pointer in this form: "origin/..". Please ignore these for now, we will discuss them in the next part.


# Instructions

1. The goal is to merge all the clauses together, and only modify the files as necessary during merge conflicts.

2. Using only the branch called `final-copy`, merge all the appropriate branches so that all the clauses are in chronological order, and with no overlap.

3. As a last step in `final copy` delete all clauses that do not start with a `+` symbol.

3. This is fairly self-directed. There is no one way to get to the final state!


# On Magna Carta

Magna Carta, meaning ‘The Great Charter’, is one of the most famous documents in the world. Originally issued by King John of England (r. 1199–1216) as a practical solution to the political crisis he faced in 1215, Magna Carta established for the first time the principle that everybody, including the king, was subject to the law. Although nearly a third of the text was deleted or substantially rewritten within ten years, and almost all the clauses have been repealed in modern times, Magna Carta remains a cornerstone of the British constitution.


Most of the 63 clauses granted by King John dealt with specific grievances relating to his rule. However, buried within them were a number of fundamental values that both challenged the autocracy of the king and proved highly adaptable in future centuries. Most famously, the 39th clause gave all ‘free men’ the right to justice and a fair trial. Some of Magna Carta’s core principles are echoed in the United States Bill of Rights (1791) and in many other constitutional documents around the world, as well as in the Universal Declaration of Human Rights (1948) and the European Convention on Human Rights (1950).

Source: https://www.bl.uk/magna-carta/articles/magna-carta-an-introduction


# Clauses

Clauses marked (+) are still valid under the charter of 1225, but with a few minor amendments. Clauses marked (*) were omitted in all later reissues of the charter. In the charter itself the clauses are not numbered, and the text reads continuously. The translation sets out to convey the sense rather than the precise wording of the original Latin.

Source: https://www.bl.uk/magna-carta/articles/magna-carta-english-translation

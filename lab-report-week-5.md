# Lab Report Week 5
Command that was chosen: `grep` (searches a file for the given string and prints matching lines).
## 1. grep -r
`grep -r` recursively searches for a specified pattern in all files and directories. This command is useful when it comes to searching big file systems to find specific strings.
(Source from [ChatGPT.](https://chat.openai.com/chat))

### Example 1:

Command:
```
grep -r "Shellfish" written_2
```
Output:
```
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:The seafood and fish of the Mediterranean provide some of the coast’s most memorable meals. A great favourite is zarzuela de mariscos, a variation of a Catalan 
dish, which combines many different ingredients, just like the Spanish operetta from which it takes its name. Shellfish is served with rice in an unlikely but very tasty sauce of olive oil, ground almonds, assorted spices, and chocolate, though local cooks sometimes cheat a bit by adding octopus and other shell-less tidbits.
```

### Example 2:

Command:
```
grep -r "Berlioz" written_2
```
Output:
```
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:The principal cemetery of Montmartre, where luminaries of the arts such as the composers Berlioz and Offenbach lie buried, may seem a world away, but it’s only a short walk west from the Moulin Rouge to the entrance (west past the Moulin Rouge, then right at avenue Rachel).
```

## 2. grep -E
`grep -E` searches for a pattern in a file using extended regular expression, which allows for more complex pattern matching (Source from [ChatGPT](https://chat.openai.com/chat)). Cmmands can also be used together, such as `-E` and `-r`. We can search more specifically with `-E` by using commands such as `^name`, which will list everything that has `name` in the first line of a sentence.

### Example 1:

Command:
```

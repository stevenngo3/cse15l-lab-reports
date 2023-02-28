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
With this command, the `grep -r` will recursively search through the `written_2` directory and all of its subdirectories to look for files that has "Shellfish". As shown in the output, the terminal will show the file and the line that contains the text "Shellfish".

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
This command is the same as the previous example, as it will recursively grep through the `written_2` directory and all of its subdirectories to look for files that has "Berlioz". As shown in the output, the terminal will show the file and the line that contains the text "Berlioz".

Output:
```
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:The principal cemetery of Montmartre, where luminaries of the arts such as the composers Berlioz and Offenbach lie buried, may seem a world away, but it’s only a short walk west from the Moulin Rouge to the entrance (west past the Moulin Rouge, then right at avenue Rachel).
```

## 2. grep -E
`grep -E` searches for a pattern in a file using extended regular expression, which allows for more complex pattern matching (Source from [ChatGPT](https://chat.openai.com/chat)). Commands can also be used together, such as `-E` and `-r`. We can search more specifically with `grep -E` by using commands such as `^name`, which will list everything that has `name` in the first line of a sentence.

### Example 1:

Command:
```
grep -E "^Rice" -r written_2
```
This command will recursively search through the `written_2` directory and all of its subdirectories to look for files that has the text "Rice" at the beginning of a line. As shown in the output, the terminal shows all the files that contains "Rice", and the line the specified text is at the beginning of.

Output:
```
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:Rice and Paella
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:Rice and fish dishes make up a substantial part of the local diet. However, meat is used in regional cooking, though in nothing like the same range and imaginative presentation.
```
### Example 2:

Command:
```
grep -E "^Outdoor" -r written_2 
```
Like the previous example, this command will recursively search through the `written_2` directory and all of its subdirectories to look for files that has the text "Outdoor" at the beginning of a line. As shown in the output, the terminal shows all the files that contains "Outdoor", and the line the specified text is at the beginning of.

Output:
```
written_2/travel_guides/berlitz2/China-WhereToGo.txt:Outdoor markets, where visitors must bargain at length, are another walking adventure. Silk Alley, the most famous and most overpriced, specializes in designer fashions. More clothes and furs are found at Yabao Market, near Ritan Park (popularly known as the Russian Market). The Hongxiao Market, near the Temple of Heaven, features clothing, crafts, and freshwater pearls. The most 
colorful market is Panjiayuan (know as the Dirt Market), starting at sunrise every Sunday, with its stalls of collectibles, antiques, family treasures, tomb art, Tibetan rugs, furniture, and Mao memorabilia.
written_2/travel_guides/berlitz2/China-WhereToGo.txt:Outdoor enthusiasts and independent travelers might have time to explore two of Hunan’s most spectacular natural attractions. The Southern Heng Mountain (Hengshannan, also called Nanyue), one of China’s Five Sacred Mountains in the ancient Daoist pantheon, is 112 km (70 miles) south of Changsha. Its temples, monasteries, and misty vistas are well worth a day’s hike. Wulingyuan, a 
large nature preserve better known to the Chinese as Zhangjiajie, is 350 km (217 miles) west of Changsha. Known as “China’s Yellowstone,” this UNESCO World Heritage Site is a remote park of spectacular and uncanny quartz labyrinths and pinnacles, massive limestone caves, white-water rapids, steep hiking trails, and minority villages.
```

## 3. grep -n
`grep -n` prints out the line number in the file that contains the pattern. (Source from [ChatGPT](https://chat.openai.com/chat)). This command is useful because if a text file is too long and you are trying to find a specific word, `grep -n` will show what line number that specific word is on.

### Example 1:

Command:
```
grep -n "Chicken" -r written_2
```
This command will recursively search through the `written_2` directory and all of its subdirectories to look for files that has the text "Chicken", as well as the line number that it is in. As shown in the output, the terminal will show all the files that has "Chicken" and what line number the text is in. 

Output:
```
written_2/travel_guides/berlitz1/HandRIsrael.txt:211:        Country Chicken ❁ The Tourist Center; Tel. (07) 637 1312.
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:84:The ruminative buffalo pulls plows and carts, then wallows in the mud of a village pond. Chickens run in and out of doorways and often may be seen peering out from roosts on the second floor of houses. Under the eaves, bundles of maize hang to dry along with large cucumbers. Pumpkin vines climb over rooftops.
written_2/travel_guides/berlitz2/NewOrleans-History.txt:52:In Louisiana, politics and politicians have always been a fascinating business — and business is the word — but none of the bosses could compare with larger-than-life Huey P. Long (1893–1935). Long was cagey, ambitious, poor, and so bright he graduated from Tulane Law School less than a year after he entered. At the age of 25 he was elected to the state public service commission; as governor he built roads and bridges that were desperately needed, and supplied all the state’s school children with free textbooks. His slogans were “Every Man a King” and “A Chicken in Every Pot.”
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:69:East of the town of Yabucoa you’ll find the start of the Ruta Panoramica. If you don’t have time to follow this entire trail, at least drive along Route 3 south of Yabucoa to the area around the Cendro la Pandura peak. The road climbs via a series of switchback turns, and once at the top you’ll have a clear view of the town lying in the flat plain below. The lifestyle of the people who live high on the hillside is fascinating. Jíbaros (country farmers) carry machetes to the fields, accompanied by their faithful hounds. Chickens scoot under cars as you approach. Around every turn, you’ll marvel at how the houses can be built on such precipitous slopes. The road then leads along the southern coastal plain through several small towns to Playa de Ponce.
```

### Example 2:

Command:
```
grep -n "Shoes" -r written_2
```
Like the previous example, this command will recursively search through the `written_2` directory and all of its subdirectories to look for files that has the text "Shoes", as well as the line number that it is in. As shown in the output, the terminal will show all the files that has "Shoes" and what line number the text is in. 

Output:
```
written_2/travel_guides/berlitz1/WhatToIbiza.txt:166:        •Shoes: ordinary shoes for both men and women can be quite
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:69:A pretty little village of pastel-colored clapboard houses, Hope Town is full of friendly locals. Kids run safely in the streets of the traffic-free town center and along the Queens Highway, only slightly wider than a sidewalk. Shoes are optional in the bars at the water’s edge, and as the sun sets you’ll hear a thousand stories here about the one that got away. Watch out for the sign “Tourists treated just like locals,” for you’ll soon feel as though you’ve lived here forever. You’ll be exchanging greetings, and before you know it, life stories. The Wyannie Malone Historical Museum on Queens Highway is the place to find out more about these fascinating people and their home island.
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt:15:Leather. You can find a very good selection of fashionable, relatively inexpensive shoes and handbags. Leather belts, bags, and shoes are very popular buys. Shoes are just about as fashionable as in Spain and Italy, and are cheaper.
```

## 4. grep -c
`grep -c` prints the number of times the pattern appears in a file. (Source from [ChatGPT](https://chat.openai.com/chat)). This command is useful as it can tell you how many times a word has appeared in a file (can tell you what a file is mainly about).

### Example 1:

Command:
```
grep -c "celebrities" -r written_2
```
This command will recursively search through the `written_2` directory and all of its subdirectories to look for files that has the text "celebrities", and how many times this text shows up in the file. As shown in the output, there are only some files that contains the word "celebrities" and it seems that they only appear once in the file. If you really want to look for celebrities, Los Angeles would be a good choice to find some as the where to go file contains the keyword "celebrities" 11 times.

Output:
```
written_2/non-fiction/OUP/Abernathy/ch1.txt:0
written_2/non-fiction/OUP/Abernathy/ch14.txt:0
written_2/non-fiction/OUP/Abernathy/ch15.txt:1
written_2/non-fiction/OUP/Abernathy/ch2.txt:0
written_2/non-fiction/OUP/Abernathy/ch3.txt:0
written_2/non-fiction/OUP/Abernathy/ch6.txt:0
written_2/non-fiction/OUP/Abernathy/ch7.txt:0
written_2/non-fiction/OUP/Abernathy/ch8.txt:0
written_2/non-fiction/OUP/Abernathy/ch9.txt:0
written_2/non-fiction/OUP/Berk/ch1.txt:0
written_2/non-fiction/OUP/Berk/ch2.txt:0
written_2/non-fiction/OUP/Berk/CH4.txt:0
written_2/non-fiction/OUP/Berk/ch7.txt:0
written_2/non-fiction/OUP/Castro/chA.txt:0
written_2/non-fiction/OUP/Castro/chB.txt:0
written_2/non-fiction/OUP/Castro/chC.txt:0
written_2/non-fiction/OUP/Castro/chL.txt:0
written_2/non-fiction/OUP/Castro/chM.txt:0
written_2/non-fiction/OUP/Castro/chN.txt:0
written_2/non-fiction/OUP/Castro/chO.txt:0
written_2/non-fiction/OUP/Castro/chP.txt:0
written_2/non-fiction/OUP/Castro/chQ.txt:0
written_2/non-fiction/OUP/Castro/chR.txt:0
written_2/non-fiction/OUP/Castro/chV.txt:0
written_2/non-fiction/OUP/Castro/chW.txt:0
written_2/non-fiction/OUP/Castro/chY.txt:0
written_2/non-fiction/OUP/Castro/chZ.txt:0
written_2/non-fiction/OUP/Fletcher/ch1.txt:0
written_2/non-fiction/OUP/Fletcher/ch10.txt:0
written_2/non-fiction/OUP/Fletcher/ch2.txt:0
written_2/non-fiction/OUP/Fletcher/ch5.txt:0
written_2/non-fiction/OUP/Fletcher/ch6.txt:0
written_2/non-fiction/OUP/Fletcher/ch9.txt:0
written_2/non-fiction/OUP/Kauffman/ch1.txt:0
written_2/non-fiction/OUP/Kauffman/ch10.txt:0
written_2/non-fiction/OUP/Kauffman/ch3.txt:0
written_2/non-fiction/OUP/Kauffman/ch4.txt:0
written_2/non-fiction/OUP/Kauffman/ch5.txt:0
written_2/non-fiction/OUP/Kauffman/ch6.txt:0
written_2/non-fiction/OUP/Kauffman/ch7.txt:0
written_2/non-fiction/OUP/Kauffman/ch8.txt:0
written_2/non-fiction/OUP/Kauffman/ch9.txt:0
written_2/non-fiction/OUP/Rybczynski/ch1.txt:0
written_2/non-fiction/OUP/Rybczynski/ch2.txt:0
written_2/non-fiction/OUP/Rybczynski/ch3.txt:0
written_2/travel_guides/berlitz1/HandRHawaii.txt:0
written_2/travel_guides/berlitz1/HandRHongKong.txt:0
written_2/travel_guides/berlitz1/HandRIbiza.txt:0
written_2/travel_guides/berlitz1/HandRIsrael.txt:0
written_2/travel_guides/berlitz1/HandRIstanbul.txt:0
written_2/travel_guides/berlitz1/HandRJamaica.txt:0
written_2/travel_guides/berlitz1/HandRJerusalem.txt:0
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:0
written_2/travel_guides/berlitz1/HandRLasVegas.txt:0
written_2/travel_guides/berlitz1/HandRLisbon.txt:0
written_2/travel_guides/berlitz1/HandRLosAngeles.txt:0
written_2/travel_guides/berlitz1/HandRMadeira.txt:0
written_2/travel_guides/berlitz1/HandRMadrid.txt:0
written_2/travel_guides/berlitz1/HandRMallorca.txt:0
written_2/travel_guides/berlitz1/HistoryDublin.txt:0
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:0
written_2/travel_guides/berlitz1/HistoryEgypt.txt:0
written_2/travel_guides/berlitz1/HistoryFrance.txt:0
written_2/travel_guides/berlitz1/HistoryFWI.txt:0
written_2/travel_guides/berlitz1/HistoryGreek.txt:0
written_2/travel_guides/berlitz1/HistoryHawaii.txt:0
written_2/travel_guides/berlitz1/HistoryHongKong.txt:0
written_2/travel_guides/berlitz1/HistoryIbiza.txt:0
written_2/travel_guides/berlitz1/HistoryIndia.txt:0
written_2/travel_guides/berlitz1/HistoryIsrael.txt:0
written_2/travel_guides/berlitz1/HistoryIstanbul.txt:0
written_2/travel_guides/berlitz1/HistoryItaly.txt:0
written_2/travel_guides/berlitz1/HistoryJamaica.txt:0
written_2/travel_guides/berlitz1/HistoryJapan.txt:0
written_2/travel_guides/berlitz1/HistoryJerusalem.txt:0
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt:0
written_2/travel_guides/berlitz1/HistoryLasVegas.txt:0
written_2/travel_guides/berlitz1/HistoryMadeira.txt:0
written_2/travel_guides/berlitz1/HistoryMadrid.txt:0
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:0
written_2/travel_guides/berlitz1/HistoryMallorca.txt:0
written_2/travel_guides/berlitz1/IntroDublin.txt:0
written_2/travel_guides/berlitz1/IntroEdinburgh.txt:0
written_2/travel_guides/berlitz1/IntroEgypt.txt:0
written_2/travel_guides/berlitz1/IntroFrance.txt:0
written_2/travel_guides/berlitz1/IntroFWI.txt:0
written_2/travel_guides/berlitz1/IntroGreek.txt:0
written_2/travel_guides/berlitz1/IntroHongKong.txt:0
written_2/travel_guides/berlitz1/IntroIbiza.txt:0
written_2/travel_guides/berlitz1/IntroIndia.txt:0
written_2/travel_guides/berlitz1/IntroIsrael.txt:0
written_2/travel_guides/berlitz1/IntroIstanbul.txt:0
written_2/travel_guides/berlitz1/IntroItaly.txt:0
written_2/travel_guides/berlitz1/IntroJamaica.txt:0
written_2/travel_guides/berlitz1/IntroJapan.txt:0
written_2/travel_guides/berlitz1/IntroJerusalem.txt:0
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:0
written_2/travel_guides/berlitz1/IntroLasVegas.txt:0
written_2/travel_guides/berlitz1/IntroLosAngeles.txt:0
written_2/travel_guides/berlitz1/IntroMadeira.txt:0
written_2/travel_guides/berlitz1/IntroMadrid.txt:0
written_2/travel_guides/berlitz1/IntroMalaysia.txt:0
written_2/travel_guides/berlitz1/IntroMallorca.txt:0
written_2/travel_guides/berlitz1/JungleMalaysia.txt:0
written_2/travel_guides/berlitz1/WhatToDublin.txt:0
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt:0
written_2/travel_guides/berlitz1/WhatToEgypt.txt:0
written_2/travel_guides/berlitz1/WhatToFrance.txt:0
written_2/travel_guides/berlitz1/WhatToFWI.txt:0
written_2/travel_guides/berlitz1/WhatToGreek.txt:0
written_2/travel_guides/berlitz1/WhatToHawaii.txt:0
written_2/travel_guides/berlitz1/WhatToHongKong.txt:0
written_2/travel_guides/berlitz1/WhatToIbiza.txt:1
written_2/travel_guides/berlitz1/WhatToIndia.txt:0
written_2/travel_guides/berlitz1/WhatToIsrael.txt:0
written_2/travel_guides/berlitz1/WhatToIstanbul.txt:0
written_2/travel_guides/berlitz1/WhatToItaly.txt:0
written_2/travel_guides/berlitz1/WhatToJamaica.txt:0
written_2/travel_guides/berlitz1/WhatToJapan.txt:0
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:1
written_2/travel_guides/berlitz1/WhatToLasVegas.txt:1
written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:0
written_2/travel_guides/berlitz1/WhatToMadeira.txt:0
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:0
written_2/travel_guides/berlitz1/WhatToMallorca.txt:0
written_2/travel_guides/berlitz1/WhereToDublin.txt:0
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:0
written_2/travel_guides/berlitz1/WhereToEgypt.txt:0
written_2/travel_guides/berlitz1/WhereToFrance.txt:1
written_2/travel_guides/berlitz1/WhereToFWI.txt:0
written_2/travel_guides/berlitz1/WhereToGreek.txt:0
written_2/travel_guides/berlitz1/WhereToHawaii.txt:0
written_2/travel_guides/berlitz1/WhereToHongKong.txt:0
written_2/travel_guides/berlitz1/WhereToIbiza.txt:0
written_2/travel_guides/berlitz1/WhereToIndia.txt:0
written_2/travel_guides/berlitz1/WhereToIsrael.txt:0
written_2/travel_guides/berlitz1/WhereToIstanbul.txt:0
written_2/travel_guides/berlitz1/WhereToItaly.txt:1
written_2/travel_guides/berlitz1/WhereToJapan.txt:0
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:0
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:0
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:11
written_2/travel_guides/berlitz1/WhereToMadeira.txt:0
written_2/travel_guides/berlitz1/WhereToMadrid.txt:0
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:0
written_2/travel_guides/berlitz1/WhereToMallorca.txt:0
written_2/travel_guides/berlitz2/Algarve-History.txt:0
written_2/travel_guides/berlitz2/Algarve-Intro.txt:0
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Amsterdam-History.txt:0
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt:0
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Athens-History.txt:0
written_2/travel_guides/berlitz2/Athens-Intro.txt:0
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bahamas-History.txt:0
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bali-History.txt:0
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Barcelona-History.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Beijing-History.txt:0
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Berlin-History.txt:0
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bermuda-history.txt:0
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Budapest-History.txt:0
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt:0
written_2/travel_guides/berlitz2/California-History.txt:0
written_2/travel_guides/berlitz2/California-WhatToDo.txt:0
written_2/travel_guides/berlitz2/California-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Canada-History.txt:0
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-History.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Cancun-History.txt:0
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt:0
written_2/travel_guides/berlitz2/China-History.txt:0
written_2/travel_guides/berlitz2/China-WhatToDo.txt:0
written_2/travel_guides/berlitz2/China-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Costa-History.txt:0
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt:1
written_2/travel_guides/berlitz2/CostaBlanca-History.txt:0
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Crete-History.txt:0
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt:0
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:1
written_2/travel_guides/berlitz2/Cuba-History.txt:0
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt:1
written_2/travel_guides/berlitz2/Nepal-History.txt:0
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:0
written_2/travel_guides/berlitz2/NewOrleans-History.txt:0
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Poland-History.txt:0
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Portugal-History.txt:0
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:0
written_2/travel_guides/berlitz2/PuertoRico-History.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Vallarta-History.txt:0
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:0
```

### Example 2

Command:
```
grep -c "hotels" -r written_2
```
This command will recursively search through the `written_2` directory and all of its subdirectories to look for files that has the text "hotels", and how many times this text shows up in the file. As shown in the output, there are actually quite a few files that contains the word "hotels", and it seems that if you want to look for a hotel at a certain place, places like Vallarta, Italy, and the Bahamas would be a good choice to find good hotels since the keyword "hotel" pops up more than 10 times in the where to go files.

Output:
```
written_2/non-fiction/OUP/Abernathy/ch1.txt:0
written_2/non-fiction/OUP/Abernathy/ch14.txt:0
written_2/non-fiction/OUP/Abernathy/ch15.txt:0
written_2/non-fiction/OUP/Abernathy/ch2.txt:0
written_2/non-fiction/OUP/Abernathy/ch3.txt:0
written_2/non-fiction/OUP/Abernathy/ch6.txt:0
written_2/non-fiction/OUP/Abernathy/ch7.txt:0
written_2/non-fiction/OUP/Abernathy/ch8.txt:0
written_2/non-fiction/OUP/Abernathy/ch9.txt:0
written_2/non-fiction/OUP/Berk/ch1.txt:0
written_2/non-fiction/OUP/Berk/ch2.txt:0
written_2/non-fiction/OUP/Berk/CH4.txt:0
written_2/non-fiction/OUP/Berk/ch7.txt:0
written_2/non-fiction/OUP/Castro/chA.txt:0
written_2/non-fiction/OUP/Castro/chB.txt:0
written_2/non-fiction/OUP/Castro/chC.txt:0
written_2/non-fiction/OUP/Castro/chL.txt:0
written_2/non-fiction/OUP/Castro/chM.txt:0
written_2/non-fiction/OUP/Castro/chN.txt:0
written_2/non-fiction/OUP/Castro/chO.txt:0
written_2/non-fiction/OUP/Castro/chP.txt:0
written_2/non-fiction/OUP/Castro/chQ.txt:0
written_2/non-fiction/OUP/Castro/chR.txt:0
written_2/non-fiction/OUP/Castro/chV.txt:0
written_2/non-fiction/OUP/Castro/chW.txt:0
written_2/non-fiction/OUP/Castro/chY.txt:0
written_2/non-fiction/OUP/Castro/chZ.txt:0
written_2/non-fiction/OUP/Fletcher/ch1.txt:0
written_2/non-fiction/OUP/Fletcher/ch10.txt:0
written_2/non-fiction/OUP/Fletcher/ch2.txt:0
written_2/non-fiction/OUP/Fletcher/ch5.txt:0
written_2/non-fiction/OUP/Fletcher/ch6.txt:1
written_2/non-fiction/OUP/Fletcher/ch9.txt:0
written_2/non-fiction/OUP/Kauffman/ch1.txt:0
written_2/non-fiction/OUP/Kauffman/ch10.txt:0
written_2/non-fiction/OUP/Kauffman/ch3.txt:0
written_2/non-fiction/OUP/Kauffman/ch4.txt:0
written_2/non-fiction/OUP/Kauffman/ch5.txt:0
written_2/non-fiction/OUP/Kauffman/ch6.txt:0
written_2/non-fiction/OUP/Kauffman/ch7.txt:0
written_2/non-fiction/OUP/Kauffman/ch8.txt:0
written_2/non-fiction/OUP/Kauffman/ch9.txt:0
written_2/non-fiction/OUP/Rybczynski/ch1.txt:0
written_2/non-fiction/OUP/Rybczynski/ch2.txt:1
written_2/non-fiction/OUP/Rybczynski/ch3.txt:0
written_2/travel_guides/berlitz1/HandRHawaii.txt:6
written_2/travel_guides/berlitz1/HandRHongKong.txt:3
written_2/travel_guides/berlitz1/HandRIbiza.txt:0
written_2/travel_guides/berlitz1/HandRIsrael.txt:0
written_2/travel_guides/berlitz1/HandRIstanbul.txt:1
written_2/travel_guides/berlitz1/HandRJamaica.txt:1
written_2/travel_guides/berlitz1/HandRJerusalem.txt:4
written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:1
written_2/travel_guides/berlitz1/HandRLasVegas.txt:4
written_2/travel_guides/berlitz1/HandRLisbon.txt:2
written_2/travel_guides/berlitz1/HandRLosAngeles.txt:5
written_2/travel_guides/berlitz1/HandRMadeira.txt:6
written_2/travel_guides/berlitz1/HandRMadrid.txt:5
written_2/travel_guides/berlitz1/HandRMallorca.txt:5
written_2/travel_guides/berlitz1/HistoryDublin.txt:0
written_2/travel_guides/berlitz1/HistoryEdinburgh.txt:0
written_2/travel_guides/berlitz1/HistoryEgypt.txt:0
written_2/travel_guides/berlitz1/HistoryFrance.txt:0
written_2/travel_guides/berlitz1/HistoryFWI.txt:0
written_2/travel_guides/berlitz1/HistoryGreek.txt:0
written_2/travel_guides/berlitz1/HistoryHawaii.txt:1
written_2/travel_guides/berlitz1/HistoryHongKong.txt:0
written_2/travel_guides/berlitz1/HistoryIbiza.txt:0
written_2/travel_guides/berlitz1/HistoryIndia.txt:0
written_2/travel_guides/berlitz1/HistoryIsrael.txt:0
written_2/travel_guides/berlitz1/HistoryIstanbul.txt:0
written_2/travel_guides/berlitz1/HistoryItaly.txt:0
written_2/travel_guides/berlitz1/HistoryJamaica.txt:0
written_2/travel_guides/berlitz1/HistoryJapan.txt:0
written_2/travel_guides/berlitz1/HistoryJerusalem.txt:0
written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt:0
written_2/travel_guides/berlitz1/HistoryLasVegas.txt:2
written_2/travel_guides/berlitz1/HistoryMadeira.txt:0
written_2/travel_guides/berlitz1/HistoryMadrid.txt:0
written_2/travel_guides/berlitz1/HistoryMalaysia.txt:0
written_2/travel_guides/berlitz1/HistoryMallorca.txt:0
written_2/travel_guides/berlitz1/IntroDublin.txt:1
written_2/travel_guides/berlitz1/IntroEdinburgh.txt:0
written_2/travel_guides/berlitz1/IntroEgypt.txt:1
written_2/travel_guides/berlitz1/IntroFrance.txt:0
written_2/travel_guides/berlitz1/IntroFWI.txt:0
written_2/travel_guides/berlitz1/IntroGreek.txt:0
written_2/travel_guides/berlitz1/IntroHongKong.txt:3
written_2/travel_guides/berlitz1/IntroIbiza.txt:1
written_2/travel_guides/berlitz1/IntroIndia.txt:0
written_2/travel_guides/berlitz1/IntroIsrael.txt:1
written_2/travel_guides/berlitz1/IntroIstanbul.txt:2
written_2/travel_guides/berlitz1/IntroItaly.txt:0
written_2/travel_guides/berlitz1/IntroJamaica.txt:3
written_2/travel_guides/berlitz1/IntroJapan.txt:0
written_2/travel_guides/berlitz1/IntroJerusalem.txt:0
written_2/travel_guides/berlitz1/IntroLakeDistrict.txt:0
written_2/travel_guides/berlitz1/IntroLasVegas.txt:0
written_2/travel_guides/berlitz1/IntroLosAngeles.txt:0
written_2/travel_guides/berlitz1/IntroMadeira.txt:4
written_2/travel_guides/berlitz1/IntroMadrid.txt:0
written_2/travel_guides/berlitz1/IntroMalaysia.txt:0
written_2/travel_guides/berlitz1/IntroMallorca.txt:4
written_2/travel_guides/berlitz1/JungleMalaysia.txt:0
written_2/travel_guides/berlitz1/WhatToDublin.txt:0
written_2/travel_guides/berlitz1/WhatToEdinburgh.txt:0
written_2/travel_guides/berlitz1/WhatToEgypt.txt:7
written_2/travel_guides/berlitz1/WhatToFrance.txt:0
written_2/travel_guides/berlitz1/WhatToFWI.txt:13
written_2/travel_guides/berlitz1/WhatToGreek.txt:0
written_2/travel_guides/berlitz1/WhatToHawaii.txt:1
written_2/travel_guides/berlitz1/WhatToHongKong.txt:2
written_2/travel_guides/berlitz1/WhatToIbiza.txt:6
written_2/travel_guides/berlitz1/WhatToIndia.txt:5
written_2/travel_guides/berlitz1/WhatToIsrael.txt:3
written_2/travel_guides/berlitz1/WhatToIstanbul.txt:1
written_2/travel_guides/berlitz1/WhatToItaly.txt:1
written_2/travel_guides/berlitz1/WhatToJamaica.txt:8
written_2/travel_guides/berlitz1/WhatToJapan.txt:0
written_2/travel_guides/berlitz1/WhatToLakeDistrict.txt:2
written_2/travel_guides/berlitz1/WhatToLasVegas.txt:0
written_2/travel_guides/berlitz1/WhatToLosAngeles.txt:0
written_2/travel_guides/berlitz1/WhatToMadeira.txt:6
written_2/travel_guides/berlitz1/WhatToMalaysia.txt:4
written_2/travel_guides/berlitz1/WhatToMallorca.txt:3
written_2/travel_guides/berlitz1/WhereToDublin.txt:1
written_2/travel_guides/berlitz1/WhereToEdinburgh.txt:0
written_2/travel_guides/berlitz1/WhereToEgypt.txt:6
written_2/travel_guides/berlitz1/WhereToFrance.txt:9
written_2/travel_guides/berlitz1/WhereToFWI.txt:8
written_2/travel_guides/berlitz1/WhereToGreek.txt:8
written_2/travel_guides/berlitz1/WhereToHawaii.txt:0
written_2/travel_guides/berlitz1/WhereToHongKong.txt:6
written_2/travel_guides/berlitz1/WhereToIbiza.txt:4
written_2/travel_guides/berlitz1/WhereToIndia.txt:7
written_2/travel_guides/berlitz1/WhereToIsrael.txt:8
written_2/travel_guides/berlitz1/WhereToIstanbul.txt:4
written_2/travel_guides/berlitz1/WhereToItaly.txt:15
written_2/travel_guides/berlitz1/WhereToJapan.txt:4
written_2/travel_guides/berlitz1/WhereToJerusalem.txt:2
written_2/travel_guides/berlitz1/WhereToLakeDistrict.txt:3
written_2/travel_guides/berlitz1/WhereToLosAngeles.txt:7
written_2/travel_guides/berlitz1/WhereToMadeira.txt:8
written_2/travel_guides/berlitz1/WhereToMadrid.txt:1
written_2/travel_guides/berlitz1/WhereToMalaysia.txt:15
written_2/travel_guides/berlitz1/WhereToMallorca.txt:13
written_2/travel_guides/berlitz2/Algarve-History.txt:0
written_2/travel_guides/berlitz2/Algarve-Intro.txt:2
written_2/travel_guides/berlitz2/Algarve-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Algarve-WhereToGo.txt:5
written_2/travel_guides/berlitz2/Amsterdam-History.txt:0
written_2/travel_guides/berlitz2/Amsterdam-Intro.txt:0
written_2/travel_guides/berlitz2/Amsterdam-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Amsterdam-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Athens-History.txt:0
written_2/travel_guides/berlitz2/Athens-Intro.txt:0
written_2/travel_guides/berlitz2/Athens-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Athens-WhereToGo.txt:0
written_2/travel_guides/berlitz2/Bahamas-History.txt:2
written_2/travel_guides/berlitz2/Bahamas-Intro.txt:1
written_2/travel_guides/berlitz2/Bahamas-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Bahamas-WhereToGo.txt:14
written_2/travel_guides/berlitz2/Bali-History.txt:1
written_2/travel_guides/berlitz2/Bali-WhatToDo.txt:5
written_2/travel_guides/berlitz2/Bali-WhereToGo.txt:17
written_2/travel_guides/berlitz2/Barcelona-History.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Barcelona-WhereToGo.txt:3
written_2/travel_guides/berlitz2/Beijing-History.txt:1
written_2/travel_guides/berlitz2/Beijing-WhatToDo.txt:7
written_2/travel_guides/berlitz2/Beijing-WhereToGo.txt:2
written_2/travel_guides/berlitz2/Berlin-History.txt:2
written_2/travel_guides/berlitz2/Berlin-WhatToDo.txt:0
written_2/travel_guides/berlitz2/Berlin-WhereToGo.txt:1
written_2/travel_guides/berlitz2/Bermuda-history.txt:3
written_2/travel_guides/berlitz2/Bermuda-WhatToDo.txt:4
written_2/travel_guides/berlitz2/Bermuda-WhereToGo.txt:2
written_2/travel_guides/berlitz2/Boston-WhereToGo.txt:2
written_2/travel_guides/berlitz2/Budapest-History.txt:0
written_2/travel_guides/berlitz2/Budapest-WhatToDo.txt:2
written_2/travel_guides/berlitz2/Budapest-WhereoGo.txt:3
written_2/travel_guides/berlitz2/California-History.txt:0
written_2/travel_guides/berlitz2/California-WhatToDo.txt:3
written_2/travel_guides/berlitz2/California-WhereToGo.txt:5
written_2/travel_guides/berlitz2/Canada-History.txt:1
written_2/travel_guides/berlitz2/Canada-WhereToGo.txt:6
written_2/travel_guides/berlitz2/CanaryIslands-History.txt:0
written_2/travel_guides/berlitz2/CanaryIslands-WhatToDo.txt:3
written_2/travel_guides/berlitz2/CanaryIslands-WhereToGo.txt:5
written_2/travel_guides/berlitz2/Cancun-History.txt:0
written_2/travel_guides/berlitz2/Cancun-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Cancun-WhereToGo.txt:10
written_2/travel_guides/berlitz2/China-History.txt:0
written_2/travel_guides/berlitz2/China-WhatToDo.txt:1
written_2/travel_guides/berlitz2/China-WhereToGo.txt:2
written_2/travel_guides/berlitz2/Costa-History.txt:0
written_2/travel_guides/berlitz2/Costa-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Costa-WhereToGo.txt:5
written_2/travel_guides/berlitz2/CostaBlanca-History.txt:0
written_2/travel_guides/berlitz2/CostaBlanca-WhatToDo.txt:4
written_2/travel_guides/berlitz2/Crete-History.txt:0
written_2/travel_guides/berlitz2/Crete-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Crete-WhereToGo.txt:5
written_2/travel_guides/berlitz2/CstaBlanca-WhereToGo.txt:4
written_2/travel_guides/berlitz2/Cuba-History.txt:0
written_2/travel_guides/berlitz2/Cuba-WhatToDo.txt:4
written_2/travel_guides/berlitz2/Cuba-WhereToGo.txt:15
written_2/travel_guides/berlitz2/Nepal-History.txt:1
written_2/travel_guides/berlitz2/Nepal-WhatToDo.txt:4
written_2/travel_guides/berlitz2/Nepal-WhereToGo.txt:8
written_2/travel_guides/berlitz2/NewOrleans-History.txt:0
written_2/travel_guides/berlitz2/Paris-WhatToDo.txt:1
written_2/travel_guides/berlitz2/Paris-WhereToGo.txt:3
written_2/travel_guides/berlitz2/Poland-History.txt:0
written_2/travel_guides/berlitz2/Poland-WhatToDo.txt:3
written_2/travel_guides/berlitz2/Portugal-History.txt:0
written_2/travel_guides/berlitz2/Portugal-WhatToDo.txt:5
written_2/travel_guides/berlitz2/Portugal-WhereToGo.txt:6
written_2/travel_guides/berlitz2/PuertoRico-History.txt:0
written_2/travel_guides/berlitz2/PuertoRico-WhatToDo.txt:6
written_2/travel_guides/berlitz2/PuertoRico-WhereToGo.txt:5
written_2/travel_guides/berlitz2/Vallarta-History.txt:2
written_2/travel_guides/berlitz2/Vallarta-WhatToDo.txt:5
written_2/travel_guides/berlitz2/Vallarta-WhereToGo.txt:21
```


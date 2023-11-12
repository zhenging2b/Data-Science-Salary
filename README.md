# Dota Analysis
Dota 2 is a popular 5v5 multiplayer online battle arena (MOBA) game. Two teams are pitted against one another to try and kill each others' ancients. The motivation of this project is to share some insight as to what determines the winner in a game. <br>

One of the hypothesis to be tested is whether early game advantages matter in determining who wins the game. Personally, I try to keep a level head even when my team loses the early game as I believe that early game does not necessarily dictate the outcome, and have always been irritated at players who give up easily. Hence, the project is to use data to support my hypothesis. 

This project involves gathering, cleaning and analysing Dota 2 matches using OpenDota Api. The doccumentation of OpenDota API can be found here: https://docs.opendota.com/#section/Introduction <br>
A brief explanation of each file will be written here.

## Getting Dota Info P1.ipynb
This file includes how IDs of Dota 2 pro matches are taken. This file also includes getting heroes ID, and how to get and clean information from 1 match. The list of match, hero id are then saved in **match_ids** and **hero_id.json** respectively <br>

There are also several functions written to gete specific information from each match, and this methods would be used in **Cleaning Dota Info p2.pynb**

## Cleaning Dota Info p2.pynb
This file includes how match info are taken from **match_ids** and cleaned to form **dota.csv**, the matches and corresponding cleaned csv file to be used for analysis. 

## Analysis of dota 2.pynb
This file shows the analysis of the cleaned **dota.csv** file, this includes EDA and different models tested to see which performs the best. Conclusion is written here as well. We see that in the 2 best performing models, Logistic Regression with L1 and AdaBoost, having an early advantage is not top 8 of most important variables. This means that having a bad start would not automatically result in a lost. Players should still focus on other more important objectives such as last hits, roshan, runes, purchasing consumables. Similarly, a team that has the advantage early cannot get complacent, for they may have won the battle, but can still lose the war.
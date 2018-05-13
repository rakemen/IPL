# IPL
IPL playoff simulator

The repository has 3 files:

1. ipl.py - This is a python based playoff probability simulator. Tested with python 2.7 on windows 64 bit computer
2. ipl.xlsm - This is an excel based macro which does the same as the python script.
3. deltas.xls - This excel needs to be manually populated and shows the jump/drop in probability before and after a game

Difference between the python and excel version:

- The python version is scalable and can be run when a lot of games are left in the tournament. 
- I have tested the python version when 24 games were left which results in about 16 million combinations. Excel cannot handle this.
- Excel is more suited when the number of games left is 14 or less, ie, 8K+ combinations.
- Why excel then?
  - I wrote the excel macro 4 years ago when I didn't know python
  - The excel can allow you to filter the probabilities and actually look at the sequence of combinations
  
 

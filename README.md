# IPL
IPL playoff simulator

This is a python based playoff probability simulator. Tested with python 3.8.5 on windows 10 64-bit OS.

Overview of algorithm:

Assuming no ties/washout/no result, each game has two possible outcomes. 
If n games remain in the tournament, there are a total of 2^n possible scenarios.
For each of these scenarios, compute how the final points table will look and from that, one can figure out which teams make it to top 2 spots and which teams makes it to top 4. In the event of multiple teams finishing with same points, NRR comes into play. 
From this final picture, it can be determined if a team makes it to top 2 confirmed on points alone, top 2 competing on NRR, top 4 confirmed spot and top 4 competing on NRR. 
Given the 2^n scenarios, if a team makes it to top 2 confirmed spot in say x scenarios, x/(2^n) is the probability of that team making it to top 2 confirmed spot.

How do i simulate the 2^n scenarios?
- run a loop from 0 to 2^n-1
- convert the number to a binary string
- if a digit is 0, assume team-1 won that game and if the digit is 1, assume team-2 won and allocate points accordingly

The script takes about ~15 minutes to estimate outcomes for 24 games (16.7 million scenarios). Can it be made more efficient? Definitely yes! I will post an algorithm shared by another reddit user which is more compact and uses recursion, but might be slightly complicated to understand/debug for someone who is not very familiar with recursions.

I prefer the current algorithm as I have tested it for accuracy and its easier to understand and debug for beginner level programmers. Also, the time taken to run the script reduces by 50% with every passing game.









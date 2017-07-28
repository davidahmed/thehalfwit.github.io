---
layout: default
---
{% include subpage-nav.html %}
{% include mathjax.html %}
## Ranking teams with winning percentage
We've previously ranked teams based on number of wins and losses. Clearly, such models loose the chance to include the scores of winning and loosing the team.
## Ranking teams with a model of strenght of schedule integrated (Massey Method)
Consider a match where A beats B by 1, B beats C by 15. Can we say A will beat C by 16 (thinking that scores will hold transitivity), but that's too much far from the truth. What happens if C beats A by 10. how do we rank the teams now?
````octave
% Form a system for the scores of the above game.
% x, y and z are the rankings of A, B and C respectively.
M = [1 -1 0;
     0 1 -1;
     -1 0 1]
scores = [1 15 10];

% This system doesn't have a solution, therefore we rely on least-squares.
% It is recommended to replace the last row of M with 1s and scores with 0....
% This adds the constraint that the scores sum to zero.
````

But we can actually find the actual system directly.
````octave
% 1. The diagonal cells contain the number of games played by the corresponding team.
% 2. The off-diagonal elements contain -1 times the number of games played.
% 3. Replace the last rows with 1s.
% 4. Scores vector can be computed directly as number of scores won-lost.
````
## Integrate weights into ranking for personalized rankings
An adaptation of the Massey method. How do we implelement that fact that recency matters in a game? In other words, how to weight games more light based on how early they were played. The change is simple- number of games (and also the scores) become the weighted number of games. How can we weight games based on other features?

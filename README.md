# Edit-Distance
Algorithm to create Edit Distance matrix and Direction Matrix.

Edit distance matrix and Direction matrix are filled using dynamic programming.

Edit Distance matrix represent edit distance between substrings $incorrect(0,i)$ and $correct(0,j)$

Edit Distance Matrix : $ D[i][j] = min(D(i-1,j)+1,D(i,j-1)+1,D(i-1,j-1)+cost) $ where

if incorrect[i]=correcr[j] then $ cost = 0 $

else $ cost = ConfusionMatrix[incorrect[i]][correct[j]] $

Direction Matrix : Direction[i][j] contains tuple (row,column) for which minimum of D[i][j] was found

Direction matrix will later be used to backtrace the path to convert incorrect word to correct word

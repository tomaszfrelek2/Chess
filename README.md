# Chess
I made Chess!
<hr>
Chess.ipynb is the notebook version of the game, chessGame is the plain-text version
<hr>
# FAQ
<p></p>
Q: Why did I make this?
<p>
A: I was bored over the summer and wanted to do something with my time
</p>
Q: Why are there no graphics
?<p>
A: There are a million versions of chess with graphics, I thought I'd make something semi-unique by using ascii based graphics. 
</p>
also I don't know Unity
<p></p>
Q: How does the A.I. work?
<p>
A: As far as chess ai's go, it's no AlphaZero. My ai brute-forces every single possible move and counter move, and decides on the best move from there. This effectivly means that the ai can see 1 turn into the future, so it can be outplayed by even a novice player (it did however, give my 6-year-old brother a run for his money). The ai determines the "best" move by calculating the material and positional advantage that each move generates.
</p>
Q: What do you mean by material and positional advantage?
<p>
A: The ai calculates the material advantage generated by moves, i.e. capturing/trading pieces. For example, trading a rook for a queen would be a positive material gain(and therefore be encouraged), while trading a knight for a pawn would be negative(and therefore be discouraged). The ai also considers the positional advantage generated by every move. For example, a knight in the center of the board has a better position than a knight on the edge of the board; likewise, a king safely castled has a better position than a king open in the center of the board. The positional advantage is calculated by referencing a series of heatmaps that determine which squares are good for each piece and which are bad.
</p>
Q: Why don't you just make the ai better by making it see more moves into the future?
<p>
A: An excellent question! First, a little backstory. When originaly planning to make this game, I didn't intend to make an ai. This led me to choosing to make the game in Python, as using it would allow me to take advantage of many of its in-built functionalities to make my life easier while coding the game. Unfortunetly, by the time I had decided to add an ai, I was in too deep, and was stuck with using Python. This was bad for ai purposes as Python is relativly slow compared to other languages. The amount of moves needed to be analyzed increases exponentially with every additional turn; while looking one move into the future takes 3-4 seconds, looking 2 moves takes about a 60-70 seconds(I timed it), looking three moves ahead takes about 5 minutes. So while I <i>could</i> have the ai look 3 moves ahead, I didn't think it would be very fun to play against a computer that takes 5 minutes to play even the most obvious moves. If I were to redo the whole project from scratch, I definetly would have used Java or C++ in order to make a better ai.
</p>
Q: If the ai is just slow, why didn't you optimise your code better?
<p>
A: Another excellent question! The simple answer, is that I did-- at one point anyway. Once I realized that my ai was slow, I implemented an optimization process called alpha-beta pruning. This actually worked, but not as well as I had hoped. At a depth of 4(i.e. two turns ahead), it about halved the time to move, from ~60-70 seconds to about 30 seconds. Since I felt that 30 seconds per move was still too slow for a computer, I decided to limit the ai to looking only one move ahead. Additionally, since alpha-beta pruning doesn't work at a depth of 2 (i.e. looking on e turn ahead), I decided to cut out the alpha-beta pruning algorithm from my code. However, as proof that I'm not talking out of my ass, I added the alpha-beta pruning algorithm in the "alpha-beta pruning algorithm" file.
</p>


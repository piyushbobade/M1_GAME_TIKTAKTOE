Report document
# **Two Player Tic-Tac-Toe Game in C:-**

# **Introduction:**
 Tic-tac-toe is a popular number game.Tic-tac-toe or Noughts and crosses, Xs and Os) is a pencil-and-paper game for two players, X and O, who take turns marking the spaces in a 3×3 grid. The player who succeeds in placing three respective marks in a horizontal, vertical, or diagonal row wins the game. Players soon discover that best play from both parties leads to a draw , Tic-tac-toe is most often played by young children.

Research:

improve hand eye coordination and incourage better social interaction by better collaborative play

Requirements:

This requires the knowledge of c programming and basic idea to solve Tic-tac-toe would be helpful.

Cost and features:

Cost – cost is not required to play this game.

Feature-1. Keyboard functions will be added. 2. We want to design more complex boards for the game in future.

Swot Analysis:

Swot analysis is a strategic planning and strategic management use to help a person and organiasation identify strengths,weaknesses,apportunities and threaths.

Strengths:

1.Good packaging and advertising

2.Good taste

Weaknesses:

1.Too sweet

2.Not too many flavors

Opportunities:

1.Introduce newer flavors

2.Tap growing markets

Threats:

1.Threat from local candies

2.Threat from chocolates

4W and 1H:

4W-WHO,WHAT,WHEN,WHERE

WHO-This game can be played by anyone.

WHAT-TIC-TAC-TOE is a brain teaser game and it is very popular.

WHEN-it is in a progress to build as a part of ltts.

WHERE-it is made on vs code on windows 10

1H:how

`it is build like it will taking inputs from user and give a solution algorithm by taking inputs form the users and give the solution for the same.

HIGH LEVEL AND LOW LEVEL REQUIREMENTS:

Contains samples and take inputs from the users

Print output if solution exists.

**The main source code file :**

-tictactoeC.c

**Executable file for the project:**

-tictactoeC.exe

**About The Game**

- This is a two player tic tac toe game ( meaning both the players are human ).
- The first player to place 3 of their mark forming a straight line wins.

[![](RackMultipart20211124-4-14b8w3s_html_b84bd19d80c6cf9e.png)](https://github.com/rajkishlay/cprogramming/blob/main/TicTacToe%20.PNG)

**Usage**

Alternates between Player1 and Player2. Enter a digit [1-9] to move:

1 | 2 | 3

---------

4 | 5 | 6

---------

7 | 8 | 9

The game ends if:

- A player completes three in a row; that player wins
- All squares are taken; neither player wins
- A player makes an illegal move; their opponent wins

![](RackMultipart20211124-4-14b8w3s_html_46f7abe62c55fb41.png)

![Shape1](RackMultipart20211124-4-14b8w3s_html_e52d4a555a018f86.gif)

Code

| #include \&lt;stdio.h\&gt; |
 |
| --- | --- |
|
 | #include \&lt;conio.h\&gt; |
|
 |

 |
|
 | char square[10] = { &#39;o&#39;, &#39;1&#39;, &#39;2&#39;, &#39;3&#39;, &#39;4&#39;, &#39;5&#39;, &#39;6&#39;, &#39;7&#39;, &#39;8&#39;, &#39;9&#39; }; |
|
 |

 |
|
 | int checkwin(); |
|
 | void board(); |
|
 |

 |
|
 | int main() |
|
 | { |
|
 | int player = 1, i, choice; |
|
 |

 |
|
 | char mark; |
|
 | do |
|
 | { |
|
 | board(); |
|
 | player = (player % 2) ? 1 : 2; |
|
 |

 |
|
 | printf(&quot; Player %d, enter a number: &quot;, player); |
|
 | scanf(&quot;%d&quot;, &amp;choice); |
|
 |

 |
|
 | mark = (player == 1) ? &#39;X&#39; : &#39;O&#39;; |
|
 |

 |
|
 | if (choice == 1 &amp;&amp; square[1] == &#39;1&#39;) |
|
 | square[1] = mark; |
|
 |

 |
|
 | else if (choice == 2 &amp;&amp; square[2] == &#39;2&#39;) |
|
 | square[2] = mark; |
|
 |

 |
|
 | else if (choice == 3 &amp;&amp; square[3] == &#39;3&#39;) |
|
 | square[3] = mark; |
|
 |

 |
|
 | else if (choice == 4 &amp;&amp; square[4] == &#39;4&#39;) |
|
 | square[4] = mark; |
|
 |

 |
|
 | else if (choice == 5 &amp;&amp; square[5] == &#39;5&#39;) |
|
 | square[5] = mark; |
|
 |

 |
|
 | else if (choice == 6 &amp;&amp; square[6] == &#39;6&#39;) |
|
 | square[6] = mark; |
|
 |

 |
|
 | else if (choice == 7 &amp;&amp; square[7] == &#39;7&#39;) |
|
 | square[7] = mark; |
|
 |

 |
|
 | else if (choice == 8 &amp;&amp; square[8] == &#39;8&#39;) |
|
 | square[8] = mark; |
|
 |

 |
|
 | else if (choice == 9 &amp;&amp; square[9] == &#39;9&#39;) |
|
 | square[9] = mark; |
|
 |

 |
|
 | else |
|
 | { |
|
 | printf(&quot; Invalid move &quot;); |
|
 |

 |
|
 | player--; |
|
 | getch(); |
|
 | } |
|
 | i = checkwin(); |
|
 |

 |
|
 | player++; |
|
 | }while (i == - 1); |
|
 |

 |
|
 | board(); |
|
 |

 |
|
 | if (i == 1) |
|
 | printf(&quot; ==\&gt;\aPlayer %d win &quot;, --player); |
|
 | else |
|
 | printf(&quot; ==\&gt;\aGame draw&quot;); |
|
 |

 |
|
 | getch(); |
|
 |

 |
|
 | return 0; |
|
 | } |
|
 |

 |
|
 | int checkwin() |
|
 | { |
|
 | if (square[1] == square[2] &amp;&amp; square[2] == square[3]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[4] == square[5] &amp;&amp; square[5] == square[6]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[7] == square[8] &amp;&amp; square[8] == square[9]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[1] == square[4] &amp;&amp; square[4] == square[7]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[2] == square[5] &amp;&amp; square[5] == square[8]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[3] == square[6] &amp;&amp; square[6] == square[9]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[1] == square[5] &amp;&amp; square[5] == square[9]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[3] == square[5] &amp;&amp; square[5] == square[7]) |
|
 | return 1; |
|
 |

 |
|
 | else if (square[1] != &#39;1&#39; &amp;&amp; square[2] != &#39;2&#39; &amp;&amp; square[3] != &#39;3&#39; &amp;&amp; |
|
 | square[4] != &#39;4&#39; &amp;&amp; square[5] != &#39;5&#39; &amp;&amp; square[6] != &#39;6&#39; &amp;&amp; square[7] |
|
 | != &#39;7&#39; &amp;&amp; square[8] != &#39;8&#39; &amp;&amp; square[9] != &#39;9&#39;) |
|
 |

 |
|
 | return 0; |
|
 | else |
|
 | return - 1; |
|
 | } |
|
 |

 |
|
 |

 |
|
 | /\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\* |
|
 | FUNCTION TO DRAW BOARD OF TIC TAC TOE WITH PLAYERS MARK |
|
 | \*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*/ |
|
 |

 |
|
 |

 |
|
 | void board() |
|
 | { |
|
 | system(&quot;cls&quot;); |
|
 | printf(&quot;\n\n \xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\n&quot;); |
|
 | printf(&quot;\t Tic Tac Toe&quot;); |
|
 | printf(&quot;\n \xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\n\n&quot;); |
|
 |

 |
|
 | printf(&quot; Player 1 (X) - Player 2 (O)\n\n&quot;); |
|
 |

 |
|
 |

 |
|
 | printf(&quot; \xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\n&quot;); |
|
 | printf(&quot;\t| | | |\n&quot;); |
|
 | printf(&quot;\t| %c | %c | %c |\n&quot;, square[1], square[2], square[3]); |
|
 |

 |
|
 | printf(&quot;\t|\_\_\_\_\_|\_\_\_\_\_|\_\_\_\_\_|\n&quot;); |
|
 | printf(&quot;\t| | | |\n&quot;); |
|
 |

 |
|
 | printf(&quot;\t| %c | %c | %c |\n&quot;, square[4], square[5], square[6]); |
|
 |

 |
|
 | printf(&quot;\t|\_\_\_\_\_|\_\_\_\_\_|\_\_\_\_\_|\n&quot;); |
|
 | printf(&quot;\t| | | |\n&quot;); |
|
 |

 |
|
 | printf(&quot;\t| %c | %c | %c |\n&quot;, square[7], square[8], square[9]); |
|
 |

 |
|
 | printf(&quot;\t| | | |\n&quot;); |
|
 | printf(&quot; \xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\xcd\n\n&quot;); |
|
 |
 |
|
 | };

High level and low level requirements:
 |

- Test Plan High Level Test Plan Test ID Description Feature Result Type of Test HT 1 Components Testing Sample Input is given Pass Requirement Based HT 2 Software Testing The inputs required is given Fail Scenario Based HT 3 System Testing The inputs of the components is given to the system Fail Boundary Based
- Low Level Test Plan Test ID Description Feature Result Type of Test LT 1 The components required for the project is tested for the further process The working of the components is taken as the input Pass Requirement Based LT 2 The software used for the sysytem is tested and if it is passed in the test it is used for the further process The inputs required is given Fail Scenario Based LT 3 Overall system is tested and then it is approved for the next process The inputs of the components is given to the system Fail Boundary Based
-

**Challenges Faced**

| **No.** | **Challenge** | **Solution** |
| --- | --- | --- |
| 1. | Output was not matching the expectation | Modified the logic of the program and code itself |
| --- | --- | --- |
| 2. | Game did not end even after player wins | Additional logic was implemented in existing function |
| 3. | Error while Building the sourcefile | Trial and Error and referred Mini Project Template |

# THANKYOU

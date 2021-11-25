# M1_GAME_TIKTAKTOE
Folder	Description
1_Requirements	Documents detailing requirements and research
2_Design	Documents specifying design details
3_Implementation	All code and documentation
4_Test_plan	Documents with test plans and procedures
5_Documentation	Documentation generated on my local machine
6_Build	Build files which was created on my local machine
7_Screenshots_and_Videos	Screenshots and videos of the working project
Contributors List and Summary
PS No.	Name	Features	Issuess Raised	Issues Resolved	No Test Cases	Test Case Pass
258260	Balkaran Singh	Whole App	7	5	6	6
Challenges Faced and How Was It Overcome
1. Unable to keep check on the input values:
This was solved by having if statements on the range of values so that it does not go out of bounds of the game grid. Moreover, I have taken the benefit of the return value of scanf to ensure that 2 values are received by the program at each time when the user enters its choice for the move.

2. Some problems in getting 'X' and 'O' on the grid
First I have used simple integers in the game grid, but then I used 'X' and 'O' on the grid by making a function to get symbols by the corresponding player integer. This function helped to treat the grid as a 2D char array.

3. Was not able to get Unity testing action working
I changed my test.c file so that each grid I'm passing to the test functions is first defined and then passed rather than just passing as a literal array. This made all my test cases pass.

4. Was not able to get C/C++ Build Status Working
This error was because of an error in the filename that i was including in my main file which was different from the real name was. There was another error that I was including .c file of operations rather than the .h header file which was supposed to be included in our program.
## Badges
[![cppcheck-action-test](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/cppcheck.yml/badge.svg)](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/cppcheck.yml)
Code Inspector-![](https://api.codiga.io/project/29841/score/svg)
![](https://api.codiga.io/project/29841/status/svg)
[![Valgrind](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/valgrind.yml/badge.svg)](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/valgrind.yml)
[![Linux C/C++ CI](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/Linux_c-cpp.yml/badge.svg)](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/Linux_c-cpp.yml)
[![C/C++ CI UnitTesting](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/unit-testing.yml/badge.svg)](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/unit-testing.yml)
[![Windows C/C++ CI](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/windows_c-cpp.yml/badge.svg)](https://github.com/piyushbobade/M1_GAME_TIKTAKTOE/actions/workflows/windows_c-cpp.yml)

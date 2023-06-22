[# Tic_tac_toe
'''
***
#include <fstream>
#include<iostream>
#include <oleidl.h>
#include <ostream>
#include <stdio.h>
#include <stdlib.h>
#include<string>
#include<Windows.h>
#include <synchapi.h>
#include<cstdlib>
#include <winuser.h>
#include<algorithm>
#include<ostream>
#include<random>//
#include<ctime>
#include<array>
#include<conio.h>
#include<vector>
using namespace std;
string name_draft;
int player_choice;
/*Rows And Collums*/
int rows;
int collums;
//////////////////////
//----------------------------//
/*Displaying board*/ 
void creator() {
 ofstream Creator("Creator_Social_Media_Links.html");
 Creator << "<html>" << endl;
 Creator << "<head><title>Creators Social Media</title></head>" << endl;
 Creator << "<body>\n";
 Creator << "<h1>Facebook: https://www.facebook.com/profile.php?id=100024820629634 </h1>\n";
 Creator << "<h2>Discord: Lewiz#3507 <h2>\n";
 Creator << "<body>Youtube Channel</title>\n";
 Creator << "<body><p>MrGhostler || https://www.youtube.com/channel/UCHhKngvY6NJxP23AZk6awrA</p></body>\n";
 Creator << "</html>\n";
 Creator.close();
 string cmd = "Start Creator_Social_Media_Links.html";
 system(cmd.c_str());
}
//////////////////////
////////game rules////

void game_rules() {
string rules[][3] = {{"1. Respect"},
                    {"2. No Provokes"},
                    {"3. No Mad"}};
cout << rules[0][0] << endl;
cout << rules[1][0] << endl;
cout << rules[2][0] << endl;
cout << "Press ESC to Return" << endl;
while (true) {
    if(_kbhit()) {
        char key = _getch();
        if (key == 27) {
            system("exit");
        }
    }
  }
} 
//////////////////////
random_device rd;
mt19937 g(rd());
mt19937 e(rd());
////////Random System////;
//////PLayers/////////
int Player_1_Scores;
int Player_2_Scores;
string Player_1;
string Player_2;
string draftplr;
string Player_Names[2] = {Player_1, Player_2};
///////////////////////Choices////////////////////////////////////
string choices[][3] = {{"1. Start"},
                      {"2. Game's Regulations"},
                      {"3. Game's Foundation And Creator"}};

////////////////////////////////////////////////////////////////////////////////
////////////////////////////Rock Paper Scissor System///////////////////////////
int ran[2] = {1, 2};
int size_of_ran = sizeof(ran)/sizeof(int);
string dots[3] = {".", "..", "..."};
////////////////////////////////////////////////////////////////////////////////////////////
////////////////////////////////////////////////////////////////////////////////////////////
void rock_paper_scissor() {
    cout << "You Will Have 2 Int Numbers Which Is 1 and 2, These Will Be Randomizely Rolled" << endl;
    Sleep(500);
    cout << "Please Press Enter Again To Start The Roll" << endl;
    if (getchar() == '\n') {
        Sleep(10000);
        cout << "Randomizing Your Number";
        for (int i = 0; i <= 3; i++) {
        Sleep(2000);
        cout << dots[i] << endl;
        }
    cout << "Roll Is Being Conducted..." << endl;
    Sleep(1000);
    }
}
//////////////////////////////////////////////////////////////////////////////////////////////////

/////////////////////////
///////TIC TAC TOE SYSTEM ////
     char board[5][5] = {{' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '},
                        {' ', ' ', ' ', ' ', ' '}};
void DisplayBoard() {
cout << "      |      |      |      |      |      " << endl;
cout << board[0][0] << "     | " << board[0][1] << "    | " <<  board[0][2] << "    | " << board[0][3] << "    | " << board[0][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "_______+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[1][0] << "     | " << board[1][1] << "    | " <<  board[1][2] << "    | " << board[1][3] << "    | " << board[1][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "_______+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[2][0] << "     | " << board[2][1] << "    | " <<  board[2][2] << "    | " << board[2][3] << "    | " << board[2][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "_______+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[3][0] << "     | " << board[3][1] << "    | " <<  board[3][2] << "    | " << board[3][3] << "    | " << board[3][4] << "    | "  << endl;
cout << "______+" << "______+" << "______+" << "______+" << "______+" << "_______+" << endl;
cout << "      |      |      |      |      |      " << endl;
cout << board[4][0] << "     | " << board[4][1] << "    | " <<  board[4][2] << "    | " << board[4][3] << "    | " << board[4][4] << "    | "  << endl;
}
    int Choosing_Boxes;
    int row, columns;
    string turn;
    bool draw = false;
/*Board System*/
void tic_tac_toe_system() {
const char E = 'O';
Sleep(3000);
cout << "This is our board, the origin is located at the first upper box on the left side " << endl;
Sleep(2000);
cout << "Type number of the collum, rows to move" << endl;
cout << "Hope you enjoy and good luck!" << endl;
cout << " " << endl;
cout << " " << endl;
cout << " " << endl;
cout << name_draft << " Gonna go first with O" << endl;
cout << " " << endl;
DisplayBoard();
cout << " " << endl;
cout << " " << endl;
cout << " " << endl;
cout << draftplr << " Gonna Go First With O" << endl;
cout << " " << endl;
cout << "Please Enter the number of the row and collum to move on" << endl;
cout << "Enter the rows and collums with interger number between 0 and 4 only!" << endl;
}
void changing_player() {
    string n;
    for (int i = 0; i <= 1; i++) {
     if (i == 0) {
        Player_Names[i] = Player_Names[i+1];
     }
     else {
        Player_Names[i] = Player_Names[i-1];
     }
    }
}
/**/
/*Returning*/
/*************************/
int main() { 
    int n = rand() %1 + 0;
    shuffle(Player_Names->begin(), Player_Names->end(), g);
    cout << "**********************************" << endl;
    cout << "X -------Tic Tac Toe 5X------- O " << endl;
    cout << "**********************************" << endl;
    Sleep(5000);
    cout << "Please Enter to Continue to the game!" << endl;
    if (getchar() == '\n') {
    cout << "Game is Loading, Please Wait A Few Seconds" << endl;
    Sleep(10000);
    cout << "Game Succesfully Loaded!(*^_^*)" << endl;
    Sleep(1000);
    cout << "Please Enter Your Name both players" << endl;
    cout << "Player_1: ";
    getline(cin, Player_1);
    Player_Names[0] = Player_1;
    cout << "Player_2: ";
    getline(cin, Player_2);
    Player_Names[1] = Player_2;
    if (Player_1 == Player_2) {
        cout << "Please don't use the same name, or you could add numbers at the end to easily differitate it" << endl;
        cout << "Name suggestion for Player_1: ";
        cout << Player_1  << rand() % 1000 + 1 << endl;

        return 0;
    }
    cout << "Proccessing Each Player's Data" << endl; 
    Player_1_Scores = 0;
    Player_2_Scores = 0;
    Sleep(1000);
    cout << "-------------------LeaderStats-----------------" << endl;
    cout << "-----------------------------------------------" << endl;
    cout << "Player Name " << " || " << " Scores " << " || " << endl;
    cout << "-----------------------------------------------" << endl;
    cout <<  Player_1 << " || " <<    Player_1_Scores   << " || " << endl; 
    cout <<  Player_2 << " || " <<    Player_2_Scores   << " || " << endl; 
    cout << "-----------------------------------------------" << endl;
    cout << "-----------------------------------------------" << endl;
    }
    Sleep(1000);
    cout << "Press Enter again to continue to the game" << endl;
    if (getchar() == '\n') {
        Sleep(2000);
        cout << "By Deciding Who go First, Let's Show it through the Roll" << endl;
        cout << "Each Players's Rolls Will Be Randomized, who has the highest number 1 rolled will go first!" << endl;
        rock_paper_scissor();
       cout <<  Player_Names[rand() % 1 + 0] << " Has Rolled Into Number: " << rand() % 2 + 1 << endl;
       string randomplayer = Player_Names[rand() % 1 + 0];
       name_draft = randomplayer;
       draftplr = randomplayer;
       int CHosen_num = rand() % 2 + 1;
       if (CHosen_num == 2) {
        cout << randomplayer << " Gonna Go First" << endl;
       }
       else {
        cout << randomplayer << " Gonna Go After" << endl;
       }
       Sleep(2000);
       system("cls");
    }
    Sleep(2000);
    cout << "*********Welcome to Tic Tac Toe 5X***********" << endl;
    cout << "Press the number following these choices to choose" << endl;
    cout << choices[0][0]  << endl;
    cout << choices[1][0] << endl;
    cout << choices[2][0] << endl;
    cin >> player_choice;

    switch(player_choice) {
        case 1: {
          tic_tac_toe_system();
          cout << "Type Pos Of The Row: ";
          cin >> rows;
          cout << "Type Pos Of The Collum: ";
            cin >> collums;
            if (rows >= 0 and rows <= 4 and collums >= 0 and collums <= 4) {
                if (board[collums][rows] and turn == draftplr) {
                    board[collums][rows] = 'X';
                    DisplayBoard();
                    Sleep(2000);
                    cout << "Wait for next player's turn" << endl;
                    changing_player();
                    Sleep(5000);
                }
                else if(board[collums][rows] and turn != draftplr)
                board[collums][rows] = 'O';
                cout << "Wait for next player's turn" << endl;
                changing_player();
                Sleep(5000);
                DisplayBoard();
            }
            else if (rows < 0 or rows > 4 and collums < 0 or collums > 4) {
                cout << "Invalid Move!" << endl;
                cout << "Error Move!" << endl;
                cout << "Restart the game!" << endl;
            
            }
          break;
        }
        case 2: {
            game_rules();
            break;
        }
        case 3: {
            cout << "Founder And Creator: " << "Lewiz" << endl;
            cout << "Press E to Show More" << endl;
            while(true) {
                if(_kbhit()) {
                    char Key = _getch();
                    if(Key == 101) {
                        creator();
                        Sleep(5000);
                    }
                }
            }
            break;
        }
        default:
        cout << "Uhh Something Goes Wrong Bud" << endl;
        break;
    }
    return 0;
}
'''
***
](https://github.com/Lewiz1909/Lewiz1909/blob/main/README.md)https://github.com/Lewiz1909/Lewiz1909/blob/main/README.md

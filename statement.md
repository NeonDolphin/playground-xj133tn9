#include <iostream>
int main(){

      int steps;
      int dmg;
      int spHP = 150;
      int trHP = 250;
      int y = 0;
      int key;
 
    
      std::string ins1 = "click some damage: \n";
      std::string ins2 = "insert steps: \n";
      
      std::cout << "Welcome to the Horror House!!!\n";
      std::cout << "How many Steps are you willing to make?\n";
      std::cout << ins2 << std::endl;
      std::cin >> steps;

      while(steps > 10 && y < 10){
            std::cout << "You fell into the pit,try again: \n";
            std::cin >> steps;
            y++;
 }
            if(steps < 10){
                  std::cout << "You encountered a spider!\n";
                  std::cout << ins1;
                  std::cin >> dmg;
            while(dmg < spHP){
                  std::cout << "You were killed,try again: \n";
                  std::cin >> dmg;
            }
            if(dmg >= spHP){
                  std::cout << "Congratulations,you killed a spider!\n";
            }
            std::cout << "you can continue now,with your voyage!\n";
            std::cout << "take some Steps in the dark!\n";
            std::cout << ins2;
            std::cin >> steps;
            while(steps > 10 && y < 10){
            std::cout << "You fell into the pit,try again: \n";
            std::cin >> steps;}
            if(steps <= 10){
                  std::cout << "you came across a Troll!\n";
                  std::cout << ins1;
                  std::cin >> dmg;
            }
            while(dmg < trHP){
                  std::cout << "you were killed by a Troll,try again: \n";
                  std::cin >> dmg;
            }
            if(dmg >= trHP){
                  std::cout << "Great job,you killed a Troll!\n";
                  std::cout << "you found a door,with a number tabs on it!\n";
                  std::cout << "Tabs have numbers: 21, 12, 19 and 74 written on them!\n";
                  std::cout << "Three are wrong, and one is right...enter one: \n";
                  std::cin >> key;
            }
            switch (key){
                  case 21:
                  std::cout << "Bingo!!!" << "\nthe dooor opens and you are free to leave,come again soon!\n";
                  break;
                  case 12:
                  std::cout << "Close enough!" << "you fell into the garbage pit,but you are free...and stinky!!\n";
                  break;
                  case 19:
                  std::cout << "Giant chandelier fell on your head, R.I.P. dude!\n";
                  break;
                  case 74:
                  std::cout << "A Gorilla steps out from the dark and punches you in th face!\n" << "Ciao baby!\n";
                  break;
            }
            }
return 0;
}

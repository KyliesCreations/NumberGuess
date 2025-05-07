//# NumberGuess
//See if your number guess matches the computer
#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main()
{
	int guess = 0;
	char again;
	srand(time(0)); //seed the random number generator with current time
	int random_number = rand() % 10 + 1; //range 1-10
	cout << "Guess what number I'm thinking of between 1 and 10" << endl;
	cin >> guess;
	while (guess != random_number)
	{
		cout << "Wrong! Try again." << endl;
		cin >> guess;
	}
	cout << "You did it! Play again (Y/N)?" << endl;
	cin >> again;
	while (toupper(again) == 'Y')
	{
		random_number = rand() % 10 + 1; //range 1-10
		cout << "Guess what number I'm thinking of between 1 and 10" << endl;
		cin >> guess;
		while (guess != random_number)
		{
			cout << "Wrong! Try again." << endl;
			cin >> guess;
		}
		cout << "You did it! Play again (Y/N)?" << endl;
		cin >> again;
	}
	cout << "Come back and play again sometime!" << endl;
	return 0;
}

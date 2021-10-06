#include<iostream>
using namespace std; 
int main() {

	int room = 1;
	int middle = 2;
	int left = 3;
	int right = 4;
	int straight = 5;
	char input;

	cout << "You wake up to find youself inside of a mansion!" << endl;
	
	do {
		switch (room) {
		case 1:
			cout << "You are in room 1. You can go to the left, middle or right" << endl;
			cin >> input;
			if (input == 'm')
				room = 2;
			else if (input == 'l')
				room = 3;
			else if (input == 'r')
				room = 4;
			else
				cout << "sorry, not an option." << endl;
			break;
		case 2:
			cout << "You are in room 2. It's a deadend" << endl;
			cin >> input;
			if (input == 'b')
				room = 1;
			else
				cout << "sorry, not an option." << endl;
			break;
		case 3: 
			cout << "You are in room 3. It's a deadend" << endl;
			cin >> input;
			if (input == 'b')
				room = 1;
			else
				cout << "sorry, not an option." << endl;
			break;
		case 4:
			cout << "You are in room 4. There's an exit straight ahead" << endl;
			cin >> input;
			if (input == 's')
				room = 5;
			else
				cout << "sorry, not an option." << endl;
			break;
		case 5:
			cout << "You made it out!" << endl;
			cin >> input;
			break;
		
		}

	} while (input != 'q');
}

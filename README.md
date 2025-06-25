# Library-Management-System
This C++ program is a simple Library Management System that allows users to store and display details of up to 20 books. It records information such as Book ID, Name, Author, Borrowing Student's Name, Price, and Pages. The program uses a menu-driven interface to input and view book details or exit the system.
#include <iostream>
#include <string>
using namespace std;
const int MAX_BOOKS = 20;
int main() {
    int ids[MAX_BOOKS];
    string names[MAX_BOOKS];
    string authors[MAX_BOOKS];
    string students[MAX_BOOKS];
    int prices[MAX_BOOKS];
    int pages[MAX_BOOKS];
    int count = 0;
    int input = 0;
    while (input != 3) {
        cout << "Enter 1 to input details like: Id, Name, Author, Student Name, Price, Pages" << endl;
        cout << "Enter 2 to display details" << endl;
        cout << "Enter 3 to quit" << endl;
        cin >> input;
        switch (input) {
            case 1:
                cout << "Enter Book Id: ";
                cin >> ids[count];
                cin.ignore();
                cout << "Enter Book Name: ";
                getline(cin, names[count]);
                cout << "Enter Book Author: ";
                getline(cin, authors[count]);
                cout << "Enter Student Name: ";
                getline(cin, students[count]);
                cout << "Enter Book Price: ";
                cin >> prices[count];
                cout << "Enter Book Pages: ";
                cin >> pages[count];
                count++;
                break;
            case 2:
                for (int i = 0; i < count; i++) {
                    cout << "Book Id: " << ids[i] << endl;
                    cout << "Book Name: " << names[i];
                    cout << "Book Author: " << authors[i];
                    cout << "Student Name: " << students[i];
                    cout << "Book Price: " << prices[i] << endl;
                    cout << "Book Pages: " << pages[i] << endl;
                }
                break;
            case 3:
                exit(0);
            default:
                cout << "You have entered the wrong value. Please try again" << endl;
        }
    }
    return 0;
}

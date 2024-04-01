Assume you oversee a small library and would like to develop a program that looks up books using their ISBNs. A list of books with their corresponding ISBN digits is in front of you. After the librarian inputs an ISBN, your software will look through the list to locate the relevant book.  The book's title and other details will be shown if the book is located. A notice stating that the book is not available in the library will appear if it cannot be located.
code:
#include <iostream>
#include <string>
using namespace std;
int main() {
    cout<<"Parampreet Singh 2310997197";
    string library[][4] = {
        {"978-0545139700", "Harry Potter and Sorcerer's Stone", "J.K. Rowling", "Fantasy"},
        {"978-0439554930", "Harry Potter and Chamber of Secrets", "J.K. Rowling", "Fantasy"},
        {"978-0439064873", "Harry Potter and Prisoner of Azkaban", "J.K. Rowling", "Fantasy"},
    };
    cout << "\nEnter the ISBN of the book you want to search for: ";
    string isbn;
    cin >> isbn;
    bool found = false;
    for (const auto& book : library) {
        if (book[0] == isbn) {
            found = true;
            cout << "Book Found!" << endl;
            cout << "Title: " << book[1] << endl;
            cout << "Author: " << book[2] << endl;
            cout << "Genre: " << book[3] << endl;
            break;
        }
    }
    if (!found) {
        cout << "Book with ISBN " << isbn << " not available in the library." << endl;
    }
    return 0;
}

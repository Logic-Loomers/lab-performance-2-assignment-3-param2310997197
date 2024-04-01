Assume you oversee a small library and would like to develop a program that looks up books using their ISBNs. A list of books with their corresponding ISBN digits is in front of you. After the librarian inputs an ISBN, your software will look through the list to locate the relevant book.  The book's title and other details will be shown if the book is located. A notice stating that the book is not available in the library will appear if it cannot be located.
code:
#include<iostream>
using namespace std;

class locate{
    long long int isbn[5]={9780061120084,9780316769488,9780743273565,9780486284736,9780590353427};
    string book [5]={"To Kill a Mockingbird","1984","The Catcher in the Rye","The Great Gatsby","Pride and Prejudice"};
    string author[5]={"Harper Lee","George Orwell","J.D. Salinger","F. Scott Fitzgerald"," Jane Austen"};
    long long int isbn_no;
 public:
        void get(){
            cout<<"enter the isbn number of the book that you want : "<<endl;
            cin>>isbn_no;
            cout<<endl;
        }
        void locates(){
            int n=0;
            for(int i=0;i<5;i++){
                if(isbn_no==isbn[i]){
                    n=1;
                    cout<<"Your book : "<<book[i]<<endl;
                    cout<<"Author : "<<author[i]<<endl;
  break;
        }
      }
            if(n==0){
                    cout<<"book not found "<<endl;
                }
        }
};
int main(){
    locate l1;
    l1.get();
    l1.locates();

    return 0;
}

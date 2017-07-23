#include <iostream>
#include <ctime>
#include <cstdlib>
#include <time.h>
#include <stdlib.h>
#include <stdio.h>
#include <fstream>
#include <string.h>
#include <cstring>
using namespace std;
int main(int argc, const char * argv[]) {

int a[4];
int repeat[10];
int b;
int i=0;
srand(time(NULL));
for(int j=0 ; j<10 ; j++)
{
    repeat[j] = 0;
}
do
{
    b = rand()%10;
    if(repeat[b] == 0)
    {
        a[i] = b;
        repeat[b] = 1;
        //cout << a[i];
        i++;
    }
    else
    {
        continue;
    }
}while(i<=3);
//cout << "\n";
int guess[4];
string input;
int counta=0;
int countb=0;
int countnum=0;
while(1)
{
    cout << "請輸入任意但不重複的四個數字(包含0) : \n";
    cin >> input;
    countnum++;
    for(int z=0 ; z<4 ; z++)
    {
        guess[z] = input.at(z)-'0';
    }
    for(int g=0 ; g<4 ; g++)
    {
        for(int f=0 ; f<4 ; f++)
        {
            if(guess[g] == a[f])
            {
                countb++;
            }
        }
        if(guess[g] == a[g])
        {
            counta++;
            countb--;
        }
    }
    cout << counta << "A" << countb << "B\n";
    if(counta == 4)
    {
        break;
    }
    else
    {
        counta = 0;
        countb = 0;
        continue;
    }
}
cout << "答對了！\n";
cout << "共猜了" << countnum << "次\n";
return 0;
}

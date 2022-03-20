#include <bits/stdc++.h>
using namespace std;
int main()
{
    ifstream fin;
    // string str;
    fin.open("file.txt");
    int count = 0;
    char str[30];
    int i = 0;

    if (!fin)
    {
        cout << "file did not open" << endl;
    }
    else
    {

        while (!fin.eof())
        {
            fin >> str;
            int len=strlen(str);
            if (str[len-1] == 's' || str[len-1] == 'S')
            {
                count++;
            }
        }
    }

    cout << "total words ends with s  = " << count << endl;
    fin.close();
}

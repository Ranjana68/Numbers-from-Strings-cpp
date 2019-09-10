# Numbers-from-Strings-cpp
C++ code to seprate numbers from a string occuring together eg: string is 123hjh4bhj6hjb34jhb1234jhb  then code will give output as 123, 4, 6, 34, 1234

//source codde
#include<iostream>
#include<vector>
using namespace std;

int main()
{
    vector<string> res;
    string s,r;
    char c;
    cout<<"Enter a string with alphabets and numbers (eg: hads2653hhdsf1234h45j6):"<<endl;;
    cin>>s;
    cout<<"The numbers in given string are:"<<endl;

    for(int i=0;i<s.size();i++)
    {
        if(i==0 &&  isdigit(s[i]))
            {
                r+=s[i];
            }
        else
            {
                if(isdigit(s[i-1]) && isdigit(s[i]))
                    {
                        r+=s[i];
                    }
                else if((isdigit(s[i-1])==0)&&(isdigit(s[i])))
                    {
                        r+=s[i];
                    }
             }


    if(isdigit(s[i+1])==0)
        {
            if (!r.empty())
            {
                cout<<endl<<r;
            }
            r.erase();

        }

    }

return 0;
}

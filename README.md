# ignore-specs-char-and-reverse
class Solution
{
    public:
    string reverse(string str)
    { 
        //code here.
        string temp="";
   
        for(int i=0;i<str.size();i++){
               if( (str[i]>='A' && str[i]<='Z') || (str[i]>='a' && str[i]<='z'))
               {
                   temp+=str[i];
               }
        }
for(int i=0;i<temp.size()/2;i++){
           swap(temp[i],temp[temp.size()-i-1]);
       }
        int k=0;
        for(int i=0;i<str.size();i++){
            if( (str[i]>='A' && str[i]<='Z') || (str[i]>='a' && str[i]<='z'))
            {
               str[i]=temp[k++];
            }
        }
     return str;   
    } 
};

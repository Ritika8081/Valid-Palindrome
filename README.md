# Valid-Palindrome
LeetCode question
class Solution {
public:
bool checkpallindrome(string s,int i,int j){
    while(i<j){
if(s[i]==s[j]){
    i++;
    j--;
}
else{
    return false;
}
    }
    return true;
}
    bool validPalindrome(string s) {
        int i=0;
        int j=s.length()-1;
        while(i<=j){
            if(s[i]==s[j]){
                i++;
                j--;
            }
            else{
                return (checkpallindrome(s,i+1,j) ||checkpallindrome(s,i,j-1));
            }
        }
        return true;
    }
};

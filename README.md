# -
记录当前进度
class Solution {
public:
    vector<int> numberOfLines(vector<int>& widths, string s) {
        int cnt=1,tot=100;
        for(auto i:s) {
            if(tot>=widths[i-'a']) tot-=widths[i-'a'];
            else ++cnt,tot=100-widths[i-'a'];
        }
        vector<int>a(2);
        a[0]=cnt,a[1]=100-tot;
        return a;
    }
};

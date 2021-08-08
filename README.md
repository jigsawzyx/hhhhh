# hhhhh
学习记录
#include <bits/stdc++.h>
using namespace std;
void solve(){
	//这里放自己程序的主函数
	//自己程序的其他函数，直接写在其他地方就行了
	int t;
    cin>>t;
    while(t--){
        int n,x;
        cin>>n>>x;
        int maxx=0;
        bool A=0;
        for(int i=0;i<n;i++){
            int k=0;
            cin>>k;
            maxx=max(k,maxx);
            if(k==x) A=1;
        }
        if(A==1){cout<<1<<endl;continue;}
        if(x%maxx==0) cout<<x/maxx<<endl;
        else if(maxx>x) cout<<2<<endl;
        else cout<<x/maxx+1<<endl;
    }
}

int main(void)
{
    for(int i = 1; i <= 10; i ++)
    {
      string fileName = "";
      string c = to_string(i);//确定对应的标号
      fileName += c;
      fileName += ".in";
      freopen(fileName.c_str(), "r", stdin);
      string fileNameout = "";
      string s = to_string(i);
      fileNameout += s;
      fileNameout += ".out";
      freopen(fileNameout.c_str(), "w", stdout);
      solve();
    }
	fclose(stdin);
	fclose(stdout);
    return 0;
}

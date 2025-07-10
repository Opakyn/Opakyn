## *BAこうぼうAzureMiraclesCo.*
### *Небо принадлежит Кивотосу*
![](https://img.picui.cn/free/2025/06/29/68612cccc666b.jpg)

```cpp
#include<bits/stdc++.h>
using namespace std;
#define ll long long
const ll g=1e6;
ll n,a[g+5];
bool f[g+5];
int main(){
    cin>>n;
    ll ans=n;
    for(int i=1;i<=n;i++){
        ll x,y;cin>>x>>y;
        a[i]=x*g+y;
    }
    sort(a+1,a+1+n);
    int j=2;
    for(int i=1;i<=n;i++){
        //cout<<a[i]<<'\n';
        f[i]=1;
        while(j<n&&a[j]-a[i]<g-1)j++;
        if(f[j]==0&&abs(a[j]-a[i]-g)<2){f[j]=1;ans--;continue;}
        if(f[j+1]==0&&abs(a[j+1]-a[i]-g)<2){f[j+1]=1;ans--;continue;}
        if(f[j+2]==0&&abs(a[j+2]-a[i]-g)<2){f[j+2]=1;ans--;continue;}
    }
    cout<<ans;
    return 0;
}
```

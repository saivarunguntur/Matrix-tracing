#include <bits/stdc++.h>
#define MOD 1000000007
using namespace std;
unsigned long long dp[2*1000001];
unsigned long long fact(unsigned long long n){
    if (n==0) return dp[n] = 1;
    if (~dp[n]) return dp[n];
    return dp[n] = (n%MOD*fact(n-1)%MOD)%MOD;
}
unsigned long long fast_exp(unsigned long long  base, unsigned long long exp){
    base%=MOD;
    unsigned long long result = 1;
    while(exp>0){
        if (exp & 1){
            result = (result*base)%MOD;
        }
        base = (base*base)%MOD;
        exp>>=1;
    }
    return result;
}
int main(){
    //cout<<fast_exp(4,MOD-2)<<"\n";
    memset(dp,-1,sizeof dp);
    int T; cin>>T;
    fact(2000000);
    while(T--){
        unsigned long long m,n;
        cin>>m>>n;
        unsigned long long ans = (dp[m+n-2]%MOD * fast_exp(dp[n-1], MOD-2)%MOD * fast_exp(dp[m-1], MOD-2)%MOD )%MOD;
        cout<<ans<<"\n";
    }
}

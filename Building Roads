//g++  5.4.0
 
#include<bits/stdc++.h>
using namespace std;
 
#define ff first
#define ss second
#define int long long
#define pb push_back
#define pii pair< int,int >
#define fast ios::sync_with_stdio(0) , cin.tie(0) , cout.tie(0) ;
 
const int nax = 1e5+5;
vector<int > g[nax] , vis(nax, 0);
 
void dfs(int n)
{
    vis[n] = 1;
    for( auto &i : g[n] )
        if( !vis[i] )
            dfs( i );
}
 
signed main()
{
    fast ;
    int n , m ;
    cin >> n >> m ;
 
    for(int i=0 ; i<m ; i++ )
    {
        int u , v;
        cin >> u >> v ;
        g[u].pb(v);
        g[v].pb(u);
    }
    vector<int> ans;
    for(int i = 1 ; i<= n ; i++ )
    {
        if( !vis[i] )
        {
            ans.pb(i);
            dfs( i );
        }
    }
    cout << (int)(ans.size()-1) << "\n";
    for(int i=0 ; i<(int)(ans.size()-1) ; i++ )
        cout << ans[i] << " " << ans[i+1] << "\n";
}

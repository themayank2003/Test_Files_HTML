#include <bits/stdc++.h>
using namespace std;

int main() {
    int num_process, num_allocation;
    cin >> num_process >> num_allocation;
    
    unordered_map<char, pair<pair<vector<int>, vector<int>>, pair<vector<int>, vector<int>>>> bank;

    char ch = 'A';
    for(int i = 0; i < num_process; i++) {
        vector<int> allocation, max, available, need;
        
        for(int j = 0; j < num_allocation; j++) {
            int n1;
            cin >> n1;
            allocation.push_back(n1);
        }
        for(int j = 0; j < num_allocation; j++) {
            int n2;
            cin >> n2;
            max.push_back(n2);
        }
        for(int j = 0; j < num_allocation; j++) {
            int n3;
            cin >> n3;
            available.push_back(n3);
        }
        
    
        for(int j = 0; j < num_allocation; j++) 
            {

                int n4;
                cin>>n4;
                        need.push_back(n4);
            }
        bank[ch] = make_pair(make_pair(allocation, max), make_pair(available, need));
        ch++;
    }
   
        for(auto it = bank.begin();it!=bank.end();it++)
        {
            cout<<it->first<<endl;
        }
   
    return 0;
}

# PASCAL_TRIANGLE



#include <iostream>

class solution{
public:
    vector<vector<int>> generate(int numRows) {
        vector<vector<int>> r(numsRow);
        
        for(int i=0; i<numRows; i++){
            r[i].resize(i+1);
            r[i][i]=r[i][i]=1;
            
            for(int j=1; j<i; j++)
            r[i][j] = r[i - 1][j - 1] + r[i - 1][j];
        }
        
        return r;
    }
};
            
       

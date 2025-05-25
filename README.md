
# DSA-algos
ARRAY ALGO :
class Solution {
  public:
//   dutch national flag Algorithm
    void sort012(vector<int>& arr) {
        // code here
        int n  = arr.size();
        int low = 0,mid = 0,high = n-1;
        while(mid <= high){
            if(arr[mid] == 0){
                swap(arr[low] ,arr[mid]) ;
                low ++;
                mid++;
            }
            else if(arr[mid] == 1){
                mid++;
            }
            else{
                swap(arr[mid],arr[high]);
                high--;
            }
        }
    }
};
2) pythagoreanTriplet :
class Solution {
  public:
    bool pythagoreanTriplet(vector<int>& arr) {
        // code here
        unordered_set<int>st(arr.begin(),arr.end());
        int n = arr.size();
        
        for(int i =0;i<n;i++){
            for(int j =i+1;j<n;j++){
            
                 int a = arr[i];
                 int b = arr[j];
                int sq = (a*a) +(b*b);
                int c = sqrt(sq);
                if(c*c ==sq && st.find(c) != st.end()){
                    return true;
                }
            }
        }
            return false;
    }
};

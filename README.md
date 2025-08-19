# CPP_STL_1
DATA STRUCTURES

## NEXT PERMUTATION
    next_permutation(v.begin(), v.end());        //to find the permutation of a number/any datatype
## STRINGS
    String s;
    cin>>s;        //picks up anything before space
    Getline(cin, s);    //Gets till the Line breaks
    cout<<s;
## SWITCH
    switch(int_name){
        case 1: ..... break;
        case 2: ..... break;
        default:.....
    }
## DO WHILE LOOP
    do{    //will execute atleast for once
    }
    while{
    }
Array Always Pass with Reference Automatically

## PAIRS
    pair<int, int>p = {1,2};
      p.first, p.second    // gets me first int =1 and second int =2 
    pair<int<pair<int,int>>p = {1,{2,3}} 
      p.first , p.second.first, p.second.second   // gets me first int 1 and second_first int 2 and second_second int 3
    pair<int,int> arr[] = {{1,2},{3,4},{5,6}}
      arr[1].second  //gets me second element of first index
## VECTORS
    vector<int> v(5,100);   //gets me size 5 and all index initialised as value 100
        v.emplace_back(1);
    vector<pair<int,int>> v;
        v.push_back({1,2);
    vector<int> v2(v);   //gets me a copy of vector v into vector v2
    v.back();    //gets me the last element of vector v
    
    vector<int> ::iterator it = v.begin();  //directly points to the memory of first index(since begin) not the element of the vector
    it++;  //moving to memory of 2nd index
    *it;    //accessing the element from memory by *
    vector<int> ::iterator it = v.end();  //directly points to the memory of an index which is right after the last(since end) element of the vector
    for(vector<int>:: iterator it= v.begin(); it != v.end(); it++) *it;
    for(auto it = v.begin(); it != v.end(); it++) *it;
    for(auto it : v) it;   //gets to access the elements automatically iterating through

    v.erase(v.begin()+1);  //gets to remove the 2nd index of the vector
    v.erase(v.begin()+2; v.begin()+4);  //remove the elements in this way [start, end)
    v.insert(v.begin()+1, 300); //gets to insert 300 at the 2nd index not replace but insert
    v.insert(v.begin()+1, 2, 300); //gets to insert twoo 300 at the 2nd and 3rd index respectively
    v.insert(v.begin(), v1.begin(), v1.end());    //gets to copy a vector v1 into another vector v
    v1.swap(v2);    //gets to swap the vectors
    v.clear;    //gets to erase the entire vector
    v.empty();    //check yes/ no if the vector is empty or not
## LISTS
    list<int> ls;
    ls.front();    //gets to access the front element of the list
    ls.back();    //gets to access the last element of the list
    ls.push_back(2);    //gets to put 2 next to the element present at the list
    ls.push_front(5);    //gets to put 5 at the front of the list
    ls.pop_front();     //gets to remove that front element from list
## DEQUES
    deque<int> dq;
## STACKS
    stack<int>st;    //follows LIFO rule
    st.top();      //gets the access to the top element in the stack
    st.size();    
    st.empty();     //check is yes/no for the stack if empty or not
    stack<int>st1,st2;
    st1.swap(st2);    //swaps the st2 with  st1
## QUEUES
    queue<int>q;    //follows FIFO rule
## HEAP/ PRIORITY QUEUES
    //Maximum Heap
    priority_queue<int> pq;  // top priority: highest element stays at top

    //Minimum Heap
    priority_queue<int, vector<int>, greater<int>> pq;  // least priority: lowest element stays at top
## SETS
    set<int> st;    //stores everything in Sorted Order + Unique elements only (highest element at top)
    auto it: st.find(6);    //starts finding/iterating for value of 6 automatically if not found returns  st.end()
    st.count(1);    //it checks of 1 is present or not
## ERASE IN SETS    
                                                //Erase is done in this way [first, last)
    st.erase(3);     //takes Logarithymic time
    auto it= st.find(3);
    st.erase(it);      //takes Constant time
    auto it1= st.find(2);
    auto it2= st.find(4);
    st.erase(st1, st2); 
## MULTISETS
    multiset<int> ms;    //stores everything in Sorted Order + Duplicate elements are allowed
    ms.erase(2);    //erase all 2 present in that multiset
    ms.erase(ms.find(2));   erase only single 2 not all
    ms.erase(ms.find(2), ms.find(2)+3);    //removes teeno 2 present in the multiset
## UNORDERED SET
    unordered_set<int> st;    //stores Randomly but Unique elements only
                    //lower and upper bound dont work for this
                    //TC is always O(1) for all cases
## MAPS
    map<int> mpp;    //stores in the form {key, value} key is always Unique and Sorted , Value is nit Unique can be of any data type int, string 
    map<int, pair<int, int>> mpp;     //key is int and value is in pair
    map<pair<int,int>, int>> mpp;    //key is in pair and value is in int
    mpp[1] = 2;            //stores 1 as key and 2 as value
    mpp[{2,3}]= 10;        //stores as {2,3} pair of key and 10 as value 

    for(auto it : mpp) it.first; it.second; it++;     //it.first refers to key of first set and it.second refers to key of second set then it++ means moving to second set and the same code                                                             //repeats for second sets key and value
    auto it = mpp.lower_bound(2);
    auto it = mpp.upper_bound(3);
## MULTIMAPS
    multimap<int> mmp;    //stores Duplicate Keys + Sorted Order
                //mmp[key] cannot be used here
## UNORDERED MAPS
    unordered_map<int> unmp;    //stores Unique Keys only + Random Order
                //TC is O(1) for all cases

ALGORITHM

BASIC MATHS CONCEPT 

    //TC always In LOGARITHMIC  if No of Iteration is based on Division
## Extraction of Digits: 
    while(N>10){
        lastdigit = N % 10;
        N= N/10;
    }
## Reverse a number
    revnum = (revnum * 10) + lastdigit
## Check if a number is Palindrome
    int a = N;
    if(revnum == a) return true;

## Armstrong Number 
    371= 3³ + 7³ + 1³ 
    1634 = 1⁴ + 6⁴+ 3⁴ + 4⁴
    while (num > 0) {
        int digit = num % 10;           
        sum += pow(digit, digits);      // last digit is Raised to power of total digits
        num /= 10;                      
    }
## Print all Divisors or factors:
    //any divisor must lie between 1 to N
    //optimising TC at O(n log n) will be finding the Square root of the number then get i to the first half anf n-i to the second half automatically
    for(int i=1; i<=N; i++){
        if(N % i == 0) cout<<i;
    }
    vector<int> ls;
    for(int i=1; i<= sqrt(N); i++){
        if(N % i == 0) ls.push_back(i);
        if((N/i) != i) ls.push_back(n/i);
    }
    sort(ls.begin(), ls.end());
    for(auto it: ls) cout<<ls;
## Prime Number check
    if(n % i == 0) count++;
    if((n/i) != i) count++;
    if(count == 2) return true;        //since a prime number has only 2 factos 1 and itself
## GCD/ HCF:
    for(int i=1; i<= min(n1, n2); i++){        //for loop from the front
        if(n1 % i==0 && n2 % i==0) gcd = i;
    }
    for(int i=min(n1, n2); i>=1; i--){        //for loop from the back
        if(n1 % i==0 && n2 % i==0) gcd = i;
        else cout<<1;
        break;
    }
## EUCLIDEAN ALGORITHM for GCD/HCF
    if(a>b)
    gcd(a-b, b);        //untill we get (0,b) then gcd becomes b to improve TC for a-b,b step
    gcd(a % b, b);
    gcd(greater % smaller, smaller)     //TC = O(log (min(a,b)))
## Recurrsion:
    when a func calls itself untill a specific condition is met... means Base condition & a core relation if formed
    Segmentation Fault in recurrsiion occurs for Stack Overflow // stack space is where the remaining non completed function (yet to be completed) are stored
## Print N times using Recurrsion
    void f(i,n){
        if(i>n) return;
        cout<<"Rex";
        f(i+1, n);
    }
    int main{
        int i, n;
        f(0,n);
    }            TC = O(n) SC= O(n)
## BACKTRACKING:
    means Back Printing i.e moving straight till return while returning we print i.e Backing way of Recurrsion
    void f(i,n){
        if(i>n) return;
        f(i+1, n);
        cout<<"Rex";
    }
    int main(){
        int i, n;
        f(n, n);
    }
## Print sum of n natural numbers in
    Parameterised Way     TC= O(n) SC= O(n)
    void f(i, sum){
        if(i<1) cout<<sum; return;
        f(i-1, sum+i);
    }
    int main(){
        int n=3; 
        f(n,0);
    }
    Functional Way     TC= O(n) SC = O(n)
    f(n){
        if(n == 0) return;
        return n+ f(n-1);
    }
    int main(){
        int n=3; 
        f(n);
    }
## Reverse an Array
    2 Variable
    f(i,j){
        if(i>=j) return;
        swap(a[i], a[j]);
        f(i+1; j-1);
    }
    1 Variable
    f(i,n){
        if(i>=n/2) return;
        swap(a[i], a[n-i-1]);
        f(i+1);
    }
## Checking a Palindrome
    bool f(i){
        if(i>=n/2) return true;
        if(a[i] != a[n-i-1] return false;
        return f(i+1);
    }
## Fibbonacci Number
    f(m){
        if(n<=1) return 1;
        last = n-1;                //1 recurrsion call
        s_last= n-2;                //2 recurrsion call or Multi Recurrsion calls
        return last + s_last;
    }    
    TC= 2^n since every recurrsion call is coupling
## Hashing:
    Pre- Storing / Fetching in Query and doing Pre-Calculation
    int main(){
        //Precomputing
        int hash[13] = {0};    //precomputed 0 in all the 13 boxes of an array
        for(.........){
            hash(arr[i]) += 1;    //if found any number in the array increase the value to 1
        }
        //Query setup
        int q;
        cin>>q;
        while(q--){
            int number;
            cin>>number;
        //Fetch
            cout<<hash[number];
        }
    }
## Checking for LowerCase Alphabets
    //if lowercase if not stated we have to take 256 inplace of 26 then no need to subtract from a
    string s;  cin>>s;
    int hash[26] = {0};
    for(.....){
        hash[s[i] - a] += 1;
    }
    int q; cin>>q;
    'while(q--){
        char ch;
        cin>>ch;
        cout<<hash[ch - 'a'];
    }
## Hashing with Maps:
    //always in Sorted Order due to key and value =  frequency 
    //if we want to check for characters then map<char, int> mpp;
    //pre-compute
    for(....){
        mpp[arr[i]]++;
    }
    int q;
    cin>>q;
    while(q--){
        int number;   cin>>number;
        cout<<mpp[number];
    }
    //iterate through map
    for(auto it: mpp){
        cout<<it.first;
    }
    //In Map both Storing and Sorting takes TC= O(log n)
## Hashing with Unordered Map:
    //here Both Sorting and Fetching takes TC= O(1)
    so by default take Unordered_map if it gives TLE then change to Map

# SORTING
    sort(a, a+n);    //sorting an array
    sort(v.begin(), v.end());  //sorting for a vector
    sort(a+2, a+4);
    sort(a, a+2, greater<int>)    //sorting in Descending order
    sort(a, a+n, comp)    //comp is a function for comparing.... lets say we are comparing 2 sets acc to 2nd element if btoh r same then acc to 1st element but in descending order
                        bool comp(pair<int, int> p1, pair<int, int> p2){
                            if(p1.second<p2.second) return true;
                            if(p1.first>p2.second) return true;
                            return false;
                        }
    int num=6;
    int cnt = _builtin_popcount();        //counts no of sets bits    i.e. turns a number into binary & count its 1s     
                                        //6 -> 111 no of set bits = 3;
    long long num= 1234424723;
    int cnt= _builtin_popcountll();

    //To Find all Possible PERMUTATIONS in a string of sorted order first sort it then ....
    do{cout<<s;}
    while(next_permutation(s.begin(), s.end());
    int maxi= *max_element (a, a+n);        // gets the maximum element from the defined section

    Swapping int array means no direct swap term is used its done by
        int temp = arr[j+1];
        arr[j+1] = arr[j];
        arr[j] = temp;

## SELECTION SORT:   
                        //Means Select Minimum & Swap
                        //TC = O(n²)
    for(int i=0; i<= n-2; i++){
        mini = i;
        for(int j=i; j<n-1; j++){
            if(arr[j] < arr[mini]) mini = j;
        }
        swap (arr[mini], arr[i]);
    }
## BUBBLE SORT:
                        //Means Pushes the Big Bubble/ Maximum to the last by Adjacent swaps
                        //TC = O(n²) //worst and avg
                        //TC = O(n) //Best Case
    for(int i=n-1; i>=1; i--){
        for(int j=0; j<=i; j++){
            if(arr[j] > arr[j+1];
            swap(arr[j], arr[j+1]);
        }
    }
## INSERTION SORT:
                        //Means it Takes/ Picks and element and Places it in the Correct Position and then Repeat
                        //TC= O(n)
    for(int i=0; i<= n-1; i++){
        int j=i;
        while(j>0 && arr[j-1] > arr[j]){
            swap(arr[j-1], arr[j]);
            j--;
        }
    }
## MERGE SORT:
                        //Means it follows Divide and Merge but in Sorted Way
                        //TC = O(n logn)        clearly the Recurrsion occurs one after another\
    Mergesort(arr, low, high){
        if(low >= high) return;
        mid = (low+high)/2;
        Mergesort(arr, low, mid);
        Mergesort(arr, mid+1, high);
        Merge(arr, low, mid, high);
    }

    Merge(arr, low, mid, high){
        int temp[];
        int left= low;
        int right= mid + 1;
        while(left <= mid && right <= high){
            if(arr[left] <= arr[right]){
                temp.add(arr[left]); 
                left++;
            }
            else{
                temp.add(arr[right]);
                right++;
            }
        }
        while(left <= mid){
            temp.add(arr[left]);
            left++;
        }
        while(right <= high){
            temp.add(arr[right]);
            right++;
        }
      //fetch the Merge
        for(int i=low; i<=high; i++){
            arr[i]= temp[i-low];
        }
    }
## QUICK SORT:
                    //Means it follows Divide and Conquer(solve it) Rule
                    //it Sorts any Data Structure in Ascending order but can also be done in Dscending by some changes
                    //TC= O(n logn) and  SC= O(1) ..no extra space used
    //Pick a Pivot and Place it in its Correct Place in the Sorted Array( By Default we Pick Pivot as 1st element)
    //find Element from the left which is greater than pivot and from right which is less than Pivot then Swap the elements
    //so Smaller on left and Larger on right
    //the moment J from right crosses I from left turns out to be position of Pivot element , Now place Pivot at the Position of J this index is called Partition Index , Seperating 2 arrrays        //One Lower Other Higher than pivot
    
    Quicksort(arr, low, high){
        if(low<high){
            PartitionIndex= f(arr, low, high);
            Quicksort(arr, low, PartitionIndex-1);
            Quicksort(arr, PartitionIndex+1, high);
        }
    }
    int f(arr, low, high){
        int Pivot(arr[low]);
        int i= low;
        int j= high;
        while(i<j){
            while(arr[i] <= arr[Pivot] && i<= high-1) i++;
            while(arr[j] > arr[Pivot] && j>= low+1) j--;
            if(i<j) swap (arr[i], arr[j]);
        }
        swap(arr[low], arr[j]);
        return j;
    }        //keep swapping untill the point of crossing (point of getting the pivot index is reached) i.e untill i>j
    
        

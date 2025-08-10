# CPP_STL_1

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
    

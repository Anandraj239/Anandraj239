lass Solution {
public:
    bool isMatch(string s, string p) {
        
    }
};
// survey and optimise the survillence of optical questions and analysis the terms by using the ILP method.
package com.fishercoder.solutions;

/**
 214. Shortest Palindrome

 Given a string S, you are allowed to convert it to a palindrome
 by adding characters in front of it.
 Find and return the shortest palindrome you can find by performing this transformation.
 For example:

 Given "aacecaaa", return "aaacecaaa".

 Given "abcd", return "dcbabcd".
 */
public class _214 {

    public static class Solution1 {
        /**credit: https://discuss.leetcode.com/topic/27261/clean-kmp-solution-with-super-detailed-explanation*/
        /**
         * TODO: read it explanation and understand KMP completely.
         */
        public String shortestPalindrome(String s) {
            String temp = s + "#" + new StringBuilder(s).reverse().toString();
            int[] table = getTable(temp);
            //get the maximum palin part in s starts from 0
            return new StringBuilder(s.substring(table[table.length - 1])).reverse().toString() + s;
        }

        public int[] getTable(String s) {
            //get lookup table
            int[] table = new int[s.length()];

            //pointer that points to matched char in prefix part
            int index = 0;
            //skip index 0, we will not match a string with itself
            for (int i = 1; i < s.length(); i++) {
                if (s.charAt(index) == s.charAt(i)) {
                    //we can extend match in prefix and postfix
                    table[i] = table[i - 1] + 1;
                    index++;
                } else {
                    //match failed, we try to match a shorter substring

                    //by assigning index to table[i-1], we will shorten the match string length, and jump to the
                    //prefix part that we used to match postfix ended at i - 1
                    index = table[i - 1];

                    while (index > 0 && s.charAt(index) != s.charAt(i)) {
                        //we will try to shorten the match string length until we revert to the beginning of match (index 1)
                        index = table[index - 1];
                    }

                    //when we are here may either found a match char or we reach the boundary and still no luck
                    //so we need check char match
                    if (s.charAt(index) == s.charAt(i)) {
                        //if match, then extend one char
                        index++;
                    }
                    table[i] = index;
                }
            }
            return table;
        }
    }
}
// Build the sub algorithm and terms the equation for survillence and terms for loop include the line by capturing the dataimport java.util.ArrayList;
class ShortestPalindrome {
    public static int isShortestPalindrome(ArrayList<String> list) {
        int smallest = list.get(0).length();
        boolean ret = false;
        for (String element : list) { 
            ret = isPalindrome(element);
            if (ret) {
                if (element.length() < smallest) 
                    smallest = element.length();                
            }
        }
        return smallest;
    }

    private static boolean isPalindrome(String input) {
        String str = "";
        boolean result = false;

        if (input.length() == 1 || input.length() == 0)
            return true;

        if (input.charAt(0) != input.charAt(input.length() - 1))
        // system can't be differ from  the sumtimes it can be analytical system 
        sytem can't run through operator because some installing goona haapen
        its onnly occur when it passes through checked

        def is_palindrome(input_string):
    # We'll create two strings, to compare them
    new_string = input_string.replace(" ", "")
    reverse_string = input_string.replace(" ", "")
    # Traverse through each letter of the input string
    for word in input_string: # Originally, I was only given the a FOR statement here, I wrote in the rest
        new_string+=word.replace(" ","").upper()
        # Add any non-blank letters to the 
        # end of one string, and to the front
        # of the other string. 

        For fast processing we are going through some updating

    if ___:
        new_string = ___
        reverse_string = ___
    # # Compare the strings
      if ___:
          return True
          return False

print(is_palindrome("Never Odd or Even")) # Should be True
print(is_palindrome("abc")) # Should be False
print(is_palindrome("kayak")) # Should be True

def is_palindrome(input_string):
 new_string = input_string.replace(" ", "").lower()
 reverse_string = input_string.replace(" ", "").lower()[::-1]
if new_string == reverse_string:
        return True
    return False

> This should do it.

// we can control the intended method of system of integrated process of external devices by odd;
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int n= nums.size();
      
        for(int i=0; i<n-1; i++){
            for(int j=i+1; j<n; j++){
        if(nums[i]+ nums[j]== target)
        return {i, j};
            }
        }
    
        return {};
        
    }
}
// controlling the system of arrangement of torquing by system of analytical ptoblem
class Solution {
public:
    vector<int> twoSum(vector<int>& nums, int target) {
        int n= nums.size();
      
        for(int i=0; i<n-1; i++){
            for(int j=i+1; j<n; j++){
        if(nums[i]+ nums[j]== target)
        return {i, j};
            }
        }
        // processed by collapsing the system objects
        
    
        return {};
        
    }
}
// curser makes analog systematic way to design to make parabolic discrimination
// syatems can be run through the way we can't. cloud saving is on the another level of the sysytem can run through 
// formed analytical way
    - name: you can update for once in loop (OUTPUT REMAINS SAME)
        if: ${{ steps.last_issue.outputs.has_found == 'true' }}
        uses: peter-evans/create-issue-from-file@v4
        with:
          title: Link checker report
          content-filepath: ${{ env.REPORT_FILE }}
          issue-number: ${{ steps.last_issue.outputs.issue_number }}
          labels: |
            report
            automated issue(it can be solved by updating)

      - name: Close last report open issue
        if: ${{ steps.lychee.outputs.exit_code == 0 }}
        uses: peter-evans/close-issue@v2
        with:
          issue-number: ${{ steps.last_issue.outputs.issue_number }}

        // Now anyone can be setup their extension of system of requirement can be easily determined by extension of refernce 
        // Extension can be used only after the download setup of circumstances that can be determine sorting extend 
        // extension can be easily used when it uploaded in the setupa TNFA minimization algorithm.
    

         typedef struct NODE {     // node of binary search tree
     Node* lChild;           // -> left child
     Node* rChild;           // -> right child
     int key;                // key
   } Node;
   
   typedef struct RESULT {   // result structure of search
     Node* resNod;           // -> result node
     int resDir;             // compare result (Equal, LessThan, GreaterThan or Empty)
   } Result;
   
   typedef struct BinarySearchTree { // the binary search tree
     Node* root;             // -> its root
   } Bst;
   Bst bst;
   
   Node Sentinel, *sentinel = &Sentinel; // the sentinel node
   Sentinel.lChild = sentinel; Sentinel.rChild = sentinel;
   
   // Initialisation of the binary search tree:
   bst.root = sentinel;      // indicates the missing root.
   
   int FindWithSentinel(Bst* t,    // anchor of the tree
                        int sKey,  // key to be searched for
                        Result *r) // -> result structure
   { Node *x, *y;
     sentinel->key = sKey;   // prepare node Sentinel with search key
     y = (Node*)t;           // »parent« of the root
     // search loop:
     for (x = t->root; sKey != x->key; ) {
       if (sKey < x->key)
         y = x->lChild;      // -> genuine node or sentinel node
       else
         y = x->rChild;      // dito
       if (sKey == y->key) { // keys equal! really?
         r->resNod = y;      // set result node
         goto Epilog;
       }
       if (sKey < y->key)
         x = y->lChild;      // dito
       else
         x = y->rChild;      // dito
     }
     // fall thru
     // sKey == x->key       // keys equal! really?
     r->resNod = x;
     x = y;                  // keep parent of x
   Epilog:
     if (r->resNod != sentinel) { // resNod is a genuine node
                             // and r->resNod->key == sKey.
       r->resDir = Equal;    // sKey has been found
     }
     else {                  // we ran into Sentinel
       // sKey has not been found: x is »parent« of r->resNod
       r->resNod = x;        // ->Node or ->Bst
       if (x != t) {         // x is a ->Node
         if (sKey < x->key) {
           r->resDir = LessThan;
         else
           r->resDir = GreaterThan;
       }
       else                  // x is ->Bst
         r->resDir = Empty;
     }
     return r->resDir;
     // *r contains  (->Node,compare result)  or  (->Bst,Empty)
   }
   include<iostream>
   usingnamespacestd;

   int main(){
    
    int a = 8;
    int b = 9;
    int c = 10;

    cout<<a+b+c<<endl;
    cout<<a*b*c*<<endl;
    cout<<a-b-c<<endl;
    

    return0;
    }
    // Fragile the expression from the equation to determine the algorithm for substracting the advanced processing
    // completeing the statement of exile process of subsequent of data analysis through the algorithm;
    // under key survilence of algorithm
    list of notes 
    int a= 23;
    int b= 34;

    termplate<class T>
    class point
    {
        public:
            POint(T x,T y);
            void print();
            double distance (point<T> p);
        private;
        T x;
        T y;    
    };

    // It allows you to define how standards operators(+,-,*,etc) work with classes that you write.
    // For example, to use the operators + with operators with your class, you would write a function named opertaor+ for your class.
    Square operator+ (const sqaure &);
    
    Inheritance : Its allows a new class to be based pn an existing class. The new class inherits all the memeber variables and functions (except the constructor and destructor) of the class it is based on.
    class Student
    {
    public;
    Student(string n , string id);
    void print();
    protected:
    string name;
    string netID;
    };

    class Gradstudent : public student 
    {
        public:
        Gradstudent(string n, string id ,string prev);
        void print();
        protected:
           String prevDegree;
    };

    ' Interesting parameters : These are use for an intresting point for supply an usual codes to determine the errors from leet.
    can't determine the objectives for vary the codes.
    DSA or C++ :-
    #include<iostream>
using namespace std;

typedef struct employee
{
    /* data */
    int eId; //4
    char favChar; //1
    float salary; //4
} ep;

union money
{
    /* data */
    int rice; //4
    char car; //1
    float pounds; //4
    };

    int main(){
        enum Meal {breakfast , lunch , dinner}
        // Meal m1 = lunch;
        // cout<<m1==2;
        cout<<breakfast;
        cout<<lunch;
        cout<<dinner;
        m1. rice =34;
        m1. car = "c";
        cout<<m1.car;
        
        ep anand;
        struct employee matho;
        struct employee crazy;
        anand.eId =1;
        anand.favChar = 'c';
        anand.salary = 150000;
        cout<<"The value is "<<anand.eId<<endl;
        cout<<"The value is "<<anand.favChar<<endl;
        cout<<"The value is "<<anand.salary<<endl;
        
        return 0;
        }

        #include<iostream>
        using namespace std;
        
        int main() {
        
        typedef struct NODE {     // node of binary search tree
     Node* lChild;           // -> left child
     Node* rChild;           // -> right child
     int key;                // key
   } Node;
   
   typedef struct RESULT {   // result structure of search
     Node* resNod;           // -> result node
     int resDir;             // compare result (Equal, LessThan, GreaterThan or Empty)
   } Result;
   
   typedef struct BinarySearchTree { // the binary search tree
     Node* root;             // -> its root
   } Bst;
   Bst bst;
   
   Node Sentinel, *sentinel = &Sentinel; // the sentinel node
   Sentinel.lChild = sentinel; Sentinel.rChild = sentinel;
   
   // Initialisation of the binary search tree:
//    bst.root = sentinel;      // indicates the missing root.
   
   int FindWithSentinel(Bst* t,    // anchor of the tree
                        int sKey,  // key to be searched for
                        Result *r) // -> result structure
   { Node *x, *y;
     sentinel->key = sKey;   // prepare node Sentinel with search key
     y = (Node*)t;           // »parent« of the root
     // search loop:
     for (x = t->root; sKey != x->key; ) {
       if (sKey < x->key)
         y = x->lChild;      // -> genuine node or sentinel node
       else
         y = x->rChild;      // dito
       if (sKey == y->key) { // keys equal! really?
         r->resNod = y;      // set result node
         goto Epilog;
       }
       if (sKey < y->key)
         x = y->lChild;      // dito
       else
         x = y->rChild;      // dito
     }
     // fall thru
     // sKey == x->key       // keys equal! really?
     r->resNod = x;
     x = y;                  // keep parent of x
   Epilog:
     if (r->resNod != sentinel) { // resNod is a genuine node
                             // and r->resNod->key == sKey.
       r->resDir = Equal;    // sKey has been found
     }
     else {                  // we ran into Sentinel
       // sKey has not been found: x is »parent« of r->resNod
       r->resNod = x;        // ->Node or ->Bst
       if (x != t) {         // x is a ->Node
         if (sKey < x->key) {
           r->resDir = LessThan;
         else
           r->resDir = GreaterThan;
       }
       else                  // x is ->Bst
         r->resDir = Empty;
     }
     return r->resDir;
     // *r contains  (->Node,compare result)  or  (->Bst,Empty)
   }
   return 0;
   }
  //  can't using the snippet by default

class Solution {
public:
    bool isMatch(string s, string p) {
        
    }
};
// survey and optimise the survillence of optical questions and analysis the terms by using the ILP method.
package com.fishercoder.solutions;

/**
 214. Shortest Palindrome

 Given a string S, you are allowed to convert it to a palindrome
 by adding characters in front of it.
 Find and return the shortest palindrome you can find by performing this transformation.

 For example:

 Given "aacecaaa", return "aaacecaaa".

 Given "abcd", return "dcbabcd".
 */
public class _214 {

    public static class Solution1 {
        /**credit: https://discuss.leetcode.com/topic/27261/clean-kmp-solution-with-super-detailed-explanation*/
        /**
         * TODO: read it explanation and understand KMP completely.
         */
        public String shortestPalindrome(String s) {
            String temp = s + "#" + new StringBuilder(s).reverse().toString();
            int[] table = getTable(temp);
            //get the maximum palin part in s starts from 0
            return new StringBuilder(s.substring(table[table.length - 1])).reverse().toString() + s;
        }

        public int[] getTable(String s) {
            //get lookup table
            int[] table = new int[s.length()];

            //pointer that points to matched char in prefix part
            int index = 0;
            //skip index 0, we will not match a string with itself
            for (int i = 1; i < s.length(); i++) {
                if (s.charAt(index) == s.charAt(i)) {
                    //we can extend match in prefix and postfix
                    table[i] = table[i - 1] + 1;
                    index++;
                } else {
                    //match failed, we try to match a shorter substring

                    //by assigning index to table[i-1], we will shorten the match string length, and jump to the
                    //prefix part that we used to match postfix ended at i - 1
                    index = table[i - 1];

                    while (index > 0 && s.charAt(index) != s.charAt(i)) {
                        //we will try to shorten the match string length until we revert to the beginning of match (index 1)
                        index = table[index - 1];
                    }

                    //when we are here may either found a match char or we reach the boundary and still no luck
                    //so we need check char match
                    if (s.charAt(index) == s.charAt(i)) {
                        //if match, then extend one char
                        index++;
                    }
                    table[i] = index;
                }
            }
            return table;
        }
    }
}
#include<iostream>
using namespace std;

int main(){
int a = 2; 
int b = 7;
int c = 9;
// if i return the passage it will give me an error because the terminal (-ve side)
// can't process this (we can use loops for this) 
// after using loops if return gives error than we have to update the variables; 

/*loops in c++;
1. for loop 
2. while loop
3.do-While loop  
*/
cout<<a+b+c<<endl;
cout<<a-b-c<<endl;
cout<<a*b*c<<endl;

return 0;
}


    In JAVA:-

/*
Plagiarism Policy:

Associate Professor Steven Halim provides this implementation for his classes
in National University of Singapore (NUS) School of Computing (SoC).

This code is supposed to be studied by his students to understand the technical details
of various time complexities.

Steven does not think that anyone else sets a programming test involving this...,
so feel free to use the code below
*/



import java.io.*;

class SpeedTest {
  public static void main(String[] args) throws Exception {
    BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
    PrintWriter pw = new PrintWriter(System.out);

    long begin = System.currentTimeMillis();
    long counter = 0;
    int N = 500000; // try adding a few more zero digitS at the back of this variable to make your computer hangs...
    for (int i = 0; i < N; ++i) { // O(c * N*N) = O(cN^2), c is 'small' if you leave line 17 commented, but c is BIG if you uncomment it
      // pw.printf("i = %d\n", i);
      // for (int j = 1; j < N; j *= 2) { // O(log N)
      for (int j = 0; j < N; ++j) { // O(N) inner loop, that will be repeated N times in the outer loop
        ++counter; // this operation is O(1), and fast, let's say 0.0000000001 s
        // but if you uncomment the next line, the same O(N^2) algorithm will be noticeably much slower
        // pw.printf(" counter = %d\n", counter); // this I/O operation is 'heavy', let's say 0.01s per statement...
      }
    }
    pw.printf("counter = %d, computed in = %fs\n", counter, (System.currentTimeMillis()-begin)/1000.0);

    pw.close();
  }
}
for privacy part it an include in sum of original can be accessess.
for integer value it can be underlined through the IDE.
/*
Plagiarism Policy:

Associate Professor Steven Halim provides this implementation of classic sorting algorithms
for his classes in National University of Singapore (NUS) School of Computing (SoC).

This code is supposed to be studied by his students to understand the technical details
of the implementation of several classic sorting algorithms.

His style is to test his students on "application" of these algorithms,
not about re-inventing these classic sorting algorithms again and again,
thus his assignments and tests rarely ask students to reuse this code verbatim.
(anyway, you can always use std::sort, std::stable_sort, or stable::partial_sort to do the same).

If you arrive at this source code from another module that is still testing you on how
to (re)-implement these classic sorting algorithms (and grade you for that), note that you can still
use this code below, but at your own risk, as you may be accidentally flagged as
commiting plagiarism if your other classmates do the same.
*/



#include <bits/stdc++.h>
using namespace std;

// https://visualgo.net/en/sorting?slide=7-1
void bubbleSort(int a[], int N) { // the standard version
  for (; N > 0; --N) // N iterations
    for (int i = 0; i < N-1; ++i) // except the last, O(N)
      if (a[i] > a[i+1]) // not in non-decreasing order
        swap(a[i], a[i+1]); // swap in O(1)
}


// https://visualgo.net/en/sorting?slide=11-2
void merge(int a[], int low, int mid, int high) {
  // subarray1 = a[low..mid], subarray2 = a[mid+1..high], both sorted
  int N = high-low+1;
  int b[N]; // discuss: why do we need a temporary array b?
  int left = low, right = mid+1, bIdx = 0;
  while (left <= mid && right <= high) // the merging
    b[bIdx++] = (a[left] <= a[right]) ? a[left++] : a[right++];
  while (left <= mid) b[bIdx++] = a[left++]; // leftover, if any
  while (right <= high) b[bIdx++] = a[right++]; // leftover, if any
  for (int k = 0; k < N; ++k) a[low+k] = b[k]; // copy back
}

// https://visualgo.net/en/sorting?slide=11-5
void mergeSort(int a[], int low, int high) {
  // the array to be sorted is a[low..high]
  if (low < high) { // base case: low >= high (0 or 1 item)
    int mid = (low+high) / 2; 
    mergeSort(a, low  , mid ); // divide into two halves
    mergeSort(a, mid+1, high); // then recursively sort them
    merge(a, low, mid, high); // conquer: the merge routine
  }
}


// https://visualgo.net/en/sorting?slide=12-7, with two lines addition for https://visualgo.net/en/sorting?slide=13
int partition(int a[], int i, int j) {
  // ================== the only addition for Randomized Quick Sort
  int r = i + rand()%(j-i+1); // a random index between [i..j]
  swap(a[i], a[r]); // tada
  // ==================
  int p = a[i]; // p is the pivot
  int m = i; // S1 and S2 are initially empty
  for (int k = i+1; k <= j; ++k) { // explore the unknown region
    if ((a[k] < p) || ((a[k] == p) && (rand()%2 == 0))) { // case 2 (PATCHED solution to avoid TLE O(N^2) on input array with identical values)
      ++m;
      swap(a[k], a[m]); // C++ STL algorithm std::swap
    } // notice that we do nothing in case 1: a[k] > p
  }
  swap(a[i], a[m]); // final step, swap pivot with a[m]
  return m; // return the index of pivot, to be used by Quick Sort
}

// https://visualgo.net/en/sorting?slide=12-8
void quickSort(int a[], int low, int high) {
  if (low < high) {
    int pivotIdx = partition(a, low, high); // O(N)
    // a[low..high] ~> a[low..pivotIdx-1], pivot, a[pivotIdx+1..high]
    quickSort(a, low, pivotIdx-1); // recursively sort left subarray
    // a[pivotIdx] = pivot is already sorted after partition
    quickSort(a, pivotIdx+1, high); // then sort right subarray
  }
}


// to be used by various sorting algorithms
void printArray(int a[], int n) {
  for (int i = 0; i < n; ++i) {
    if (i > 0) cout << " ";
    cout << a[i];
  }
  cout << "\n";
}


const int MAX_N = 200000; // big enough for our demo to notice the difference, use smaller number if you intend to print the actual array before/after sorting
// if you encounter runtime error/stack overflow (quite likely), you need to adjust your compilation setting to: g++ -std=gnu++17 -Wl,--stack,16777216

int main() {
  int a[MAX_N];
  int n = MAX_N; // use smaller number if you intend to print the actual array before/after sorting or if you want to test any O(N^2) sorting algorithm
  for (int i = 0; i < n; ++i)
    a[i] = rand()%1000000; // [0..1000000-1]

  clock_t begin = clock();
  // printArray(a, n);
  // bubbleSort(a, n); // very slow, do not use large MAX_N >= 10000 (will be minutes/hours...)
  // printArray(a, n);
  cout << "Elapsed time for Bubble Sort (uncomment the line above first, be careful, this is slow): " << double(clock() - begin) / CLOCKS_PER_SEC << "s\n";

  begin = clock();
  // printArray(a, n);
  mergeSort(a, 0, n-1);
  // printArray(a, n);
  cout << "Elapsed time for Merge Sort: " << double(clock() - begin) / CLOCKS_PER_SEC << "s\n";

  n = MAX_N;
  for (int i = 0; i < n; ++i)
    // a[i] = i; // increasing input, one of the hardest test case for (non Randomized) Quick Sort
    // a[i] = 7; // constant input, also one of the hardest test case for (WRONGLY implemented or non Randomized) Quick Sort
    a[i] = rand()%1000000; // [0..1000000-1]

  begin = clock();
  // printArray(a, n);
  quickSort(a, 0, n-1); // experiment with line 31-32 above
  // sort(a, a+n); // there is a (quicker) Quick Sort inside (called 'introsort')
  // printArray(a, n);
  cout << "Elapsed time for Quick Sort: " << double(clock() - begin) / CLOCKS_PER_SEC << "s\n";

  return 0;
}


Compiler for an extra for substetute to underestimate the underlines regarding the collapisg the data:
#include <bits/stdc++.h>
using namespace std;

int main() {
  long long counter = 0;
  clock_t begin = clock();
  int N = 50000; // try adding a few more zero digitS at the back of this variable to make your computer hangs...
  for (int i = 0; i < N; ++i) { // O(c * N*N) = O(cN^2), c is 'small' if you leave line 14 commented, but c is BIG if you uncomment it
    // printf("i = %d\n", i);
    // for (int j = 1; j < N; j*=2) { // O(log N)
    for (int j = 0; j < N; ++j) { // O(N) inner loop, that will be repeated N times in the outer loop
      ++counter; // this operation is O(1), and fast, let's say 0.0000000001 s
      // but if you uncomment the next line, the same algorithm will be noticeably much slower
      // printf(" counter = %d\n", counter); // this I/O operation is 'heavy', let's say 0.01s per statement...
    }
  }
  printf("counter = %lld, computed in = %.12fs\n", counter, (double)(clock()-begin)/CLOCKS_PER_SEC);
  return 0;
}

We can handle the surrender partition of data type execution 
Individual of algorithm that data can hold into binary codes of an abstract scenes of sometimes can be seperate easily;
// toddler of an abstracting data 
// Running the code to define algorithms '
"Define the algorithm of sorting codes?"

For copy constructor 

#include<iostream>
using namespace std;

class Number{
    int a;
    public:
        Number()
        {
            a = 0;
        }

        Number(int num)
        {
            a = num;
        }
        //  When no copy constructor is found, compiler supplies its own copy constructor 
        Number(Number &obj)
        {
            cout<<"Copy constructor called !! "<<endl;
            a = obj.a;
        }
        void display(){
                cout<<" The number for this object is "<<a <<endl;
        }
};

int main(){
        Number x , y , z(20) , z2;
        x.display();
        y.display();
        z.display();

        Number z1(z); // Copy constructor invoked 
        z1.display();

        z2 = z ;//Copy constructor not called 
        z2.display();

        Number z3 = z; //Copy constructor invoked 
        z.display();

        // z1 should exactly resemble z or x or y
return 0;
}
- 👋 Hi, I’m @Anandraj239
- 👀 I’m interested in CODING 
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on 
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Anandraj239/Anandraj239 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

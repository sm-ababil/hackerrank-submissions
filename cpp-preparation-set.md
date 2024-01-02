## [1. Say "Hello, World!" With C++](https://www.hackerrank.com/challenges/cpp-hello-world/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    printf("Hello, World!");
    return 0;
}
```
## [2. Input and Output](https://www.hackerrank.com/challenges/cpp-input-and-output/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    int m, n, o;
    cin >> m >> n >> o;
    int r = m+ n+ o;
    cout<< r <<endl;
    return 0;
}
```
## [3. Basic Data Types](https://www.hackerrank.com/challenges/c-tutorial-basic-data-types/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    // Complete the code.
    int a;
    long b;
    char c;
    float d;
    double e;
    scanf("%d %ld %c %f %lf",&a,&b,&c,&d,&e);
    printf("%d\n%ld\n%c\n%f\n%lf",a,b,c,d,e);
    
    return 0;
}
```
## [4. Conditional Statements](https://www.hackerrank.com/challenges/c-tutorial-conditional-if-else/problem?isFullScreen=true)
```cpp
#include <bits/stdc++.h>

using namespace std;

string ltrim(const string &);
string rtrim(const string &);



int main()
{
    string n_temp;
    getline(cin, n_temp);

    int n = stoi(ltrim(rtrim(n_temp)));

    // Write your code here
    if (n_temp == "1"){
        cout<<"one"<<endl;
    }
    else if (n_temp == "2"){
        cout<<"two"<<endl;
    }
    else if (n_temp == "3"){
        cout<<"three"<<endl;
    }
    else if (n_temp == "4"){
        cout<<"four"<<endl;
    }
    else if (n_temp == "5"){
        cout<<"five"<<endl;
    }
    else if (n_temp == "6"){
        cout<<"six"<<endl;
    }
    else if (n_temp == "7"){
        cout<<"seven"<<endl;
    }
    else if (n_temp == "8"){
        cout<<"eight"<<endl;
    }
    else if (n_temp == "9"){
        cout<<"nine"<<endl;
    }
    else {
        cout<<"Greater than 9"<<endl;
    }
    
    return 0;
}

string ltrim(const string &str) {
    string s(str);

    s.erase(
        s.begin(),
        find_if(s.begin(), s.end(), not1(ptr_fun<int, int>(isspace)))
    );

    return s;
}

string rtrim(const string &str) {
    string s(str);

    s.erase(
        find_if(s.rbegin(), s.rend(), not1(ptr_fun<int, int>(isspace))).base(),
        s.end()
    );

    return s;
}
```
## [5. For Loop](https://www.hackerrank.com/challenges/c-tutorial-for-loop/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
using namespace std;

int main() {
    // Complete the code.
    int a,b;
    cin>>a;
    cin>>b;
    for (a;a<=b;a++){
        if (a==1){
            cout<<"one"<<endl;
        }
        else if (a==2){
            cout<<"two"<<endl;
        }
        else if (a==3){
            cout<<"three"<<endl;
        }
        else if (a==4){
            cout<<"four"<<endl;
        }
        else if (a==5){
            cout<<"five"<<endl;
        }
        else if (a==6){
            cout<<"six"<<endl;
        }
        else if (a==7){
            cout<<"seven"<<endl;
        }
        else if (a==8){
            cout<<"eight"<<endl;
        }
        else if (a == 9){
            cout<<"nine"<<endl;
        }
        else if (a>9 && a%2 == 0){
            cout<<"even"<<endl;
        }
        else if (a>9 && a%2 != 0){
            cout<<"odd"<<endl;
        }
    }
    return 0;
}
```
## [6. Function](https://www.hackerrank.com/challenges/c-tutorial-functions/problem?isFullScreen=true)
```cpp
#include <iostream>
#include <cstdio>
#include <algorithm>
using namespace std;


int max_of_four(int a, int b, int c, int d){
    int arr[4] = {a,b,c,d};
    int max_num = a;
    for (int i = 0; i<4;i++){
        if (arr[i]>max_num){
            max_num = arr[i];
        }
    }
    return max_num;
}

int main() {
    int a, b, c, d;
    scanf("%d %d %d %d", &a, &b, &c, &d);
    int ans = max_of_four(a, b, c, d);
    printf("%d", ans);
    
    return 0;
}
```
## [7. Arrays Introduction](https://www.hackerrank.com/challenges/arrays-introduction/problem?isFullScreen=true)
```cpp
#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;


int main() {
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */ 
    int N;
    cin>>N;
    int arr[N];
    for(int i=0;i<N;i++){
        cin>>arr[i];
    }
    for(int i=N-1;i>=0;i--){
        cout<<arr[i]<<" ";
    }
      
    return 0;
}

```

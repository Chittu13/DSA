- Imagine you have a number, let's say nn, and you want to find all the smaller numbers that can fit into nn perfectly without leaving any remainder. These smaller numbers are called "factors" of nn. For example, if nn is 10, then its factors are 1, 2, 5, and 10 because:

   - 10 divided by 1 leaves no remainder (10/1 = 10)
   - 10 divided by 2 leaves no remainder (10/2 = 5)
   - 10 divided by 5 leaves no remainder (10/5 = 2)
   - 10 divided by 10 leaves no remainder (10/10 = 1)

- So, the factors of 10 are {1, 2, 5, 10}.

- Now, if someone asks you for the "3rd factor" of 10, you would look at your list of factors {1, 2, 5, 10} and pick the third one in the list, which is 5.

```cpp
#include <iostream>
using namespace std;
#include <string>
#include <vector>
#include <algorithm>

long ithFactor(long n, long i) {
	vector<long> factors;
	for (long j=1;j<=n;++j)
	{
		if(n%j==0)
		{
			factors.push_back(j);
		}
	}
sort(factors.begin(),factors.end());
if(i-1<factors.size()){
	return factors[i-1];
}
else
	return 0;
 
}

int main(int argc, char *argv[]) {
	long n = atol(argv[1]);
	long i = atol(argv[2]);
	cout << ithFactor(n, i) << "\n";
	return 0;
}
```

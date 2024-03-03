# Problem Statement:
- K is a positive integer k.
- Your task is to find the geometric sum i.e. 1 + 1/2 + 1/4 + 1/8 + _______ + 1/(2^k)
- for exameple k=3 --->  1+ 1/(2^1) + 1/(2^2) + 1/(2^3) = 1.875

```cpp
#include <iostream>
using namespace std;
#include <string>
#include <iomanip>
#include <cmath>

float geometricSum(int k) {
if (k==0)
{
	return 1;
}
return 1 /pow(2,k)+geometricSum(k-1);
}
int main(int argc, char *argv[]) {
	int k = atoi(argv[1]);
	cout << scientific;
	cout << setprecision(6) << geometricSum(k) << "\n";
	return 0;
}
```

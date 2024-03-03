# Problem Statement:
### Your task is to determine if the given number num is a Armstrong number or not.
### You will return "true" if number is Armstrong, otherwise return "false".

- For example:
- num = 371.
- no of digits in num are: 3.
- So according to the explanation given above regarding the Armstrong numbers we do 33 + 73 + 13 = 371, so num = 371 is Armstrong no.


```cpp

#include <iostream>
using namespace std;
#include <string>
#include <cmath>

string checkArmstrong(int num) {
	int org=num;
	int rem,n=0;
	float result=0.0;
	
	while (org!=0)
	{
		org /=10;
		n++;
	}
	org=num;
	
	
	while(org!=0)
	{
		rem=org%10;
		result += pow(rem,n);
		org /=10;
	}
	
	if(result==num)
	{
		return "yes";
	}
	else
	{
		return "no";
	}

}

int main(int argc, char *argv[]) {
	int num = atoi(argv[1]);
	cout << checkArmstrong(num)<< "\n";
	return 0;
}
```


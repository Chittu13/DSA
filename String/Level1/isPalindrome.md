# Problem Statement:
- The function should return a boolean indicating whether n is a palindromic number or not.
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>


int isPalindrome(long n) {
	long origi=n;
	long rev=0;
	while(n>0){
		long last=n%10;
		rev=rev*10+last;
		n /=10;
	}
	return (origi==rev) ? 1:0;
}

int main(int argc, char *argv[]) {
	long n = atol(argv[1]);
	printf(isPalindrome(n) ? "true\n" : "false\n");
	return 0;
}
```

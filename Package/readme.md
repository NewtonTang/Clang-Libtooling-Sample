# Code Modification Tool

This is `test.c`:

```c++
//The header is commented because handling header needs additional effort.
//#include <stdio.h>

void do_math(int *x) {
  double target3 = 1;   // need to change to int
  *x += 5;
}

int main(void) {
  double result = -1;
  long double target = 2.0;   //need to change to double
  int target2 = 2;   //need to change to long double
  int val = 4;
  do_math(&val);
  printf("abc\n");
  return result;
}
```

This is what we want our final code would be.

```c++
//The header is commented because handling header needs additional effort.
//#include <stdio.h>

void do_math(int *x) {
  int target3 = 1;   // need to change to int
  *x += 5;
}

int main(void) {
  double result = -1;
  double target = 2.0;   //need to change to double
  long double target2 = 2;   //need to change to long double
  int val = 4;
  do_math(&val);
  printf("abc\n");
  return result;
}
```

# Lab Report 2
**Part 1: String Server**

**Part 2: Lab 3 Bug**
- When testing the ReversedInPlace method originally with the test below it ran perfectly fine.
```
@Test 
  public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```
- However when I tested a longer Array like the one below the bug became clear.
```
@Test
  public void testReverseInPLace3() {
    int[] input = { 2, 4, 6 };
    ArrayExamples.reverseInPlace(input);
    assertArrayEquals(new int[]{ 6, 4, 2 }, input);
  }
```
- an image of what the error looked like.
- Bug: The loop broke halfway through the run probably as a result of the value of i in the 3rd loop. This is because the value at the beginning was changed first so when the value at the end is changed with the one in the beginning it already is 6. The issue was the code was replacing the front of the array without swapping the end so what was originally changed in the front remained the same in the end. By changing the loop to half the arr.length the code was able to properly loop.

- The Original code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
- The fixed code:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length / 2; i += 1) {
      int a = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = a;
    }
  }
```
**Part 3: What I learned**
- In the week 2 lab I learned how to initialize a server and get it running. 
- I was able to create a unique URL for my personal server and get it to run as well as change the URL to manipulate what was shown.
- In the week 3 lab I learned how to search for bugs on code and edit the code to fix the bugs.

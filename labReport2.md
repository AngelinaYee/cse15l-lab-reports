# Lab Report 2

## Part 1

## Part 2

Regarding the bug for reverseInPlace: 
1. A failure-inducing input for the buggy program would be: 

```
@Test
public void testReverseInPlace(){
	int[] input = {1,2,3,4};
	ArrayExamples.ReverseInPlace(input);
	assertArrayEquals(new int[]{4,3,2,1}, input);
}
``` 

2. An input that doesn't induce a failure: 

```
@Test
public void testReverseInPlace1(){
    int[] input2 = {1};
    ArrayExamples.reverseInPlace(input2);
    assertArrayEquals(new int[]{1}, input2);
}
```
3. The symptom (screenshot): 
![Image](The_Symptom.png)

4. The bug:

The code before- 
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
}
```
The code after - 
```
static void reverseInPlace(int[] arr) {
    int [] args = new int[arr.length];
    for (int i = 0; i < arr.length; i += 1) {
      args[i] = arr[arr.length - i - 1];
    }
    for (int i = 0; i < arr.length; i += 1) {
      arr[i]=args[i];
    }
}
```

The issue with the code before was that when the array {1,2,3,4} was added, the array differed at element [2] where the expected was 2, but the output was 3. 
The code was using the array that was in the process of being reversed, which was why the output was three for element [2]. 
In order to fix this, we could create a new int array that the reversed values would go into and then, change the values of arr using a for loop after that process is completed. 
By creating a new int array, and doing `args[i] = arr[arr.length - i - 1]` in the for loop, the program would still be using {1,2,3,4} or the given array since we haven't made any changes to arr yet. 

## Part 3

Something that I learned from week 2 or week 3 would be implementing a web server. 



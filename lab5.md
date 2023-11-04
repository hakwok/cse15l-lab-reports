**Lab Report 2**

**Part 1**
A failure-inducing input
```
@Test
public void testReverseInPlace() {
   int[] input2 = { 2, 4, 1 };
   ArrayExamples.reverseInPlace(input2);
   assertArrayEquals(new int[]{ 1, 4, 2 }, input2);
}
```
An input that doesn't induce a failure
```
@Test
public void testReverseInPlace() {
   int[] input1 = { 3 };
   ArrayExamples.reverseInPlace(input1);
   assertArrayEquals(new int[]{ 3 }, input1);
}
``` 
Symptom
![screen1](/Screenshots/Report3-1.png)
The Bug
``` 
  static void reverseInPlace(int[] arr){
    for(int i = 0; i < arr.length; i+= 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
The fixed code
```
  static void reverseInPlace(int[] arr) {
    int[] tempArr = new int[arr.length];
    for(int i = 0; i < arr.length; i++) {
      tempArr[i] = arr[arr.length - 1 - i];
      arr[arr.length - 1 - i] = tempArr[i];
    }
    for(int i = 0; i < arr.length; i++){
      arr[i] = tempArr[i];
    }
  }
```
The issue with the original code was that it attempted to reverse the array by iterating through it and replacing each element with the element at the corresponding position from the end of the array. However, this approach overwrites the original values before they can correctly move to their new positions, resulting in the array losing the values that need to be included and instead being replaced with values that have already been looped through. The corrected code includes a temporary array to store the values of the reversed array in order to avoid the replacement of values and properly reverse the list.

**Part 2**

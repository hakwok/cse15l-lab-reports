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

I asked BardAI to "list 4 different basic command-line operations for the find command" and the output was 
```-name, -size, -regex, -type.```.

Using ```find -name``` with ./technical:
```
find ./technical -name "*"
```
Output:
```
./technical/directory1/file1.txt
./technical/document.pdf
./technical/image.jpg
./technical/file.txt
```
```
find ./technical -name "reports*"

```
Output:
```
./technical/reportsHousing.txt
./technical/reports/
./technical/reportFromOneYearAgo.pdf
```

The former usage of find -name would simply look through the entirety of the ./technical directory for all files and output them. The latter would look for all files that are within the ./technical directory that have "reports" inside of the name of the path or file. This is helpful for generally searching through a directory to find a file that you might want to use.

In order to find the usage of this command I utilized the following link: [website](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/)

Using ```find -size``` with ./technical:
```
find ./technical -type f -size +100K
```
Output:
```
./technical/file1_largerThan100K
./technical/file2_largerThan100K
./technical/file3_largerThan100K
```
```
find ./technical -type d -size +1M

```
Output:
```
./technical/larger_then1M_directory1
./technical/larger_then1M_directory2
./technical/larger_then1M_directory3
```

The former usage of find -size would look for all files that are approximately 100 kilobytes or larger while the latter usage would look for all directories that are at least a megabyte. This would be helpful to sort out files that are either too small or too large for an operation you plan to undergo.

In order to find the usage of this command I utilized the following link: [website](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/)

Using ```find -regex``` with ./technical:
```
find ./technical -type f -regex ".*/file[0-4]"
```
Output:
```
./technical/file2
./technical/file3
```
```
find ./technical -type d regex ".*/playing[[:alpha:]]+"

```
Output:
```
./technical/playingCrazy
./technical/playingInClass
./technicalplayingWithFriends
```

The former searches for a file with a corresponding number of a certain range, which would be very helpful in finding multiple occurrences of a file belonging to a certain group but only wanting a certain index range. The latter finds directories that include the word playing that also has at least one follow-up word, which is usefull for finding a directory with more than one version of in the form of an ending term but a similar starting term.

In order to find the usage of this command I utilized the following link: [website](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/)

Using ```find -type``` with ./technical:
```
find ./technical -type f"
```
Output:
```
./technical/document.pdf
./technical/image.jpg
./technical/file.txt
```
```
find ./technical -type f -name "*.txt"

```
Output:
```
./technical/files1.txt
./technical/files2.txt
./technical/files3.txt
```

The former finds all files that are within the technical directory, this is useful for finding for files of all kinds instead of just focusing on for example a .txt we can look for .pdf as well. The latter looks for all .txt files within ./technical, which is very helpful when trying to find a specific type of file.

In order to find the usage of this command I utilized the following link: [website](https://linuxize.com/post/how-to-find-files-in-linux-using-the-command-line/)

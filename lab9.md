**Lab Report 5**

**Part 1**

1. ![screen1](/Screenshots/lab5-2.png)<br />
**Student**: There was one failure when running the bash script and I assume that it came from running testMerge2, which indicates that the merge function did not work for a certain test case. The failure states that it timed out at line 19 when running the test case for ListExamples.merge() which indicates that the bug might be causing that line to not work properly. Is my line of thinking correct? On a different note, I'm not quite sure what is causing it to act that way as I am using a code editor without access to viewing the files directly and can only access the terminal.
2. **TA**: Yes, you are on the right track, the test that is not producing the expected output comes from line 19 in ListExamplesTests.java which indicates that you were correct in that testing the Merge function is where we can expect the error. To view and edit the java file you can use vim, try ```vim ListExamples.java``` to open the file, navigate using j,k to move down and up respectively, and h,l to move left and right respectively. Once you are finished editing simply do ```:wq``` to save and exit vim. Once you are finished run your bash script again to check if it is correct. In terms of debugging your code, it seems that your actual list is smaller than the expected list, which indicates that your merge function is not properly adding all of the elements in both arrays. Check the validity of this suggestion by analyzing the code with vim.
3. ![screen1](/Screenshots/right.png)<br />
   ![screen1](/Screenshots/lab5-3.png)<br />
**Student**: Thank you for your help. After using vim to check out the file, I discovered that the bug was located in the last while loop which incremented the index2 by 2 instead of 1, which skipped over 1 index in the second array, causing it to only add 2 out of the 3 elements. I have fixed it and changed it to 1, running ```bash test.sh``` to confirm the tests work properly.

4. Assume that the student was only able to access the terminal and no code editor environment. </br>
![screen1](/Screenshots/right.png)<br />
![screen1](/Screenshots/lab5-4.png)<br />
![screen1](/Screenshots/lab5-5.png)<br />
  Ran ```bash test.sh``` to trigger the bug.
  Edited line 43 from ```index2 += 2``` to ```index2 += 1```.
   
**Part 2** 

Reflection: Something I learned during the second half of this quarter was how to use vim to directly edit files without having an interface to do so. This is especially handy at times when I am unable to access files that are a part of secluded folders and are hard to add to workspaces on vscode, but are readily accessible through the terminal with the usage of -find. Furthermore, after learning about the specific shortcuts and different modes to access, my productivity and speed while addressing buggy files and such have improved immensely. Overall, I felt that lab7 was the most helpful and productive as the muscle memory I gained while dealing with the scenario of having to quickly update and upload changes to Github are very relevant to my future as a programmer.

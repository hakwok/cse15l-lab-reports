**Lab Report 2**

**Part 1**

1. ![screen1](/Screenshots/lab7-1.png)<br />
  There was one failure when running the bash script and I assume that it came from running testMerge2, which indicates that the merge function did not work for a certain test case. The failure states that it timed out at line 44 when running ListExamples.merge() which indicates that the bug might be from that line. Is my line of thinking correct?
2. Yes, you are on the right track, the test that is not producing the expected output comes from line 19 in ListExamplesTests.java which indicates that you were correct in that testing the Merge function is where we can expect the error. Try the following commands to debug the code: ```<javac -g ListExamples.java>``` to compile the java file, ```<jdb -classpath .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests>``` to run jdb on your test file, ```stop at ListExamplesTests:19``` to create a breakpoint at line 19 in which we identified to be producing the symptom, and finally ```run``` to run jdb.
3. ![screen1](/Screenshots/lab7-1.png)<br />
  
4. 

**Part 2**

Reflection: Something I learned during the second half of this quarter was how to use vim to directly edit files without having an interface to do so. This is especially handy at times when I am unable to access files that are a part of secluded folders and are hard to add to workspaces on vscode, but are readily accessible through the terminal with the usage of -find. Furthermore, after learning about the specific shortcuts and different modes to access, my productivity and speed while addressing buggy files and such have improved immensely. Overall, I felt that lab7 was the most helpful and productive as the muscle memory I gained while dealing with the scenario of having to quickly update and upload changes to Github are very relevant to my future as a programmer.

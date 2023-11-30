**Lab Report 4**

4. Log into ieng6<br />
   ![screen1](/Screenshots/lab7-1.png)<br />
   Keys Pressed:```ssh cse15lfa23ig@ieng6.ucsd.edu<enter>```<br />
5. Clone your fork of the repository from your GitHub account<br />
   ![screen2](/Screenshots/lab7-2.png)<br />
   Keys Pressed:```git clone git@github.com:hakwok/lab7.git<enter>```<br />
6. Run the tests, demonstrating that they fail<br />
   ![screen3](/Screenshots/lab7-3.png)<br />
   Keys Pressed:```bash test.sh<enter>```<br />
7. Edit the code file to fix the failing test<br />
    ![screen4](/Screenshots/labt7-4.png)<br />
    Keys Pressed:```vim Li<tab>.java<enter>, 43j, 11k, x, i, 2, <esc>, :wq<enter>.``` Here, I decided not to type out the entirety of ListExamples and used tab to fill up the rest of the file name. After running the command I pressed ```43j``` to move down 43 lines, then ```11k``` to move right 11 indices, ```x``` to delete the 2, ```i``` and ```2``` to insert 2, and finally ```<esc>``` to exit out of the editing mode and ```:wq``` to save and quit out of vim.<br />
8. Run the tests, demonstrating that they now succeed<br />
    ![screen5](/Screenshots/labt7-5.png)<br />
    Keys Pressed:```bash test.sh<enter>```<br />
9. Commit and push the resulting change to your GitHub account (you can pick any commit message!)<br />
    ![screen6](/Screenshots/labt7-6.png)<br />
   Keys Pressed:```git add Li<tab>.java<enter>```. Used tab for the same reason as in step 7.<br />
   ```git commit Li<tab>.java -m "fixed bug"<enter>```. Used tab for the same reason as in step 7, and decided to use the -m shortcut to include the message in the line to save time. <br />
   Keys Pressed:```git push<enter>```<br />

**Lab Report 4**

4. Log into ieng6<br />
   ![screen1](/Screenshots/lab7-1.png)<br />
   ssh cse15lfa23ig@ieng6.ucsd.edu<br />
5. Clone your fork of the repository from your GitHub account<br />
   ![screen2](/Screenshots/lab7-2.png)<br />
   git clone <enter><br />
6. Run the tests, demonstrating that they fail<br />
   ![screen3](/Screenshots/lab7-3.png)<br />
   bash test.sh<enter><br />
7. Edit the code file to fix the failing test<br />
    ![screen4](/Screenshots/labt7-4.png)<br />
    vim Li<tab>.java<enter>, 43j, 11k, x, i, 2, <esc>, :wq<enter><br />
8. Run the tests, demonstrating that they now succeed<br />
    ![screen5](/Screenshots/labt7-5.png)<br />
    bash test.sh<enter><br />
9. Commit and push the resulting change to your GitHub account (you can pick any commit message!)<br />
    ![screen6](/Screenshots/labt7-6.png)<br />
   git add Li<tab>.java<enter><br />
   git commit Li<tab>.java -m "fixed bug"<enter><br />
   git push<enter><br />

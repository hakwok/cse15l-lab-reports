**Lab Report 4**

4. Log into ieng6
   ![screen1](/Screenshots/lab7-1.png)
   ssh cse15lfa23ig@ieng6.ucsd.edu
5. Clone your fork of the repository from your GitHub account
   ![screen2](/Screenshots/lab7-2.png)
   git clone <enter>
6. Run the tests, demonstrating that they fail
   ![screen3](/Screenshots/lab7-3.png)
   bash test.sh<enter>
7. Edit the code file to fix the failing test
    ![screen4](/Screenshots/labt7-4.png)
    vim Li<tab>.java<enter>, 43j, 11k, x, i, 2, <esc>, :wq<enter>
8. Run the tests, demonstrating that they now succeed
    ![screen5](/Screenshots/labt7-5.png)
    bash test.sh<enter>
9. Commit and push the resulting change to your GitHub account (you can pick any commit message!)
    ![screen6](/Screenshots/labt7-6.png)
   git add Li<tab>.java<enter>
   git commit Li<tab>.java -m "fixed bug"<enter>
   git push<enter>

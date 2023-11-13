**Lab Report 4**

4. Log into ieng6
ssh cse15lfa23ig@ieng6.ucsd.edu
5. Clone your fork of the repository from your GitHub account
git clone <enter>
6. Run the tests, demonstrating that they fail
bash test.sh<enter>
7. Edit the code file to fix the failing test
vim Li<tab>.java<enter>, 43j, 11k, x, i, 2, <esc>, :wq<enter>
8. Run the tests, demonstrating that they now succeed
bash test.sh<enter>
9. Commit and push the resulting change to your GitHub account (you can pick any commit message!)
git add Li<tab>.java<enter>
git commit Li<tab>.java -m "fixed bug"<enter>
git push<enter>

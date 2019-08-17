# Using Git

[Back](README.md)

## Github Commands
Have a look at this super helpful [Cheat Sheet from Github](https://education.github.com/git-cheat-sheet-education.pdf) to get you started.

## Git Branching Strategies
I prefer to use the [Github Flow Method](https://guides.github.com/introduction/flow/) so that there are 
no long living branches and it encourages me to release often.

Another popular git branching strategy is called [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow).
It's worth reading about this too as it's used in many large companies.

## Authenticating with Github Using SSH
1. Sign into github, click on your pic in the right top corner and select `settings`.
2. Click on the tab `SSH and GPG Keys`.
3. Click `New SSH Key`.
4. Open a new terminal.
5. Type `ssh-keygen -t rsa`.
6. Follow the prompt keeping all default, you may choose a password if you wish. 
7. You should get something that looks like a square ascii art masterpiece. Your keys have been created.
8. Type `cd ~/.ssh` to change directory to `.ssh`.
9. Type `ls` to view all files.
10. Type `more id_rsa.pub`.
11. Copy ALL the text it returns. 
12. Paste into Github `Key` sections and give it a title that describe which laptop you're using.
13. Click `Add SSH Key`.
14. All done, now you can clone repositories using SSH.

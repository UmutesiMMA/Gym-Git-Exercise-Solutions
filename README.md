# Gym-Git-Exercise-Solutions
## Bundle 1
### Exercise 1
```bash
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Git
$ cd ~/Documents/TheGym/Project1
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1
$ git init
Initialized empty Git repository in C:/Users/user/Documents/TheGym/Project1/.git/

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (master)
$ git branch -m master main

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch start.txt

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch end.txt

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch intro.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch story.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ ls
end.txt  intro.html  lamp.jpeg  start.txt  step.jpeg  story.html  trees-lamp.jpeg
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git add --a
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git mv lamp.jpeg streetlamp.jpeg

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ ls
end.txt     start.txt  story.html       trees-lamp.jpeg
intro.html  step.jpeg  streetlamp.jpeg
user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git add -A

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   end.txt
        new file:   intro.html
        new file:   start.txt
        new file:   step.jpeg
        new file:   story.html
        new file:   streetlamp.jpeg
        new file:   trees-lamp.jpeg


user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git commit -m "First commit"
[main (root-commit) 618306e] First commit
 7 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 end.txt
 create mode 100644 intro.html
 create mode 100644 start.txt
 create mode 100644 step.jpeg
 create mode 100644 story.html
 create mode 100644 streetlamp.jpeg
 create mode 100644 trees-lamp.jpeg
 user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git switch -c dev
Switched to a new branch 'dev'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (dev)
$ git branch test

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (dev)
$ git branch
* dev
  main
  test

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (dev)
$ git branch -d test
Deleted branch test (was 618306e).

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (dev)
$ git branch
* dev
  main

 ```

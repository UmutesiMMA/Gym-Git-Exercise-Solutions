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
 
 ### exercise 2
 ```bash
 user@DESKTOP-TQVNUUS MINGW64 ~
$ cd ~/Documents/TheGym/Project1

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (dev)
$ git switch main
Switched to branch 'main'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch home.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash
No local changes to save

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git status
On branch main
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash
Saved working directory and index state WIP on main: 618306e First commit

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list
stash@{0}: WIP on main: 618306e First commit

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash show
 home.html | 16 ++++++++++++++++
 1 file changed, 16 insertions(+)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git status
On branch main
nothing to commit, working tree clean

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch about.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash -m "About page"
Saved working directory and index state On main: About page

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ touch team.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git add .

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash -m "Team"
Saved working directory and index state On main: Team

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list
stash@{0}: On main: Team
stash@{1}: On main: About page
stash@{2}: WIP on main: 618306e First commit

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash pop index 1
Too many revisions specified: 'index' '1'

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash pop --index 1
<stdin>:20: trailing whitespace.

warning: 1 line adds whitespace errors.
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped refs/stash@{1} (fed11cbd663a7fbe4b3a799344f34f3d35f49b7e)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list
stash@{0}: On main: Team
stash@{1}: WIP on main: 618306e First commit

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash pop stash@{1}
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (f9cf96175da2d7bf0b0e854e3a065f9ebdccd315)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list
stash@{0}: On main: Team

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git commit -m "commit stash pop changes"
[main a31a8b4] commit stash pop changes
 2 files changed, 32 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list
stash@{0}: On main: Team

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash pop
On branch main
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (9c15736e9a1809013af66dcf685240409d33532c)

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash
Saved working directory and index state WIP on main: a31a8b4 commit stash pop change
s

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
$ git stash list
stash@{0}: WIP on main: a31a8b4 commit stash pop changes

user@DESKTOP-TQVNUUS MINGW64 ~/Documents/TheGym/Project1 (main)
```


C:\Users\soukrat55>git clone https://github.com/brik-50/formation_git
Cloning into 'formation_git'...
remote: Enumerating objects: 20, done.
remote: Counting objects: 100% (20/20), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 20 (delta 6), reused 12 (delta 4), pack-reused 0
Receiving objects: 100% (20/20), 6.42 KiB | 821.00 KiB/s, done.
Resolving deltas: 100% (6/6), done.

C:\Users\soukrat55>cd formation_git

C:\Users\soukrat55\formation_git>git log
commit fd91f995063d1a0c516e94990fdf0fe72266b888 (HEAD -> main, origin/main, origin/HEAD)
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Mon Feb 19 12:15:38 2024 +0100

    Update README.md

commit b9b63e3c2b4098b088c080cbf9ab5bb2d6d9d251
Merge: 6316ade 50621de
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Mon Feb 19 12:14:33 2024 +0100

    Merge branch 'main' of https://github.com/brik-50/formation_git

commit 6316ade240bca5bd3dd7c6bcd4beb5ac3aa4542c
Merge: 4b879c8 7cd28e7
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Fri Feb 16 18:43:18 2024 +0100

    Merge branch 'main' of https://github.com/brik-50/formation_git

commit 50621def1743d84b2538c325c2e19338aadf6134
Merge: 4b879c8 7cd28e7
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Fri Feb 16 18:43:18 2024 +0100

    Merge branch 'main' of https://github.com/brik-50/formation_git

commit 4b879c8a37fab9c35749340ab932d017c00fe9e9
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Fri Feb 16 17:52:56 2024 +0100

    feat: add new files

commit 7cd28e78201a73fccb0d867a46cd94ca779fc2b0
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Fri Feb 16 17:52:56 2024 +0100

    feat: add new files

commit c2a32207bd7784f40c1c3d1f3ab3e8a559617605
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Fri Feb 16 17:49:33 2024 +0100

    Initial commit

C:\Users\soukrat55\formation_git>git diff 7cd28e78201a73fccb0d867a46cd94ca779fc2b0 c2a32207bd7784f40c1c3d1f3ab3e8a559617605
diff --git a/index.html b/index.html
deleted file mode 100644
index dd2afcf..0000000
--- a/index.html
+++ /dev/null
@@ -1,26 +0,0 @@
-<!DOCTYPE html>
-<html lang="en">
-<head>
-    <meta charset="UTF-8">
-    <meta name="viewport" content="width=device-width, initial-scale=1.0">
-    <title>todo list</title>
-    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-giJF6kkoqNQ00vy+HMDP7azOuL0xtbfIcaT9wjKHr8RbDVddVHyTfAAsrekwKmP1" crossorigin="anonymous">
-    <link rel="stylesheet" href="style.css">
-</head>
-<body>
-    <div class="container">
-        <div class="row row1" id="row-1">
-            <h1>TODO</h1>
-            <br>
-            <div class="input-group mb-3">
-                <input type="text" class="form-control" id="saisir"  aria-describedby="button-addon2">
-                <button class="btn btn-outline-secondary add " type="button" id="button-addon2">+</button>
-              </div>
-        </div>
-        <div class="row " id="list">
-
-        </div>
-    </div>
-    <script src="script.js"></script>
-</body>
-</html>
\ No newline at end of file
diff --git a/script.js b/script.js
deleted file mode 100644
index ac2543b..0000000
--- a/script.js
+++ /dev/null
@@ -1,36 +0,0 @@
-//selectors
-const add=document.querySelector(".add");
-var saisir=document.querySelector("#saisir");
-var row2=document.querySelector("#row2");
-var list=document.querySelector("#list");
-var todolist=document.getElementById("row2")
-
-//addeventlistner
-add.addEventListener("click" , ()=>{
-    var paragraph=document.createElement('p');
-    list.appendChild(paragraph);
-    paragraph.innerText=saisir.value;
-    paragraph.style.padding='0px 0px 0px 150px'
-    paragraph.addEventListener('click', ()=>{
-        paragraph.style.textDecoration="line-through";
-    })
-    paragraph.addEventListener('dblclick', ()=>{
-        list.removeChild(paragraph);
-    })
-
-
-
-    saisir.value=''
-
-});
-
-
-
-
-
-
-//functions
-
-
-
-
diff --git a/style.css b/style.css
deleted file mode 100644
index 1aab153..0000000
--- a/style.css
+++ /dev/null
@@ -1,6 +0,0 @@
-.row1{
-    margin: 50px;
-}
-p{
-    padding: 0px  0px  0px 150px ;
-}

C:\Users\soukrat55\formation_git>git commit --amend --no-edit
Committer identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got 'soukrat55@DESKTOP-R1HQFTR.(none)')

C:\Users\soukrat55\formation_git>git config --global user.email "fleursoukrat@gmail.Com"

C:\Users\soukrat55\formation_git>git config --global user.email "fleursoukrat@gmail.com"

C:\Users\soukrat55\formation_git>git config --global user.name "Soukrat55"

C:\Users\soukrat55\formation_git>git commit --amend --no-edit
[main 9f63543] Update README.md
 Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
 Date: Mon Feb 19 12:15:38 2024 +0100
 1 file changed, 2 insertions(+), 2 deletions(-)

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        hello.html

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\soukrat55>git clone https://github.com/Soukrat55/formation_git
Cloning into 'formation_git'...
remote: Enumerating objects: 20, done.
remote: Counting objects: 100% (20/20), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 20 (delta 6), reused 13 (delta 4), pack-reused 0
Receiving objects: 100% (20/20), 6.42 KiB | 938.00 KiB/s, done.
Resolving deltas: 100% (6/6), done.

C:\Users\soukrat55>git status
fatal: not a git repository (or any of the parent directories): .git

C:\Users\soukrat55>cd formation_git

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   index.html

no changes added to commit (use "git add" and/or "git commit -a")


C:\Users\soukrat55\formation_git>git commit -m "modification index.html"
[main 31fbf52] modification index.html
 1 file changed, 1 insertion(+), 1 deletion(-)

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

C:\Users\soukrat55\formation_git>git add solutions.md
fatal: pathspec 'solutions.md' did not match any files

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        solutions.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\soukrat55\formation_git>git commit -m "ajout solutions.md"
[main 624b481] ajout solutions.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 solutions.md

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean


C:\Users\soukrat55\formation_git>git commit -m "suppression solutions.md"
[main b778722] suppression solutions.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 solutions.md

C:\Users\soukrat55\formation_git>git log
commit b7787226b2e98c64522e6bf156dfd546368dd294 (HEAD -> main)
Author: Soukrat55 <fleursoukrat@gmail.com>
Date:   Fri Mar 1 10:23:51 2024 +0100

    suppression solutions.md

commit 624b48164b2f0ec4d639c931ccf73e601e032c75
Author: Soukrat55 <fleursoukrat@gmail.com>
Date:   Fri Mar 1 10:23:04 2024 +0100

    ajout solutions.md

commit 31fbf52e134e371705e17e5f4d8b9c2f4e200055
Author: Soukrat55 <fleursoukrat@gmail.com>
Date:   Fri Mar 1 10:21:39 2024 +0100

    modification index.html

commit fd91f995063d1a0c516e94990fdf0fe72266b888 (origin/main, origin/HEAD)
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Mon Feb 19 12:15:38 2024 +0100

    Update README.md

commit b9b63e3c2b4098b088c080cbf9ab5bb2d6d9d251
Merge: 6316ade 50621de
Author: MOHAMED AIT BRIK <74569734+brik-50@users.noreply.github.com>
Date:   Mon Feb 19 12:14:33 2024 +0100


C:\Users\soukrat55\formation_git>git push origin newbranche
error: src refspec newbranche does not match any
error: failed to push some refs to 'https://github.com/Soukrat55/formation_git'

C:\Users\soukrat55\formation_git>git push origin
info: please complete authentication in your browser...
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 608 bytes | 608.00 KiB/s, done.
Total 6 (delta 4), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (4/4), completed with 2 local objects.
To https://github.com/Soukrat55/formation_git
   fd91f99..b778722  main -> main

C:\Users\soukrat55\formation_git>git push origin newbranche
error: src refspec newbranche does not match any
error: failed to push some refs to 'https://github.com/Soukrat55/formation_git'

C:\Users\soukrat55\formation_git>git push origin master
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/Soukrat55/formation_git'

C:\Users\soukrat55\formation_git>git rm fichier_inutile.txt
rm 'fichier_inutile.txt'

C:\Users\soukrat55\formation_git>git commit -m "suppression fichier inutile"
[main 5060267] suppression fichier inutile
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 fichier_inutile.txt

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

C:\Users\soukrat55\formation_git>git push origin
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 234 bytes | 234.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Soukrat55/formation_git
   b778722..5060267  main -> main

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        solutions.md

nothing added to commit but untracked files present (use "git add" to track)

C:\Users\soukrat55\formation_git>git add .

C:\Users\soukrat55\formation_git>git commit -m "ajout solutions.md"
[main e83c406] ajout solutions.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 solutions.md

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean

C:\Users\soukrat55\formation_git>git push origin master
error: src refspec master does not match any
error: failed to push some refs to 'https://github.com/Soukrat55/formation_git'

C:\Users\soukrat55\formation_git>git push origin
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 274 bytes | 274.00 KiB/s, done.
Total 3 (delta 1), reused 1 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Soukrat55/formation_git
   5060267..e83c406  main -> main

C:\Users\soukrat55\formation_git>git branch
* main

C:\Users\soukrat55\formation_git>git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean


# PULL REQUEST (PR), MERGE PR. REJECT PR

$ ls -l
total 112
-rw-r--r--@ 1 javedalam  staff   2148 Aug  9 13:12 0-create-repository.md
-rw-r--r--@ 1 javedalam  staff     76 Aug  9 13:12 1-Git-Installations.md
-rw-r--r--@ 1 javedalam  staff   7107 Aug  9 13:12 2-Conflict-Pull-LifeCycle.md
drwxr-xr-x@ 5 javedalam  staff    160 Aug  9 13:12 3-Git-Documents
-rw-r--r--@ 1 javedalam  staff  32294 Aug  9 13:12 4-Git-Commands.md
-rw-r--r--@ 1 javedalam  staff   7837 Aug 10 12:27 5-git-fork-commands.md
$ 
$ git branch 
* master
$ git branch feature 
$ git checkout feature
Switched to branch 'feature'
$ ls -l
total 112
-rw-r--r--@ 1 javedalam  staff   2148 Aug  9 13:12 0-create-repository.md
-rw-r--r--@ 1 javedalam  staff     76 Aug  9 13:12 1-Git-Installations.md
-rw-r--r--@ 1 javedalam  staff   7107 Aug  9 13:12 2-Conflict-Pull-LifeCycle.md
drwxr-xr-x@ 5 javedalam  staff    160 Aug  9 13:12 3-Git-Documents
-rw-r--r--@ 1 javedalam  staff  32294 Aug  9 13:12 4-Git-Commands.md
-rw-r--r--@ 1 javedalam  staff   7837 Aug 10 12:27 5-git-fork-commands.md
$ 
$ git branch 
* feature
  master
$ 
$ vim 5-git-fork-commands.md 
$ git status
On branch feature
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   5-git-fork-commands.md

no changes added to commit (use "git add" and/or "git commit -a")
$ git add 5-git-fork-commands.md ; git commit -m "line added and removed"
[feature 9a4631a] line added and removed
 1 file changed, 4 insertions(+), 2 deletions(-)
$ git push 
fatal: The current branch feature has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin feature

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

$ 
$ git push --set-upstream origin feature 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 8 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 371 bytes | 371.00 KiB/s, done.
Total 4 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 3 local objects.
remote: 
remote: Create a pull request for 'feature' on GitHub by visiting:
remote:      https://github.com/xavyaly/git-lab/pull/new/feature
remote: 
To https://github.com/xavyaly/git-lab.git
 * [new branch]      feature -> feature
branch 'feature' set up to track 'origin/feature'.


# NOTE:
Switched to github.com UI
You can see PR has been raised
Click on "Compare & Pull Request" button
Add a proper comment 
Click on "Create Pull Request"
Next add 1-2 reviewers who can review your code
Once added, reviewers will get an email to review
Reviewers landed to your github page and review the code
It reviewers think your code is valid then he Merge your code 
Else he/she will reject your code 

$ git branch 
* feature
  master
$ 
$ git checkout master 
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
$ 
$ git branch --delete feature 
warning: deleting branch 'feature' that has been merged to
         'refs/remotes/origin/feature', but not yet merged to HEAD.
Deleted branch feature (was 9a4631a).
$ 
$ git push origin --delete feature 
To https://github.com/xavyaly/git-lab.git
 - [deleted]         feature
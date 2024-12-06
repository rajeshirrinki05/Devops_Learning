# git log

Git log command will be used for to view the commits history of a repository. It will show the detail list of information related to commits such as commit hash, author, commit messages and commit date and time.

<h3> Here are some git log usage and options </h3>

<b>Basic usage: </b> If you run the git log directly it will provide all the commits history of the repository.

Syntax : 
``` 
git log   
```
Example :
```
root@C-FFF3P32T7:~/Devops_Learning/Git# git log
commit 962f76ea14ced4bc5f8de9db9503d01d47684941 (HEAD -> main)
Author: root <root@C-PF3PN2T7>
Date:   Fri Dec 6 04:23:53 2024 +0530

    corrected the errors in the Readme.md file

commit 85775068db8855fd7e571557c18a27179b40a962
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:57:30 2024 +0530

    removed italic style in the git.md

commit 046bf218926b4fc98130bf918035d6aeb534bc53
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:52:54 2024 +0530

    content finalised for git.md file

commit a69770ae12631e11606062f7879b659cb4b27a39
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:34:39 2024 +0530

    content enhanced


```

<h3>Commit history for specific file: </h3> We can get the commit history of a specific file.

Syntax : 
``` 
git log  <specifyFileName>
```
Example :
```
root@C-PF3PN2T7:~/Devops_Learning/Git#
root@C-PF3PN2T7:~/Devops_Learning/Git# git log Git.md
commit 85775068db8855fd7e571557c18a27179b40a962
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:57:30 2024 +0530

    removed italic style in the git.md

commit 046bf218926b4fc98130bf918035d6aeb534bc53
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:52:54 2024 +0530

    content finalised for git.md file

```
<h3>Limit the number of commits:</h3>

It will show the last specified number of commits history of the repository.

Syntax :
```
git log -n <number>
```
Example :
```
root@C-PF3PN2T7:~/Devops_Learning/Git# git log -n 2
commit 962f76ea14ced4bc5f8de9db9503d01d47684941 (HEAD -> main)
Author: root <root@C-PF3PN2T7>
Date:   Fri Dec 6 04:23:53 2024 +0530

    corrected the errors in the Readme.md file

commit 85775068db8855fd7e571557c18a27179b40a962
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:57:30 2024 +0530

    removed italic style in the git.md
root@C-PF3PN2T7:~/Devops_Learning/Git#
```


<h3> git patch : </h3>

Git patch will displays the modifications done in each commit.

Syntax:
```
git log -p
```
Output
```
root@C-PF3PN2T7:~/Devops_Learning/Git#
root@C-PF3PN2T7:~/Devops_Learning/Git# git log -p
commit 962f76ea14ced4bc5f8de9db9503d01d47684941 (HEAD -> main)
Author: root <root@C-PF3PN2T7>
Date:   Fri Dec 6 04:23:53 2024 +0530

    corrected the errors in the Readme.md file

diff --git a/README.md b/README.md
index 24fe42e..0aaea11 100644
--- a/README.md
+++ b/README.md
@@ -2,7 +2,7 @@

 This Repository contains all the DevOps Tools installation guide and learning with setup of all required commands

-***-> Tools Included:***
+<h2> Tools Included:</h2>^M
 <body>
 <p>Jenkins</p>
 <p>Git</p>
@@ -12,7 +12,7 @@ This Repository contains all the DevOps Tools installation guide and learning wi
 <p>Terraform</p>
 <p>AWS (Cloud)</p>
 <p>Premotheous</p>
-<p>**Grafana</p>
-<p>**Maven</p>
+<p>Grafana</p>^M
+<p>Maven</p>^M
 <p>Splunk</p>
 </body>
```
<h3> Filter Commits by Author :</h3>

It will display all the commits of the repository done by the specified author.

Syntax :

```
git log --author "authorName"
```
Example:
```
root@C-PF3PN2T7:~/Devops_Learning/Git# git log -n 2
commit 962f76ea14ced4bc5f8de9db9503d01d47684941 (HEAD -> main)
Author: root <root@C-PF3PN2T7>
Date:   Fri Dec 6 04:23:53 2024 +0530

    corrected the errors in the Readme.md file

commit 85775068db8855fd7e571557c18a27179b40a962
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:57:30 2024 +0530

    removed italic style in the git.md
root@C-PF3PN2T7:~/Devops_Learning/Git# git log --author="rajeshirrinki"
commit 85775068db8855fd7e571557c18a27179b40a962
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:57:30 2024 +0530

    removed italic style in the git.md

commit 046bf218926b4fc98130bf918035d6aeb534bc53
Author: rajeshirrinki <60837660+rajeshirrinki05@users.noreply.github.com>
Date:   Thu Dec 5 19:52:54 2024 +0530

    content finalised for git.md file
```
<h3> Pretty print the commit history : </h3>

It will shows each commit in a single line. This will help for review the commits quickly.

Syntax :
```
git log --pretty=online
```

Example :
```
root@C-PF3PN2T7:~/Devops_Learning/Git# git log --pretty=oneline
962f76ea14ced4bc5f8de9db9503d01d47684941 (HEAD -> main) corrected the errors in the Readme.md file
85775068db8855fd7e571557c18a27179b40a962 removed italic style in the git.md
046bf218926b4fc98130bf918035d6aeb534bc53 content finalised for git.md file
a69770ae12631e11606062f7879b659cb4b27a39 content enhanced
ebb2515c58f3ee7e2966d8f9d65487e76ddbce3f fixed the content typos in git.md file
```

These are just a few examples of how we can use the git log command to explore our repository's history. We can go through more available options by using git help or man pages.

``` git log --help ```
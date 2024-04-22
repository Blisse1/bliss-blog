---
title: "Git notes from ProGit"
description: "Git learning"
publishDate: "22 April 2024"
tags: ["git-learning"]
---

## Git notes
## About git add
"If you modify a file after you run git add, you have to run git add again to stage the
latest version of the file"
## About git status
New files that aren’t tracked have a ?? next to them
New files that have been added to the staging area have an A
Modified files have an M and so on
There are two columns to the output — the lefthand column indicates the status
of the staging area and the right-hand column indicates the status
of the working tree
## About git diff
Git diff compares what is in your working directory with what is on your staging area.
The results tells you the changes you've made that you haven't staged.

If you want to see what you've staged that will go to your next commit, you can use ```git
diff --staged```

It’s important to note that git diff by itself doesn’t show all changes made since your last
commit — only changes that are still unstaged. If you’ve staged all of your changes, git diff will
give you no output.
## About git commit
For an even more explicit reminder of what you’ve modified, you can pass the -v
option to git commit. Doing so also puts the diff of your change in the editor so you
can see exactly what changes you’re committing
Adding the -a option to the git commit command makes
Git automatically stage every file that is already tracked before doing the commit, letting you skip
the git add part: git commit -a -m "Add new benchmark"
## About git rm
If you modified the file or
had already added it to the staging area, you must force the removal with the -f option.
Another useful thing you may want to do is to keep the file in your working tree but remove it from
your staging area. This is particularly useful if you forgot to add something to your .gitignore
file and accidentally staged it, like a large log file or a bunch of .a compiled files. To do this, use the
--cached option: git rm --cached FILE
## About moving files on git
git mv file_from file_to
In fact, if you run something like this and look at the status, you’ll see that Git
considers it a renamed file: git mv file_from file_to
The only real difference is that git mv is one command instead of three
## About git log
One of the more helpful options is -p or --patch, which shows the difference (the patch output)
introduced in each commit. You can also limit the number of log entries displayed, such as using -2
to show only the last two entries.

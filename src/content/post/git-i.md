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
Another really useful option is --pretty. This option changes the log output to formats other than
the default. A few prebuilt option values are available for you to use. The oneline value for this
option prints each commit on a single line, which is useful if you’re looking at a lot of commits. In
addition, the short, full, and fuller values show the output in roughly the same format but with
less or more information, respectively
git log --pretty=format:"%h - %an, %ar : %s"
This option adds a nice little ASCII graph showing your branch and merge history:
git log --pretty=format:"%h %s" --graph
However, the time-limiting options such as --since and --until are very useful. For example, this
command gets the list of commits made in the last two weeks
git log --since=2.weeks
For instance, if you wanted to find the last commit that added or removed a reference to a
specific function, you could call: git log -S function_name
The last really useful option to pass to git log as a filter is a path. If you specify a directory or file
name, you can limit the log output to commits that introduced a change to those files
git log -- path/to/file
## About undoing things (ammend)
One of the common undos takes place when you commit too early and possibly forget to add some
files, or you mess up your commit message. If you want to redo that commit, make the additional
changes you forgot, stage them, and commit again using the --amend option: $ git commit --amend
It’s important to understand that when you’re amending your last commit, you’re
not so much fixing it as replacing it entirely with a new, improved commit that
pushes the old commit out of the way and puts the new commit in its place.
Effectively, it’s as if the previous commit never happened, and it won’t show up in
your repository history.
The obvious value to amending commits is to make minor improvements to your
last commit, without cluttering your repository history with commit messages of
the form, “Oops, forgot to add a file” or “Darn, fixing a typo in last commit”.
Only amend commits that are still local and have not been pushed somewhere.
Amending previously pushed commits and force pushing the branch will cause
problems for your collaborators

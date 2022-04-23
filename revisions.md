# Git Intro

## Version Control

A Version Control System (VCS) keeps track of previous versions of files, allowing you to track which edits were made when and by whom. New versions can be easily reverted if you find mistakes. The original VCSs were local to a user's computer, which limited collaboration. 

Centralized and Distributed Version Control Systems (CVCS and DVCS, respectively) were created to allow developers to collaborate. In a CVCS, everything is stored on the same server. This makes it easy to track work, but having all files in a single central location means a single system failure can take down the whole operation. A DVCS addresses this by allowing multiple mirrored repositories, so if one is damaged, another can be copied over to replace it.

## What is Git?

Git is a DVCS. Every time you save (commit) a change to a file, Git saves a snapshot of the file's current state, tracking every single change that has been made over the course of a project and organizing that information for you. A copy of that information is stored locally, which means it spends less time and energy communicating with the server and means you can work on a project when you're offline.

Files can be "staged" (flagged to be committed in the next snapshot), "modified" (changes have been made, but not saved), or "committed" (the file is saved).

Git can be installed on Windows, Mac, or Linux. You can import existing local projects or clone them from a server.

## Workflow

Your local installation of Git has three components: the working directory, where all the files live, the index, where files are staged, and the head, which is the most recent version. 


---
title: "VCs. Git"
subtitle: Welcome! This article is dedicated to VCs, their use and functions. Also you will learn more about the most used VCS in the worla - Git.

# Summary for listings and search engines
summary: Welcome! This article is dedicated to VCs, their use and functions. Also you will learn more about the most used VCS in the worla - Git

# Link this post with a project
projects: []

# Date published
date: '2023-03-10T00:00:00Z'

# Date updated
lastmod: '2023-03-10T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named featured.jpg/png in this page's folder and customize its options here.
image:
  caption: 'Image credit: **Unsplash** (https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ''
  placement: 2
  preview_only: false

authors:
  - admin

tags:
  - git
  - VCs
  - systems of version control

categories:
  - Demo
---

## Version control systems. Git

## Version control. Git.

Version control systems (VCS, vngl. VCS - Vesion Control Systems) are used when several people are working on a project. They allow you to roll back to previous versions of the project without losing new developments and changes made to the project. For example, the developers posted a new version of the project, but there were errors in it. In order not to lose changes and correct errors, thanks to version control systems, it is possible to return to the old, working version, and then eliminate the flaws.

Users, in turn, have the opportunity to see what exactly has changed and compare the new version with the old one. Developers see who and what changes have been made to the project, so that if anything happens, they know who to ask.

Of course, you can simply copy the project to another directory, this approach is often used because of its simplicity, but it has many disadvantages:

* redundancy (all code is duplicated, not just changes);
* there are no mechanisms for distributing work between multiple developers;
* there is no data on what exactly has changed (usually they write a history file with general information about the changes).

To solve some of these problems, local SLE has been developed. One of the first and most popular SLE of this type was RCS, which was developed in 1985. For each file registered in the system, it stores a complete history of changes, and for text files, an effective delta compression algorithm is used, when only the latest version and all interversion changes are stored. Such SLE solved only the first problem - data redundancy. Modern SLE can be divided into two groups: centralized and distributed.

## Centralized version control systems

The next major problem was the need to collaborate with developers on other computers. To solve it, centralized version control systems (CSCs) were created. In such systems, for example, CVS, Subversion and Perforce, there is a central server on which all files are stored under versioning control, and a number of clients who receive copies of files from it. This has been the standard for version control systems for many years.

This approach has many advantages, especially over local SLE. For example, everyone knows who and what is doing in the project. Administrators have clear control over who can do what, and, of course, it is much easier to administer the CSCS than local databases on each client.

However, with this approach, there are several serious drawbacks. The most obvious one is that a centralized server is a vulnerable point of the entire system. If the server is shut down for an hour, then developers cannot interact for an hour, and no one can save a new version of their work. If the disk with the central database is damaged and there is no backup, you lose absolutely everything — the entire history of the project, except for a few working versions preserved on users' working machines. Local version control systems are subject to the same problem: if the entire project history is stored in one place, you risk losing everything.

## Distributed version control systems

And in this situation, distributed version control systems come into play. In systems such as Git, Mercurial, Bazaar, or Darcs, clients do not just download the latest versions of files, but completely copy the entire repository (a repository, in the vulgar turnip, is a place where any data is stored and maintained). At the same time, it is possible to allocate a central repository (conditionally) to which changes from local ones will be sent and, with it, these local repositories will be synchronized. Therefore, in the case when the server through which the work was carried out “dies”, any client repository can be copied back to the server to restore the database. Every time a client picks up a fresh version of the files, he creates himself a full copy of all the data. In addition, in most of these systems, you can work with several remote repositories.
To date, the de facto standard has become a distributed version control system - GIT, but in old large projects, outdated SLE may well occur (for example, Subversion, which was popular at the time).

## GIT Basics

Almost all operations are local
To perform most operations in Git, only local files and resources are needed, i.e. usually information from other computers on the network is not needed. For example, to show the project history, Git doesn't need to download it from the server, it just reads it directly from your local repository. Therefore, you will see the story almost instantly. If you need to view the changes between the current version of the file and the version made a month ago, Git can take a month-old file and calculate the difference on the spot, instead of requesting the difference from the SLE server or downloading an old version of the file from it and making a local comparison.
In addition, working locally means that almost everything can be done without network access. If you are on a plane or on a train and want to work a little, you can safely make commits and send them as soon as the network becomes available.

Most often, data is only added to Git, Almost all actions that you perform in Git only add data to the database. It is very difficult to force the system to delete data or do something irrevocable. It is possible, as in any other SLE, to lose data that you have not saved yet, but once they are committed, it is very difficult to lose them, especially if you regularly send changes to another repository.

## Three file states

In Git, files can be in one of three states: committed, modified, and prepared. “Committed” means that the file has already been saved in your local database. Modified files include files that have changed, but have not yet been committed. Prepared files are modified files marked for inclusion in the next commit.

The standard workflow using Git looks something like this:

1. You make changes to files in your working directory.
2. Prepare files by adding their casts to the prepared files area.
3. Make a commit that takes the prepared files and puts them in the Git directory for permanent storage.


- 5/10/2024 

# Introduction to Git

- What is git: an epic save button for files and directories
- Officially: version control system


## 1.1 Getting started - About version control

- What is version control: A system that records changes to a file or set of files over time so that you recall specific version later

## 1.2 Getting started - A short history of Git

- Key
1. Speed
2. Simple Design
3. Strong support for non-linear development (thousands of parallel branches)
4. Fully distributed
5. Able to handle large proejcts like the Linux kernal efficiently (speed and data size)

## 1.3 Getting started - What is git?

- Major difference between git and any other VCS (version control system) is that other VCS store as a list of file-based changes
- Git thinks of its data like a stream of snapshots

### Git has integrity

- Everything in git is checksummed before it is stored
- Mechanism used is a SHA-1 hash ~ 40 character string composed of hexadecimal characters (0-9 and a-f)
- Git stored everything in its database not by file name but by hash values


### Git generally only adds data

- Most actions only add data to the git database

### The three states

- Modified ~ you have changed the file but have not committed to your database yet
- Staged - marked a modified file in its current version to go into your next commit snapshot
- Committed - data is safely stored in your local database
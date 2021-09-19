# git-secret
practice repo for git-secret

## install
[installation instructions](https://git-secret.io/installation)

```bash
brew install git-secret
```

## how it works

- uses gpg to encrypt 
- public key encryption
- used in teams
 - each team member has private key and public key stored
 - when member leaves, delete pub key

## usage 

0.  have gpg key pair
1.  init
```bash
git secret init
```
creates .gitsecret folder
2. add user 
```bash
git secret tell email
```
3.  add file
```bash
git secret add filename
```
this updates .gitignore
4.  encrypt added files
```bash
git secret hide
```
5.  add precommit hook
6.  reveal 
```bash 
git secret cat path/to/file
git secret reveal
```
adds files without the .secret extension, retaining the file prefix

## what if i accidently push a password

[option 1, kill the history and everything related to the file](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/removing-sensitive-data-from-a-repository)

option 2, make the repo private 

option 3, delete the repo 
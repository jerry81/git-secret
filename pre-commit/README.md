# precommit
- precommits run before the commit is attempted
- they can prevent a commit by returning 0 
- the sample git provides uses sh script
# usage
- place a file that has executable rights "pre-commit" with pre-commit script in ./.git/hooks/
- next time you try "git commit" it will run the precommit first
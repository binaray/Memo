# Git
Cheatsheet and quick setup commands

## Cloning/Committing using PA token
Set the git url to the following:
```
https://<your_token>@github.com/username/repo.git
```

## First setup
```
```

## Removing Credentials
Useful when working on temporary machines.  
### For windows:
1. Go to Credentail Manager from Control Panel
2. Delete entries under Generic Credentials
3. Remove git name and email using following commands:  
```
git config --global --unset user.name
git config --global --unset user.email
```

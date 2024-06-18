```PS
Remove-Item -Path "*" -Recurse -Force
```

still in PS is equivalent to:
```PS
rm -r -fo *
```

equivalent in Bash:
```bash
rm -rf *
```

In PS `;` = `&&`
```PS
git add .; git commit -m "Init repo"; git push
```

In PS:
```PS
New-Item -Type "Directory" new_directory_name
```

still in PS is equivalent to:
```PS
md new_directory_name
```

in PS:
```PS
New-Item new_file_name
```

still in PS:
```PS
ni new_file_name
```

Change first and any message commit message and content
Example hash: 7dh3897s
```git
git rebase --onto 7dh3897s
git add .
git commit --amend
git push --force
```

Reset to a commit (including first)
```git
git reset --hard 7dh3897s
```

Rebase interactively upto n-1 commits (first commit is not shown)
example for 3 commits after the root commit
```git
git rebase -i HEAD~3
```

Same interactive rebase, but including the very first commit
```git
git rebase -i --root
```

Resetting the author name of the commit
```git
git commit --amend --reset-author
```

Example username: joe
```git
git commit --amend --author="joe"
```

```git
git rev-list --count HEAD
```

```git
git rebase --onto HEAD~n --exec "git commit --amend --reset-author --no-edit" HEAD~n
```

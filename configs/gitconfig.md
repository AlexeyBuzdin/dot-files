##### ~/.gitconfig
```
[merge]
    tool = p4merge
    keepBackup = false
[mergetool "p4merge"]
    cmd = p4merge "$BASE" "$LOCAL" "$REMOTE" "$MERGED"
    keepTemporaries = false
    trustExitCode = false
    keepBackup = false
    prompt = false
[diff]
    external = p4diff
[push]
    default = current
[credential]
    helper = osxkeychain
[branch]
    autosetuprebase = always
[user]
    name = Alexey Buzdin
    email = alex.buzdin@gmail.com
```

##### /usr/local/bin/p4merge
```
#!/bin/sh
/Applications/p4merge.app/Contents/Resources/launchp4merge $*
```

#####  /usr/local/bin/p4diff
```
#!/bin/sh
[ $# -eq 7 ] && /usr/local/bin/p4merge "$2" "$PWD/$5"
```

# Aliases
```
alias github="echo curl -u \"'LArchaon' https://api.github.com/user/repos -d '{\"name\":\"REPO\"}'\""
alias la='ls -a'
```

# Variables
```
source /Library/Developer/CommandLineTools/usr/share/git-core/git-prompt.sh
export PS1="\[\e[1;32m\]\[\e[40m\]\u \w$(__git_ps1 ' (%s)')> \[\e[m\]\[\e[0;32m\]\[\e[40m\]"
```

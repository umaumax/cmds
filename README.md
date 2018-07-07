# commands

a filter command like diff

## how to install
```
wget https://raw.githubusercontent.com/umaumax/diff-filter/master/diff-filter.awk
mv diff-filter.awk diff-filter
chmod u+x diff-filter
mv diff-filter <path>
```

## how to use
```
alias find-dotfiles='find . -name ".*" -not -name ".git" | sed "s:\./\|^\.$::g" | grep .'
alias git-filter='diff-filter -F, -v file=<(git ls-files)'
```

```
find-dotfiles | git-filter
```

## FYI
[comm\(1\): compare two sorted files line by line \- Linux man page]( https://linux.die.net/man/1/comm )

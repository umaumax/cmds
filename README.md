# commands

a filter command like diff

## how to install
```
wget https://raw.githubusercontent.com/umaumax/diff-filter/master/diff-filter
chmod u+x diff-filter
mv diff-filter <path>
```

## how to use
```
cat $input_filepath | diff-filter -v file=$filter_filepath
```

```
alias find-dotfiles='find . -name ".*" -not -name ".git" | sed "s:\./\|^\.$::g" | grep .'
alias git-filter='diff-filter -v file=<(git ls-files)'
```

```
find-dotfiles | git-filter
```

## FYI
[comm\(1\): compare two sorted files line by line \- Linux man page]( https://linux.die.net/man/1/comm )

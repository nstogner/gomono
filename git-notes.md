# Git Notes

You can convert git repo to a shallow one:

```sh
git show-ref -s HEAD > .git/shallow
git reflog expire --expire=0
git prune
```

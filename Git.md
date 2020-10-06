# Git

### Git pull single file from Remote

```
git fetch
git checkout origin/master -- path/to/file
```

Be sure to `git fetch` to get all recent changes.
Can get path/to/file from Github (under the ellipsis button).

### git diff

```
git diff >> my.diff
```

Can save `git diff` changes onto a gist

### Find rubocop errors or offenses


`bin/rubocop` or `yarn lint` or `make test`

`bin/rubocop -a` will check all of Nitro.

`bin/rubocop -a /components/recruiting` will check a particular folder.

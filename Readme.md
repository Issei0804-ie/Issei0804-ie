# 環境構築方法

```
$ git submodule init
$ git submodule update
```

```
$ cat .git/hooks/pre-commit
#!/bin/sh
hugo
git add docs
```

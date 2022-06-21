# 環境構築方法

```
$ cat .git/hooks/pre-commit
#!/bin/sh
hugo
git add docs
```

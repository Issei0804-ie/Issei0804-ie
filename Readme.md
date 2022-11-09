# 環境構築方法

```
$ git clone --recursive git@github.com:Issei0804-ie/blog.git
```

```
$ cat .git/hooks/pre-commit
#!/bin/sh
hugo
git add docs
```

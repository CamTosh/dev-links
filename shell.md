[back](README.md)

## Shell Commands

```
$ echo 1 2 3 4 | xargs
( xargs accepts each param before pipe, like a forEach )
( more examples : http://www.cyberciti.biz/faq/linux-unix-bsd-xargs-construct-argument-lists-utility/ )
```
```
$ grep -lr '<string>'
( search across files )
```
```
$ ln -s <path/to/original> <link-name>
( create symlink )
```
```
$ ln -sfn </path/to/original> <link-name>
( update symlink )
```
```
$ rm <link-name>
( remove symlink )
```
```
$ sudo lsof -i -P 
( list running processes )
```


## git

### general resources
- atlassian : https://www.atlassian.com/git/tutorials/advanced-overview
- scm : https://git-scm.com/doc

### commands 
```
$ git checkout --ours <path-to-file>
( checkout local version during merge )
```
```
$ git checkout --theirs <path-to-file>
( checkout remote branch version during merge )
```
```
$ git diff HEAD <path-to-file>
( diff current state to state of most recent commit )
```
```
$ git checkout HEAD -- <path-to-file>
( revert file to state in most recent commit, (IF NOT STAGED - if staged see git reset HEAD ...) )
( -- indicates file, to disambiguate vs branch )
( http://stackoverflow.com/questions/692246/undo-working-copy-modifications-of-one-file-in-git )
( http://stackoverflow.com/questions/215718/reset-or-revert-a-specific-file-to-a-specific-revision-using-git )
```
```
$ git checkout origin/master -- <path-to-file>
( checkout file from upstream master )
```
```
$ git reset HEAD <path-to-file>
$ git checkout file <path-to-file>
( revert file to state in most recent commit, (IF STAGED - if NOT staged, see git checkout HEAD ...) )
```
```
$ grep -lr '<<<<<<<' . | xargs git checkout --ours
( checkout all local with merge conflicts )
```
```
$ git config --global url."https://".insteadOf git://
( change protocol )
```
```
$ git config --global credential.helper osxkeychain
( clear cached passwords )
```


ALTER TABLE `pharma`.`physicians` 
ADD COLUMN `PRE_MARKET_TRX` INT(11) NULL COMMENT '' AFTER `Account Size Segmentation`,
ADD COLUMN `POST_MARKET_TRX` INT(11) NULL COMMENT '' AFTER `PRE_MARKET_TRX`;

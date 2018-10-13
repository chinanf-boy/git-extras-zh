
# Git显示树(1)——显示提交历史的分支树

## 简介

`git-show-tree`

## 描述

显示一个内衬的装饰图形概括来自所有分支.

## 实例

将所有分支的提交历史记录作为树视图输出:

```
*   4b57684 (HEAD, develop) Merge branch upstream master.
|\
| *   515e94a Merge pull request #128 from nickl-/git-extras-html-hyperlinks
| |\
| | * 815db8b (nickl/git-extras-html-hyperlinks, git-extras-html-hyperlinks) help ronn make hyperlinks.
| * | 7398d10 (nickl/develop) Fix #127 git-ignore won't add duplicates.
| |/
| | * ab72c1e (refs/stash) WIP on develop: 5e943f5 Fix #127 git-ignore won't add duplicates.
| |/
|/|
* | 730ca89 (bolshakov) Rebase bolshakov with master
|/
* 60f8371 (origin/master, origin/HEAD, master) Merge pull request #126 from agrimaldi/fix-changelog-last-tag
* 9627780 (tag: 1.7.0) Release 1.7.0
* 2e53ff6 (tag: 1.6.0) Release 1.6.0
* bbd32d8 (tag: 1.5.1) Release 1.5.1
| * 6b6b758 (nickl/gh-pages, gh-pages) add example git-extras to gh-pages
| * 19cfd11 (origin/gh-pages) Index page
| | * 881a70e (tag: 1.5.0) Release 1.5.0
| |/
|/|
* | 4db5ee0 (tag: 1.4.0) Release 1.4.0
* | 9b0bc89 (tag: 1.3.0) Release 1.3.0
* | be49961 (tag: 1.2.0) Release 1.2.0
* | c1d2dfc (tag: 1.1.0) Release 1.1.0
* | 4a56adb (tag: 1.0.0) Release 1.0.0
* | 948308b (tag: 0.9.0) Release 0.9.0
* | 40b131d (tag: 0.8.1) Release 0.8.1
* | 391431d (tag: 0.8.0) Release 0.8.0
```

## 作者

Nick Lombard笔下<mailto:github@jigsoft.co.za>

## 报告错误

\<<https://github.com/tj/git-extras/issues>>

## 也见

\<<https://github.com/tj/git-extras>>

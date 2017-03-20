* 00.pull/push标准操作<br>
`git push <远程主机名> <本地分支名>:<远程分支名>`<br>
`git pull <远程主机名> <远程分支名>:<本地分支名>`

* 01.禁止直接向官方仓库push<br>
`git remote set-url --push origin no-pushing`

* 02.同时向两个远程仓库push<br>
`git remote set-url --add --push origin git@gitlab.com:root/XXX.git`

* 03.从远程分支检出到本地<br>
`git checkout --track -b [分支名] [远程名]/[分支名]`

* 04.文件删除/重命名<br>
`git rm git_node.md`<br>
`git mv git_node.md git_note.md`

* 05.未push时候修改最近commit message<br>
`git commit --amend `

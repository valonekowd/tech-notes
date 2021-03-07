* git checkout `develop`
* git pull origin `develop`
* git checkout `feature/abc-xyz`
* git rebase `-i HEAD~n`
* git rebase `develop`
* git add .
* git rebase `-continue`
* git push origin `feature/abc-xyz -f`
* `resolve discussions`
* git add .
* git commit -m `"discussion related messages"`
* git push origin `feature/abc-xyz`
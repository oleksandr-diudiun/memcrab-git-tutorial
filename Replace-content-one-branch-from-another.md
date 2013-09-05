Ситуация:
-------------
Если нам нужно полностью заменить содержимое master c другой ветки

Решение:
-------------
<code>
git checkout merged_branch
git merge -s ours master
git checkout master
git merge merged_branch
</code>
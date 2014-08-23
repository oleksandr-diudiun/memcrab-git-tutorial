Ситуация:
-------------
Если нам нужно полностью заменить содержимое master c другой ветки

Решение:
-------------
<code>git checkout merged_branch</code>
<code>git merge -s ours master</code>
<code>git checkout master</code>
<code>git merge merged_branch</code>

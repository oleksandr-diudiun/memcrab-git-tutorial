Ситуация:
-------------
В локальной версии не актуальные файлы или плохой merge.   
Также рядом есть важные изменения которые нужно положить на remote.
При такой ситуации git иногда может попросить reset --hard

Решение:
-------------
1. Добавляем в commit только нужные файлы и проводим push
  1. Если в коммите уже есть ненужные нам файлы обходим это с помощью [Commit-only-one-dir-when-all-files-staged](https://github.com/noon-ehos/memcrab-git-tutorial/blob/master/Commit-only-one-dir-when-all-files-staged.md "memcrab-git-tutorial")
2. Делаем git fetch.   
<code>git fetch --all</code>  
*(Эта команда скачивает последние изменения с remote без попыток merge или rebase чеголибо)*  
3. Делаем git reset.   
<code>git reset --hard origin/master</code>  
*(Эта команда сбрасывает master ветку к тому состоянию которое мы только что получили средствами fetch)*  
**Осторожно! Этот способ перетрет все локальные файлы ветки и удалить файлы невходящие в последний commit на remote**

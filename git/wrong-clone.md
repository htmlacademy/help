# Я склонировал репозиторий Академии вместо своего форка

*Проблема*: Вы склонировали не тот репозиторий и теперь не можете его запушить.

Ничего страшного, нужно просто изменить *ориджин* на ваш. Давайте посмотрим, с какими удалёнными репозиториями связан репозиторий на вашем компьютере:

```
git remote -v

origin git@github.com:htmlacademy-adaptive/6-pink.git (fetch)
origin git@github.com:htmlacademy-adaptive/6-pink.git (push)
```

Так и есть, тут репозиторий Академии. Видите `htmlacademy-adaptive`? Переименуем его из `origin` в `upstream`:

```
git remote rename origin upstream
```

И посмотрим, что получилось:

```
git remote -v

upstream git@github.com:htmlacademy-adaptive/6-pink.git (fetch)
upstream git@github.com:htmlacademy-adaptive/6-pink.git (push)
```

Теперь добавим в ориджин ваш форк. Зайдите на страницу своего форка и скопируйте адрес. Важно выбрать SSH:

![](https://cloud.githubusercontent.com/assets/529247/14052181/4910f750-f2d9-11e5-9a1d-a7aede28bc2b.png)

Теперь назначаем этот адрес ориджином:

```
git remote add origin git@github.com:meritt/6-pink.git
```

Проверим, что всё правильно:

```
git remote -v

origin  git@github.com:meritt/6-pink.git (fetch)
origin  git@github.com:meritt/6-pink.git (push)
upstream    git@github.com:htmlacademy-adaptive/6-pink.git (fetch)
upstream    git@github.com:htmlacademy-adaptive/6-pink.git (push)
```

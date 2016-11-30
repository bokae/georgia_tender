A `.gitignore` fajlban azok a fajlok vannak felsorolva, amiket nem szeretnenk felszinkronizalni. Ilyenek a notebookok checkpointjai, illetve az adat, az ugysem valtozik.

Mielott elkezdesz dolgozni:

```
git fetch upstream
git checkout master
git merge upstream/master
```

Mikor vegeztel, vagy egy munkafazist rogziteni szeretnel:

```
git add .
git commit -m "commit message"
git push
```

Amikor mar nem dolgozol tovabb, akkor annak a kerese, hogy en is beolvasszam magamnal a valtoztatasokat:

[leiras itt](https://help.github.com/articles/creating-a-pull-request-from-a-fork/)

Ha nem olvasztom be a pull requestedet, akkor akarmit commitolsz meg kesobb, az is belekerul, nem kell ujra letrehoznod.



A kovetkezo lepeseket csinaltam meg a letrehozas elott:
* https://help.github.com/articles/set-up-git/
* https://help.github.com/articles/generating-an-ssh-key/
* https://help.github.com/articles/fork-a-repo/
* https://help.github.com/articles/syncing-a-fork/

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

Ha pl. csak egy fajlt valtoztattal meg, es csak ahhoz szeretnel commit message-t fuzni, akkor akar lehet a `git add .` helyett `git add filename`-t hasznalni.


Amikor mar nem dolgozol tovabb, akkor annak a kerese, hogy en is beolvasszam magamnal a valtoztatasokat:

* https://help.github.com/articles/creating-a-pull-request-from-a-fork/

Ha nem olvasztom be a pull requestedet, akkor akarmit commitolsz meg kesobb, az is belekerul, nem kell ujra letrehoznod.

Megjegyzes: a bejelentkezeshez letrehozott ssh-kulcs nem adodik hozza automatikusan az agenthez, ugyhogy a kovetkezo ket sort irtam bele a `~/.bashrc` fajl vegere:

```
eval "$(ssh-agent -s)" >/dev/null 2>&1
ssh-add /home/bencs/.ssh/id_github >/dev/null 2>
```

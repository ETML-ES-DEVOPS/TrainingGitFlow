# Solution du labo

## git initialization

```git
git init
touch readme .gitignore
git add .
git commit -m "chore:"
```

## git flow initialization

```git
git flow init
```

## hotfix

```git
git flow hotfix start 1.0.1
mkdir hotfix
touch hotfix/test
git add .
git commit -m "test:"
touch hotfix/fix
git add .
git commit -m "fix:"
touch hotfix/refactor"
git add .
git commit -m "refactor:"
git flow hotfix finish 1.0.1
```

## start feature branches

```git
git flow feature start f1
git flow feature start f2
git flow feature start f3
```

## code and deliver feature f1

```git
git switch feature/f1
mkdir f1
touch f1/test
git add .
git commit -m "test:"
touch f1/feat
git add .
git commit -m "feat:"
touch f1/refactor
git add .
git commit -m "refactor:"
git flow feature finish
```

## deliver release

```git
git flow release start 1.1.0
mkdir release
touch release/test
git add .
git commit -m "test:"
touch release/fix
git add .
git commit -m "fix:"
touch refactor
git add .
git commit -m "refactor:"
git flow release finish 1.1.0
```

## code and deliver feature f2

```git
git switch feature/f2
mkdir f2
touch f2/test
git add .
git commit -m "test:"
touch f2/feat
git add .
git commit -m "feat:"
touch f2/fix
git add .
git commit -m "fix:"
touch f2/refactor
git add .
git commit -m "refactor:"
git flow feature finish
```

## start to code feature f3

```git
git switch feature/f3
mkdir f3
touch f3/test
git add .
git commit -m "test:"
touch f3/feat
git add .
git commit -m "feat:"
touch f3/fix
git add .
git commit -m "fix:"
touch f3/feat
git add .
git commit -m "feat:"
```

## draw git tree

```git
git log --graph --oneline --decorate --all
```

```
λ git log --graph --oneline --decorate --all
* ffe3951 (HEAD -> feature/f3) fix:                               // Question - Est-ce normal que la F3 soit "HEAD" ?
* 981d8ff feat:                                                   // Réponse dans l'issue "Erreur dans le correction"
* aaa7e62 test:                                                   // https://github.com/ETML-ES-DEVOPS/TrainingGitFlow/issues/1
| *   8e23bbf (develop) Merge branch 'feature/f2' into develop
| |\
| | * f7e7e2c refactor:
| | * 3c6339d fix:
| | * e4a5f35 feat:
| | * 435da76 test:
| |/
|/|
| *   a4697ba Merge tag '1.1.0' into develop
| |\
| | *   78a1e2d (tag: 1.1.0, main) Merge branch 'release/1.1.0'
| | |\
| | | * edf6304 refactor:
| | | * c2fd371 fix:
| | | * fd400f0 test:
| | |/
| |/|
| * | a00a275 Merge branch 'feature/f1' into develop
|/| |
| * | 136a702 refactor:
| * | 5abee9b feat:
| * | 904b00f test:
|/ /
* | 6a28c86 Merge tag '1.0.1' into develop
|\|
| * cc1b360 (tag: 1.0.1) Merge branch 'hotfix/1.0.1'
|/|
| * e441143 refactor:
| * 206e412 fix:
| * 2c234b5 test:
|/
* 3baad53 chore:
```



# Solução

1. Essa branch parte diretamente da `master` e todos os commits dessa branch devem ser transformados em
um só, então podemos usar a `master` como referencia do rebase iterativo:

```sh
git rebase -i master
```

2. Ira abrir no seu editor configurado uma tela com a lista de commits, e devalos usar os seguintes
comandos, dando `fixup` em todos os commits, menos no ultimo, que devera recever um squash
para podemos editar a mensagem em seguida. Segue o resultado desse passo:

```
pick cb17a43 commit parcial
f e840208 wip 1
f d8d0477 wip 2
f 908c1b6 wip 3
f 4a12892 wip 4
f e429b3f wip 5
f 11a7a44 wip 6
f e36be2b wip 7
f aadd4b7 wip 8
f d5f3a5a wip 9
s 20e143e mensagem do commit

# Rebase 310c80e..20e143e onto 310c80e (11 commands)
#
# Commands:
# p, pick = use commit
# r, reword = use commit, but edit the commit message
# e, edit = use commit, but stop for amending
# s, squash = use commit, but meld into previous commit
# f, fixup = like "squash", but discard this commit's log message
# x, exec = run command (the rest of the line) using shell
# d, drop = remove commit
```

3. Ao salvar e fechar o arquivo anterior abrira um novo para editar a mensagem do ultimo commit,
onde apagaremos todo o trecho abaixo com a mensagem final na descrição do exercicio:

```
# This is a combination of 11 commits.
# This is the 1st commit message:

commit parcial

# The commit message #2 will be skipped:

# wip 1

# The commit message #3 will be skipped:

# wip 2

# The commit message #4 will be skipped:

# wip 3

# The commit message #5 will be skipped:

# wip 4

# The commit message #6 will be skipped:

# wip 5

# The commit message #7 will be skipped:

# wip 6

# The commit message #8 will be skipped:

# wip 7

# The commit message #9 will be skipped:

# wip 8

# The commit message #10 will be skipped:

# wip 9

# This is the commit message #11:

mensagem do commit
```

Antes de ser salvo e fechado o arquivo devera ficar dessa forma:

```
feat(case-1): primeiro exercicio do workshop

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
#
# Date:      Mon Oct 15 19:12:15 2018 -0300
#
# interactive rebase in progress; onto 310c80e
# Last commands done (11 commands done):
#    fixup d5f3a5a wip 9
#    squash 20e143e mensagem do commit
# No commands remaining.
# You are currently rebasing branch 'case-1-solucao' on '310c80e'.
#
# Changes to be committed:
#	new file:   descricao.md
#
```

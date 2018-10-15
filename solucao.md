# Solução

Vixi, agora tem um commit no meio, não da só para dar um commit de amend! Vamos ter de apelar para o rebase!

1. Faça a alteração necessária no arquivo `descricao.md` usando seu editor preferido.

2. Crie um commit temporário com qualquer mensagem apenas para realizar o rebase interativo:

```sh
git commit -am "WIP: corrigindo descrição do exercicio"
git rebase -i master
```

3. Reorganize o seu ultimo commit temporário para ficar abaixo do primeiro commit,
e marque ele com um squash, para poder editar a mensagem de commit logo em seguida,
conforme exemplo abaixo:

```
pick 71a72e8 feat(case-666): terceiro exercicio do workshop
s 70a1d0c WIP: corrigindo descrição do exercicio
pick 85e0122 feat(novo-arquivo): arquivo para dificultar sua vida num commit intermediario

# Rebase 310c80e..70a1d0c onto 310c80e (3 commands)
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

4. Ao salvar e fechar o arquivo do git, será aberto mais um arquivo para alterar a mensagem do commit,
onde devemos alterar o seguinte conteúdo:

```
# This is a combination of 2 commits.
# This is the 1st commit message:

feat(case-666): terceiro exercicio do workshop

# This is the commit message #2:

WIP: corrigindo descrição do exercicio
```

Que devemos alterar para o nome correto do commit:

```
feat(case-3): terceiro exercicio do workshop
```

# Solução

Esse problema pode ser resolvido com um rebase interativo, porém não é necessário.
Como estamos alterando o ultimo commit da linha do tempo dessa branch,
podemos simplesmente dar um `ammed` com o comando de `commit`.

1. Primeiro altere o título do arquivo de `descricao.md` usando qualquer editor.

2. Depois rode o comando abaixo para ao mesmo tempo editar o conteúdo e a mensagem do commit:

```sh
git commit --amend -am "feat(case-2): segundo exercicio do workshop"
```
# Solução

Calma, não criemos panico! O segundo commit não sumiu, ele foi para o limbo do git, e enquanto você não limpar o histórico do git, ele estará lá!

1. Veja a lista do histórico de mudanças do seu HEAD com o comando `git reflog`:

```sh
$ git reflog
c555ba0 (HEAD -> case-5-solucao) HEAD@{0}: reset: moving to HEAD~1
e0162b6 (case-5) HEAD@{1}: checkout: moving from case-5 to case-5-solucao
```

2. Como podemos ver na lista acima, antes de rodar o comando de reset de preparação do exercicio, o hash do commit q estavamos era o `e0162b6`, então podemos agora ir resgatar esse commit:

`git checkout e0162b6`

3. Agora com nosso trabalho salvo, podemos arrumar nossa branch original:

`git checkout -B case-5`

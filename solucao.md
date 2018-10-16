# Solução

Como os dois commits são iguais, podemos pegar qualquer um dos commits e refazer nossa branch.

1. Primeiro pegue a hash de um dos dois commts com um `git log` ou `gitk`.

```sh
$ git log                                                              
commit a8bc2965b3eecd1e9f331d237ea03b5f92644e54 (HEAD -> case-4)       
Merge: 4530df8 43ef141                                                 
Author: William Grasel <d.rufos@gmail.com>                             
Date:   Tue Oct 16 08:50:55 2018 -0300                                 
                                                                       
    Merge branch 'case-4-solucao' into case-4                          
                                                                       
commit 43ef14199c9754822accfadd7adeb5ca5527fb7b (case-4-solucao)       
Author: William Grasel <d.rufos@gmail.com>                             
Date:   Tue Oct 16 08:50:07 2018 -0300                                 
                                                                       
    feat(case-4): quarto exercicio do workshop                         
                                                                       
commit 4530df8c2ce9f9d30b1b2cf63d095809eca1afc5                        
Author: William Grasel <d.rufos@gmail.com>                             
Date:   Mon Oct 15 19:12:15 2018 -0300                                 
                                                                       
    feat(case-4): quarto exercicio do workshop                         
                                                                       
commit 310c80edf86a3dea515b2c505714ddcfde134643 (origin/master, master)
Author: William Grasel <d.rufos@gmail.com>                             
Date:   Mon Oct 15 19:10:11 2018 -0300                                 
                                                                       
    commit inicial                                                     
```

2. Depois faça um checkout diretamente para um dos dois commits duplicados:

```sh
$ git checkout 4530df8c2ce9f9d30b1b2cf63d095809eca1afc5
Note: checking out '4530df8c2ce9f9d30b1b2cf63d095809eca1afc5'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by performing another checkout.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -b with the checkout command again. Example:

  git checkout -b <new-branch-name>

HEAD is now at 4530df8 feat(case-4): quarto exercicio do workshop
```

3. O git nos avisou q estamos em um estado de `detached HEAD`, o que significa que estamos conectados diretamente num commit, sem uma branch intermediária. Agora precisamos voltar para a branch `case-4` com a linha do tempo correta:

`git checkout -B case-4`

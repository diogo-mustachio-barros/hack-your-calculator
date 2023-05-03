---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Slots
---

![slots](/images/slot-machine.webp){:height="300px" .centered-image}

O jogo **Slots** simula uma máquina de slots do casino. O jogador começa com uma determinada
    quantia inicial e 

## Lógica de Jogo

1. O jogador entra no casino com 250 *dinheiros*
2. Cada vez que o jogador joga na *slot machine*, gasta 25 *dinheiros*
3. Enquanto o jogador tiver *dinheiros* para gastar:
    1. A máquina tira 3 números aleatórios entre 1 e 7
    2. Se os primeiros dois números forem iguais, o jogador recebe 25 vezes o produto desses dois
        números
    3. Se todos os números forem iguais, o jogador recebe 50 vezes o produto desses 3 números
4. O jogo termina quando o jogador chegar à bancarrota

## Código passo-a-passo 

\<Pede por ajuda no passo a passo deste exemplo\>

## Código completo

[Source](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/SLOTS/SLOTS.txt){:.btn}
[TI Program](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/SLOTS/SLOTS.8xp){:.btn}

```basic
250→M

While (M≥25)

ClrHome
0-25→G


randInt(1,7)→A
Output(4,5,A

For(X,1,1000)
End

randInt(1,7)→B
Output(4,8,B)

For(X,1,1000)
End

randInt(1,7)→C
Output(4,11,C


If A=B and B≠C
Then
 G+25*A*B→G
Else
 If A=B and B=C
 Then
  G+50*A*B*C→G
 End
End


If G≥0
Then
 Output(7,1,"Gain:")
Else
 Output(7,1,"Loss:")
End
Output(8,1,G)


M+G→M


Output(7,10,"Money:")
Output(8,10,M)

Pause 

End
ClrHome
Disp "You went bankrupt!"
```

## References
- [TI-Basic Developer - The Home Screen and Its Commands](http://tibasicdev.wikidot.com/homescreen)
- [TI-Basic Developer - The Output( Command](http://tibasicdev.wikidot.com/output)
- [TI-Basic Developer - Getting Input from the User](http://tibasicdev.wikidot.com/userinput)
- [TI-Basic Developer - Controlling Program Flow](http://tibasicdev.wikidot.com/controlflow#toc1)
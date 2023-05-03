---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Defuse the Bomb
---

![bomb](/images/bomb.webp){:height="300px" .centered-image}

O jogo **Defuse the Bomb** coloca uma bomba prestes a explodir nas mãos do jogador. Para
  sobreviver, o jogador tem de desarmar a bomba ao inserir a combinação correta de teclas 
  sem se enganar, caso contrário ***Game Over***.

## Lógica de Jogo

1. O jogo vai escolher aleatoriamente 4 botões da calculadora
2. O jogo vai mostrar ao jogador quais os 4 botões por ordem que deve carregar
3. O jogo inicia uma contagem regressiva
4. Enquanto a contagem não chega a zero, ou o jogador não desarma a bomba:
  1. O jogador deve carregar num botão da calculadora
  2. Se for o botão correto, a bomba desarma mais um *fio*
  3. Se não for o botão correto, explode de imediato


## Código passo-a-passo 

\<Pede por ajuda no passo-a-passo deste exemplo\>

## Código completo

[Source](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/DEFUSE/DEFUSE.txt){:.btn}
[TI Program](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/DEFUSE/DEFUSE.8xp){:.btn}

```basic
ClrHome

ClrList L₁
For(I,1,4)
  Repeat K≠101 and K≠35
    randInt(1,10)→L
    randInt(1,5)→C
    
    L*10+C→K
  End
  
  K→L₁(I)
End
  
Disp L₁
getKey

1→C
250→T
While C≤4 and T>0
  getKey→X

  If X=L₁(C) and X≠0
  Then
    C+1→C
  Else
    If X≠0
    Then
      0→T
    End
  End
  
  T-1→T

  Output(3,2,T)
End

ClrHome

If C>4
Then
  Disp "You win!
Else
  Disp "KABOOM!
End

Pause 
ClrHome
```

## Referências
- [TI-Basic Developer - The Home Screen and Its Commands](http://tibasicdev.wikidot.com/homescreen)
- [TI-Basic Developer - The Output( Command](http://tibasicdev.wikidot.com/output)
- [TI-Basic Developer - Controlling Program Flow](http://tibasicdev.wikidot.com/controlflow#toc1)
- [TI-Basic Developer - Operators](http://tibasicdev.wikidot.com/operators)
- [TI-Basic Developer - Getting Input from the User](http://tibasicdev.wikidot.com/userinput)
- [TI-Basic Developer - Lists and Their Commands](http://tibasicdev.wikidot.com/lists)
- [Programming the TI-83 Plus/TI-84 Plus - Chapter 6. Advanced input and events](https://livebook.manning.com/book/programming-the-ti-83-plus-ti-84-plus/chapter-6/69)
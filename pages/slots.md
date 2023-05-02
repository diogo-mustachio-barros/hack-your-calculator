---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Game - Slots
---

![slots](/images/slot-machine.webp){:height="300px" .centered-image}

## Lógica de Jogo
**TODO**

## Código passo-a-passo 
**TODO**

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
  G+25*A*B*C→G
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
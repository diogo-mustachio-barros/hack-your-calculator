---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Game - Guessing Game
---

![thinking](/images/thinking.webp){:height="280px" .centered-image}



## Lógica de Jogo
**TODO**

## Código passo-a-passo 
**TODO**

## Código completo

[Source](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/GUESS/GUESS.txt){:.btn}
[TI Program](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/GUESS/GUESS.8xp){:.btn}

```basic
ClrHome

randInt(1,100)→N

Disp "Guess a number"

For(T,1,10)
  Input "Guess?",G
  
  If N=G:Then
    Disp "You've got it!","Guesses:",T
    Pause 
    Return
  Else
    If N>G:Then
      Disp "Higher…"
    Else
      Disp "Lower…"
    End
  End
End

Disp "You lose!","The number was:",N
```

## References
- [TI-Basic Developer - The Home Screen and Its Commands](http://tibasicdev.wikidot.com/homescreen)
- [TI-Basic Developer - Getting Input from the User](http://tibasicdev.wikidot.com/userinput)
- [TI-Basic Developer - Controlling Program Flow](http://tibasicdev.wikidot.com/controlflow#toc1)
- [TI-Basic Developer - The randInt( Command](http://tibasicdev.wikidot.com/randint)

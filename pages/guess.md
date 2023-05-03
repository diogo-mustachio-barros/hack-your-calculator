---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Guessing Game
---

![thinking](/images/thinking.webp){:height="280px" .centered-image}

O jogo **Guessing Game** desafia o jogador a adivinhar um número aleatório entre 1 e 100. O
    jogador tem 10 tentativas para adivinhar o número. Sempre que errar é dada uma pista:
    'Higher' se o número for maior, ou 'Lower' se o número for menor.

## Lógica de Jogo

1. O jogo escolhe um número aleatoriamente
2. O jogo pergunta um máximo de 10 vezes ao utilizador por um palpite
    1. Se o jogador acertar, vence o jogo
    2. Se o palpite for maior que o número, o jogo diz 'Higher...'
    3. Se o palpite for menor que o número, o jogo diz 'Lower...'
3. Se o jogador não adivinhar em 10 tentativas, perde o jogo (e a resposta certa é mostrada)

## Código passo-a-passo 
**TODO**

## Código completo

[Source](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/GUESS/GUESS.txt){:.btn}
[TI Program](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/GUESS/GUESS.8xp){:.btn}

```basic
ClrHome

randInt(1,100)→N

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

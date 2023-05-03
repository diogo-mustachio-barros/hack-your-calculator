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

Começamos por limpar o ecrã inicial da calculadora.

```basic
ClrHome
```

E retiramos um número aleatório entre 1 e 100, que guardamos depois numa variável N.

```basic
randInt(1,100)→N
```

A partir daqui estamos prontos para dar 10 tentativas ao jogador através de um ciclo `For`.
  Os ciclos sâo a forma de os programas **repetirem** um conjunto de instruções. Neste caso,
  queremos repetir **10 vezes** perguntar ao jogador por um palpite.

```basic
For(T,1,10)
  <código a repetir>
End
```

Em cada iteração do ciclo, isto é, cada vez uma das 10 vezes que o ciclo vai ser executado,
  vamos ter na variável `T`, a iteração em que vamos, ou no nosso caso, qual é o número da 
  tentativa em que o jogador vai.

Para perguntarmos ao utilizador por um palpite usamos o comando `Input "Guess?", G` que vai
  mostrar ao jogador `Guess?` na calculadora e depois vai deixar que este introduza o seu 
  palpite, sendo depois esse palpite guardado na variável `G`.

```basic
  Input "Guess?",G
```

Depois de termos o palpite do jogador `G` e o número aleatório `N`, podemos então comparar
  os dois e ver se:
- o jogador acertou, e por isso deve ganhar
- o número é maior que o palpite, e por isso deve dizer-se que é maior
- o número é menor que o palpite, e por isso deve dizer-se que é menor

Em programação isto corresponde a termos condicionais do género, 
  `se <isto> então <faz isto> caso contrário <faz aquilo>`. Na calculadora fazemos isto com 
  `If <condition> Then <code> Else <code> End`.

```basic
  If N=G
  Then
    <o jogador venceu>
  Else
    If N>G
    Then
      <o número é maior que o palpite>
    Else
      <o número é menor que o palpite>
    End
  End
```

Para mostrar mensagens ao jogador usamos o comando `Disp `. No caso de vitória,
  mostramos a mensagem, juntamente com o número de tentativas que o jogador precisou,
  pausamos o jogo com `Pause `(para que o jogador se possa bajular na glória da vitória),
  e terminamos o jogo com o comando `Return`.

```basic
    Disp "You've got it!","Guesses:",T
    Pause 
    Return
```

Nos casos em que o jogador nâo acerta, mostramos a respetiva mensagem com `Disp "Higher…"` ou
  `Disp "Lower…"`.

Entâo e se não acertar dentro das 10 tentativas que tem? Nesse caso, depois do nosso ciclo `For`,
  adicionamos a mensagem de derrota. Sabemos que se o jogador checgou até aqui foi porque esgotou 
  as suas tentativas sem acertar.

```basic
Disp "You lose!","The number was:",N
```

## Código completo

[Source](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/GUESS/GUESS.txt){:.btn}
[TI Program](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/GUESS/GUESS.8xp){:.btn}

```basic
ClrHome

randInt(1,100)→N

For(T,1,10)
  Input "Guess?",G
  
  If N=G
  Then
    Disp "You've got it!","Guesses:",T
    Pause 
    Return
  Else
    If N>G
    Then
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

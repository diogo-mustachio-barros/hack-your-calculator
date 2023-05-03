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

Começamos por dar ao jogador 250 *dinheiros* ao jogador, que ficam guardados na variável `M`.

```basic
250→M
```

Queremos que enquanto o jogo continue enquanto o jogador tiver *dinheiros* para continuar a 
    apostar (cada aposta vai custar 25). Para tal vamos usar um ciclo `While` que vai 
    repetir-se enquanto a nossa condição for verdadeira (o jogador ter dinheiro para apostar).

```basic
While M≥25
  <código a repetir>
End
```

Uma vez que dentro do ciclo, o jogador já terá apostado, vamos guardar o saldo dele (por 
    enquanto negativo) na variável `G`.

```basic
  ClrHome
  0-25→G
```

(E aproveitamos para limpar o ecrã da nossa máquina)

A nossa *slot machine* vai gerar 3 números aleatórios entre 1 e 7 e vai mostrar ao jogador
    com algum intervalo de tempo (para o suspense). Para isto vamos combinar a utilização do
    `randInt()` para gerar números aleatórios, com o `Output(` para mostrar informação ao 
    jogador num local específico da calculadora e um ciclo `For` para fazer a calculadora
    esperar um pouco.

Normalmente os ciclos `For` não são usados para fazer compassos de espera, no entanto, como
    a calculadora é uma tartaruga comparada com o carro de Fórmula 1 que são os processadores,
    contar de 1 até 100 demora o tempo suficiente para o efeito que queremos.

```basic
  randInt(1,7)→A
  Output(4,5,A

  For(X,1,1000)
  End
```

Repetimos isto 3 vezes para termos todos os números da *slot machine* (guardados nas variáveis 
    `A`, `B` e `C`), resultando em:

```basic
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
```

Por fim só temos de verificar se temos uma combinação de 2 ou 3 números seguidos. Fazemos isto
    com a ajuda de **condicionais** do género `se <isto> então <faz isto> caso contrário <faz aquilo>`
    , que a calculadora fazemos com `If <condition> Then <code> Else <code> End`.

```basic
  If A=B and B≠C
  Then
    <acertou 2 números>
  Else
    If A=B and B=C
    Then
      <acertou 3 números>
    End
  End
```

Se acertou 2 números, então damos de prémio 25 vezes o produto desses 2 números, e se acertar 3 números
    damos de prémio 50 vezes o produto desses 3 números. Adicionamos este prémio à nossa variável `G` 
    que guarda os ganhos (ou perdas) que o jogador tem numa jogada. Ficamos com:

```basic
  If A=B and B≠C
  Then
    G+25*A*B→G
  Else
    If A=B and B=C
    Then
      G+50*A*B*C→G
    End
  End
```

O mais importante está feito! Apenas precisamos de mostrar ao jogador quanto ganhou
    (ou perdeu):
    
```basic
  If G≥0
  Then
    Output(7,1,"Gain:")
  Else
    Output(7,1,"Loss:")
  End
  Output(8,1,G)
```
    
E quanto dinheiro que tem de momento, primeiro atualizamos o seu valor, que está guardado na 
    varíavel `M`, e mostramos:
```basic
  M+G→M

  Output(7,10,"Money:")
  Output(8,10,M)
```

Pausamos o jogo para o jogador ver o que saiu e o seu dinheiro com o comando `Pause `, depois
    do qual o jogo continua até que o dinheiro acabe!

No fim do jogo, avisamos que o jogador ficou na bancarrota.
```basic
ClrHome
Disp "You went bankrupt!"
```

**A casa ganha sempre** ;)

## Código completo

[Source](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/SLOTS/SLOTS.txt){:.btn}
[TI Program](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/hack-your-calculator/hack-your-calculator.github.io/blob/master/programs/SLOTS/SLOTS.8xp){:.btn}

```basic
250→M

While M≥25

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
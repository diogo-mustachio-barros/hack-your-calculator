---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

## Guessing Game
![thinking](images/thinking.webp){:height="280px" .centered-image}

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


## Slot Machine
![slots](images/slot-machine.webp){:height="300px" style="display: block; margin-left: auto margin-right: auto}

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


## Defuse the bomb
![bomb](images/bomb.webp){:height="300px" style="display: block; margin-left: auto margin-right: auto}
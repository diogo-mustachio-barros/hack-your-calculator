---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Game - Defuse the Bomb
---

![bomb](/images/bomb.webp){:height="300px" .centered-image}

```basic
ClrHome

ClrList L₁
For(I,1,3)
  Repeat K≠101
    randInt(1,10)→L
    randInt(1,5)→C
    
    L*10+C→K
  End
  
  K→L₁(I)
End
  
Disp L₁

1→C
500→T
While C≤3 and T>0
  getKey→X

  If X=L₁(C)
    C+1→C
  End
  
  T-1→T
  
  Output(5,7,T)
  
  For(I,1,100)
  End
End
```

## References
- [TI-Basic Developer - Getting Input from the User](http://tibasicdev.wikidot.com/userinput)
- [Programming the TI-83 Plus/TI-84 Plus - Chapter 6. Advanced input and events](https://livebook.manning.com/book/programming-the-ti-83-plus-ti-84-plus/chapter-6/69)
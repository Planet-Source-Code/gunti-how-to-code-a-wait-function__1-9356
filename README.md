<div align="center">

## How to code a "wait" function\.\.\.


</div>

### Description

This code shows you, how you can easily implement a "wait" function into visual-basic...
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[gunti](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/gunti.md)
**Level**          |Beginner
**User Rating**    |3.0 (18 globes from 6 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VB Script, ASP \(Active Server Pages\) 
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__1-43.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/gunti-how-to-code-a-wait-function__1-9356/archive/master.zip)





### Source Code

```
'place a timer-controle & 3 Labels into your app.
Public Sub Wait(seconds)
  Timer1.Enabled = True
  Me.Timer1.Interval = 1000 * seconds
  While Me.Timer1.Interval > 0
  DoEvents
  Wend
  Timer1.Enabled = False
End Sub
Private Sub Timer1_Timer()
  Timer1.Interval = 0
End Sub
Private Sub Command1_Click()
  Label1.Caption = "1"
  Wait (5)
  Label2.Caption = "2"
  Wait (5)
  Label3.Caption = "3"
End Sub
```


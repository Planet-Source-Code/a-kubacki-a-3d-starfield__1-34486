<div align="center">

## a 3d starfield\!\!\!\!\!\!\!


</div>

### Description

3d starfield
 
### More Info
 
all you need is a timer control, and a back background for the form

stars!!!

extreme obsessiong with putting this on every platform possible, calculators, etc...


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[A Kubacki](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/a-kubacki.md)
**Level**          |Beginner
**User Rating**    |3.9 (27 globes from 7 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__1-46.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/a-kubacki-a-3d-starfield__1-34486/archive/master.zip)





### Source Code

```
Dim X(1000) As Integer
Dim Y(1000) As Integer
Dim z(1000) As Integer
Dim xv(1000) As Long
Dim yv(1000) As Long
Dim sss As Long
Dim numstarz As Integer
Dim colora As Long
Dim i, j, k, m As Integer
Private Sub Form_KeyDown(KeyCode As Integer, Shift As Integer)
If KeyCode = vbKeyEscape Then
Form1.Hide
End If
End Sub
Private Sub Form_Load()
Timer1.Enabled = True
Timer1.Interval = 1
Form1.Show
numstarz = 250
Form1.Enabled = True
init
End Sub
Private Sub init()
For i = 1 To numstarz
X(i) = Rnd() * 1000 - 500
Y(i) = Rnd() * 1000 - 500
z(i) = 1 + Rnd() * 256
Next i
End Sub
Private Sub drawptz()
Dim asdf As Integer
sss = 40 * ScaleWidth / 1000
For k = 1 To numstarz
xv(k) = X(k) * 3 * sss / ((z(k)))
yv(k) = Y(k) * 3 * sss / ((z(k)))
Next k
For j = 1 To numstarz
z(j) = z(j) - 1
  If z(j) < 40 Then
    z(j) = 200 + Rnd() * 40
  End If
Next j
For i = 1 To numstarz
asdf = 256 - z(i)
colora = RGB(asdf, asdf, asdf)
PSet (xv(i) + ScaleWidth / 2, yv(i) + ScaleHeight / 2), colora
Next i
End Sub
Private Sub Timer1_Timer()
 Form1.Enabled = True
 Timer1.Enabled = True
For m = 1 To 10
Cls
drawptz
Next m
End Sub
```


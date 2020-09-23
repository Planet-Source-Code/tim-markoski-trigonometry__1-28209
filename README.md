<div align="center">

## Trigonometry


</div>

### Description

Simplifies the use of the most common Trig Functions (Sine, Cosine, Tangent) and their Inverse Functions (ArcSine, ArcCosine, ArcTangent).

The native VB Trig functions require the conversion from degrees to radians or vice-versa.

These functions eliminate that need.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tim Markoski](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tim-markoski.md)
**Level**          |Beginner
**User Rating**    |4.7 (33 globes from 7 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VBA MS Access, VBA MS Excel
**Category**       |[Math/ Dates](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/math-dates__1-37.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tim-markoski-trigonometry__1-28209/archive/master.zip)





### Source Code

```
Attribute VB_Name = "TRIGONOMETRY"
Option Explicit
Public Function Sine(p_dblVal As Double) As Double
  ' Comments :
  ' Parameters: p_dblVal -
  ' Returns  : Double -
  ' Modified :
  '
  ' -------------------------
  'Degree Input Radian Output
  On Error GoTo PROC_ERR
  Dim dblPi      As Double
  Dim dblRadian    As Double
  ' xx Calculate the value of Pi.
  dblPi = 4 * Atn(1)
  ' xx To convert degrees to radians,
  '  multiply degrees by Pi / 180.
  dblRadian = dblPi / 180
  p_dblVal = Val(p_dblVal * dblRadian)
  Sine = Sin(p_dblVal)
PROC_EXIT:
  Exit Function
PROC_ERR:
  Sine = 0
  MsgBox Err.Description, vbExclamation
  Resume PROC_EXIT
End Function
Public Function Cosine(p_dblVal As Double) As Double
  ' Comments :
  ' Parameters: p_dblVal -
  ' Returns  : Double -
  ' Modified :
  '
  ' -------------------------
  'Degree Input Radian Output
  On Error GoTo PROC_ERR
  Dim dblPi      As Double
  Dim dblRadian    As Double
  ' xx Calculate the value of Pi.
  dblPi = 4 * Atn(1)
  ' xx To convert degrees to radians,
  '  multiply degrees by Pi / 180.
  dblRadian = dblPi / 180
  p_dblVal = Val(p_dblVal * dblRadian)
  Cosine = Cos(p_dblVal)
PROC_EXIT:
  Exit Function
PROC_ERR:
  Cosine = 0
  MsgBox Err.Description, vbExclamation
  Resume PROC_EXIT
End Function
Public Function Tangent(p_dblVal As Double) As Double
  ' Comments :
  ' Parameters: p_dblVal -
  ' Returns  : Double -
  ' Modified :
  '
  ' -------------------------
  'Degree Input Radian Output
  On Error GoTo PROC_ERR
  Dim dblPi      As Double
  Dim dblRadian    As Double
  ' xx Calculate the value of Pi.
  dblPi = 4 * Atn(1)
  ' xx To convert degrees to radians,
  '  multiply degrees by Pi / 180.
  dblRadian = dblPi / 180
  p_dblVal = Val(p_dblVal * dblRadian)
  Tangent = Tan(p_dblVal)
PROC_EXIT:
  Exit Function
PROC_ERR:
  Tangent = 0
  MsgBox Err.Description, vbExclamation
  Resume PROC_EXIT
End Function
Public Function ArcSine(p_dblVal As Double) As Double
  ' Comments :
  ' Parameters: p_dblVal -
  ' Returns  : Double -
  ' Modified :
  '
  ' -------------------------
  'Radian Input Degree Output
  On Error GoTo PROC_ERR
  Dim dblSqr     As Double
  Dim dblPi       As Double
  Dim dblDegree    As Double
  ' xx Calculate the value of Pi.
  dblPi = 4 * Atn(1)
  ' xx To convert radians to degrees,
  '   multiply radians by 180/pi.
  dblDegree = 180 / dblPi
  p_dblVal = Val(p_dblVal)
  dblSqr = Sqr(-p_dblVal * p_dblVal + 1)
  ' xx Prevent division by Zero error
  If dblSqr = 0 Then
    dblSqr = 1E-30
  End If
  ArcSine = Atn(p_dblVal / dblSqr) * dblDegree
PROC_EXIT:
  Exit Function
PROC_ERR:
  ArcSine = 0
  MsgBox Err.Description, vbExclamation
  Resume PROC_EXIT
End Function
Public Function ArcCosine(p_dblVal As Double) As Double
  ' Comments :
  ' Parameters: p_dblVal -
  ' Returns  : Double -
  ' Modified :
  '
  ' -------------------------
  'Radian Input Degree Output
  On Error GoTo PROC_ERR
  Dim dblSqr     As Double
  Dim dblPi       As Double
  Dim dblDegree    As Double
  ' xx Calculate the value of Pi.
  dblPi = 4 * Atn(1)
  ' xx To convert radians to degrees,
  '   multiply radians by 180/pi.
  dblDegree = 180 / dblPi
  p_dblVal = Val(p_dblVal)
  dblSqr = Sqr(-p_dblVal * p_dblVal + 1)
  ' xx Prevent division by Zero error
  If dblSqr = 0 Then
    dblSqr = 1E-30
  End If
  ArcCosine = (Atn(-p_dblVal / dblSqr) + 2 * Atn(1)) * dblDegree
PROC_EXIT:
  Exit Function
PROC_ERR:
  ArcCosine = 0
  MsgBox Err.Description, vbExclamation
  Resume PROC_EXIT
End Function
Public Function ArcTangent(p_dblVal As Double) As Double
  ' Comments :
  ' Parameters: p_dblVal -
  ' Returns  : Double -
  ' Modified :
  '
  ' -------------------------
  'Radian Input Degree Output
  On Error GoTo PROC_ERR
  Dim dblPi      As Double
  Dim dblDegree    As Double
  ' xx Calculate the value of Pi.
  dblPi = 4 * Atn(1)
  ' xx To convert radians to degrees,
  '   multiply radians by 180/pi.
  dblDegree = 180 / dblPi
  p_dblVal = Val(p_dblVal)
  ArcTangent = Atn(p_dblVal) * dblDegree
PROC_EXIT:
  Exit Function
PROC_ERR:
  ArcTangent = 0
  MsgBox Err.Description, vbExclamation
  Resume PROC_EXIT
End Function
```


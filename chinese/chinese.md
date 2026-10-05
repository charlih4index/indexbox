---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
kernelspec:
  display_name: Python 3
  language: python
  name: python3
title: Chinese
abstract: ""
authors:
  - name: Author Name
exports:
  - format: typst
    template: lapreprint-typst
    output: _build/exports/typst/
---

# Chinese

## Zhuyin AKA. BoPoMoFo

| 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 | 19 | 20 | 21 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| [ㄅ](u3105.md) | [ㄆ](u3106.md) | [ㄇ](u3107.md) | [ㄈ](u3108.md) | [ㄉ](u3109.md) | [ㄊ](u310a.md) | [ㄋ](u310b.md) | [ㄌ](u310c.md) | [ㄍ](u310d.md) | [ㄎ](u310e.md) | [ㄏ](u310f.md) | [ㄐ](u3110.md) | [ㄑ](u3111.md) | [ㄒ](u3112.md) | [ㄓ](u3113.md) | [ㄔ](u3114.md) | [ㄕ](u3115.md) | [ㄖ](u3116.md) | [ㄗ](u3117.md) | [ㄘ](u3118.md) | [ㄙ](u3119.md) |
| **1** | **2** | **3** |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| [ㄧ](u3127.md) | [ㄨ](u3128.md) | [ㄩ](u3129.md) |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **1** | **2** | **3** | **4** | **5** | **6** | **7** | **8** | **9** | **10** | **11** | **12** | **13** |  |  |  |  |  |  |  |  |
| [ㄚ](u311a.md) | [ㄛ](u311b.md) | [ㄜ](u311c.md) | [ㄝ](u311d.md) | [ㄞ](u311e.md) | [ㄟ](u311f.md) | [ㄠ](u3120.md) | [ㄡ](u3121.md) | [ㄢ](u3122.md) | [ㄣ](u3123.md) | [ㄤ](u3124.md) | [ㄥ](u3125.md) | [ㄦ](u3126.md) |  |  |  |  |  |  |  |  |

Total possible pronuciation = (((**3**+1)*(**13**+1)*(**21**+1))*5-(1*1*1*5) = ((4*14)*22)*5-5 = 6155

### Zhuyin table

[ZhuyinTable.md](ZhuyinTable.md) vs. [ZhuyinTable.html](ZhuyinTable.html) vs. [ZhuyinTable.xlsx](ZhuyinTable.xlsx)

### A Chinese character eq2 the Zhuyin

| Zhuyin | Chinese character | meaning | pronounce | others |
|--------| ------------------|---------|-----------|--------|
| **A** | **B** | **Tag#1** | **Tag#2** | **Tag#3** |
| ㄅㄚ | 八 | 阿拉伯數字8 | bā | 大寫為捌 |
| ㄅㄚ | 巴 | 符號bar | bā | 大氣壓力的單位 |

```
詞類 (word class) AKA. 詞性
英語中有八個詞性：
名詞、代詞、形容詞、動詞、副詞、介詞、連詞、感嘆詞、綴詞。
[名],[代],[形],[動],[副],[介],[連],[感],[綴]
中文多了一個詞性：
綴詞。
[綴]

[名] = 名詞
[代] = 代詞
[形] = 形容詞
[動] = 動詞
[副] = 副詞
[介] = 介詞
[連] = 連詞
[感] = 感嘆詞
[擬] = 擬聲詞
[綴] = 綴詞

"[名]
1.介於七與九之間的自然數。如：「六、七、八、九……」。大寫作「捌」，阿拉伯數字作「8」。
2.姓。如漢代有西域人八滑。
3.二一四部首之一。
[形]
表示數量是八的。如：「八字」、「八方」。
[副]
形容多數或多方面。如：「四通八達」。
（「八」字口語連用在去聲字前讀成陽平，如：「八號」、「八拜」。）"
```

```
Help me to update the uploaded Excel file named "SingleWord.xlsx" on Github.com/charlih4index/indexbox/Chinese/ to extract column V labeled "釋義" content's "[名],[代],[形],[動],[副],[介],[連],[感], or[擬]" into column O labeled "詞類 (word class)" and insert a new whole row below the checked row. So, if column V labeled "釋義" content has 3 sections  "[名], [形], or [副]", then the Excel will insert 3 new rows then. Stay untouched, and new rows added below. And the new row's column V labeled "釋義" content to just keep its [] .... and delete all others' []..... For example, if found [名] sentence here, then remove all other [] likes [形] sentence here [動]sentence here etc.
```

Paste this into Excel → VBA → Module:

```
Sub ExtractWordClasses_InsertRows()

    Dim ws As Worksheet
    Dim lastRow As Long, r As Long
    Dim text As String
    Dim classes As Variant
    Dim c As Variant
    Dim count As Long
    Dim i As Long
    Dim foundClasses As Collection
    Dim sectionText As String
    Dim startPos As Long, endPos As Long
    
    Set ws = ActiveSheet
    lastRow = ws.Cells(ws.Rows.Count, "V").End(xlUp).Row
    
    ' Word class tags to detect
    classes = Array("[名]", "[代]", "[形]", "[動]", "[副]", "[介]", "[連]", "[感]", "[擬]")
    
    ' Process bottom → top
    For r = lastRow To 2 Step -1
        
        text = ws.Cells(r, "V").Value
        
        Set foundClasses = New Collection
        
        ' Find all tags present in column V
        For Each c In classes
            If InStr(text, c) > 0 Then
                foundClasses.Add c
            End If
        Next c
        
        count = foundClasses.Count
        
        If count > 0 Then
            
            ' Insert N new rows below original row
            ws.Rows(r + 1).Resize(count).Insert Shift:=xlDown
            
            ' For each tag found, create a new row
            For i = 1 To count
                
                ' Copy entire row (A to V)
                ws.Range(ws.Cells(r, 1), ws.Cells(r, 22)).Copy _
                    Destination:=ws.Range(ws.Cells(r + i, 1), ws.Cells(r + i, 22))
                
                ' Write the word class into column O
                ws.Cells(r + i, "O").Value = foundClasses(i)
                
                ' Extract only the section belonging to this tag
                startPos = InStr(text, foundClasses(i))
                
                If startPos > 0 Then
                    ' Find next "[" after this tag
                    endPos = InStr(startPos + 1, text, "[")
                    
                    If endPos = 0 Then
                        ' No more sections → take until end of text
                        sectionText = Mid(text, startPos)
                    Else
                        ' Extract only this section
                        sectionText = Mid(text, startPos, endPos - startPos)
                    End If
                End If
                
                ' Write cleaned definition into column V
                ws.Cells(r + i, "V").Value = Trim(sectionText)
                
            Next i
            
        End If
        
    Next r

End Sub
```

## Pinyin AKA. romanization

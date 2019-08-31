```
EXPORT 读取已知点()
BEGIN
LOCAL i,ch,pointNames:=Points.A:A;
LOCAL pointN:=Points.B:B;
LOCAL pointE:=Points.C:C;
LOCAL pointH:=Points.D:D;

CHOOSE(ch,"请选择一个已知点",pointNames);

IF ch>0 THEN
PRINT();
PRINT("点名:"+pointNames[ch]);
PRINT("N:"+pointN[ch]);
PRINT("E:"+pointE[ch]);
PRINT("H:"+pointH[ch]);
END;
END;
```

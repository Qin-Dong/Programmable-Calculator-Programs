```
EXPORT UG()
BEGIN
LOCAL pax,pay,pah,pbx,pby,pbh;
LOCAL px,py,ph,ch;
INPUT({pax,pay,pah,pbx,pby,pbh},"请输入直线上的两个已知点坐标：",
{"直线A点X：","直线A点Y：","直线A点H：","直线B点X：","直线B点Y：","直线B点H："},
{"请输入直线A点X：","请输入直线A点Y：","请输入直线A点H：","请输入直线B点X：","请输入直线B点Y：","请输入直线B点H："});

CHOOSE(ch,"请选择待算点计算方式","由X计算Y、H","由Y计算X、H","由H计算X、Y");

REPEAT

CASE
IF ch==1 THEN
INPUT(px,"请输入待算点X:","待算点X:","待算点X:",0);
py:=finvalue(pax,pay,pbx,pby,px);
ph:=finvalue(pax,pah,pbx,pbh,px);
END;

IF ch==2 THEN
INPUT(py,"请输入待算点Y:","待算点Y:","待算点Y:",0);
px:=finvalue(pay,pax,pby,pbx,py);
ph:=finvalue(pay,pah,pby,pbh,py);
END;

IF ch==3 THEN
INPUT(ph,"请输入待算点H:","待算点H:","待算点H:",0);
px:=finvalue(pah,pax,pbh,pbx,ph);
py:=finvalue(pah,pay,pbh,pby,ph);
END;

DEFAULT
px:=-1;
py:=-1;
ph:=-1;
END;

IF  px≠-1 AND py≠-1 AND ph≠-1 THEN
PRINT("直线A点："+ROUND(pax,3)+","+ ROUND(pay,3)+","+ ROUND(pah,3));
PRINT("直线B点："+ ROUND(pbx,3)+","+ ROUND(pby,3)+","+ ROUND(pbh,3));
PRINT("待算点 X="+ ROUND(px,3)+" Y="+ ROUND(py,3)+" H="+ ROUND(ph,3));
WAIT();
END;

UNTIL px==-1 OR py==-1 OR ph==-1;

//MSGBOX("覃东两河口水电站");

END;
```

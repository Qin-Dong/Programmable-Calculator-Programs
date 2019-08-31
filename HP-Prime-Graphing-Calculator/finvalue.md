```
EXPORT finvalue(xa,ya,xb,yb,xp)
BEGIN
RETURN ya+(yb-ya)*(xp-xa)/(xb-xa);
END;
```

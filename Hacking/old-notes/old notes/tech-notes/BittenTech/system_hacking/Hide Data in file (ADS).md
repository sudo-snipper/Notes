* ### in NTFS there is Alternative data stream(ADS) which keep metadata or info about file

---

## hide data

1. use this ADS to hide data , this is used to hide malicous files
2. in cmd
```
echo "data" visbile.txt:hidden.txt
```

> only visible.txt will show not hidden.txt

3. to view data

```
notepad visible.txt:hidden.txt
```

---

## hide EXE

> use full path locations

* hide
```
type C:\windows\notepad.exe > visibile.txt:hidden.exe
```
> it wil hide notepad.exe  in ADS of visible of exe

* run
```
start C:\windows\visbile.txt:hidden.exe 
```

---
## ADS in directory

```
echo "hii" > :hidden.txt

```

> make ADS to curret directory

## Find ADS of files
```
dir /r
```
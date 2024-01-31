# Quickly delete all local feature branches

in Windows

```dos
for /f "tokens=*" %b in ('git branch ^| findstr /r /v "^\* master"') do git branch -D %b
```

in Unix/Mac

```bash
git branch | grep -v "master" | xargs git branch -D
```

## General

```
•
“”
’
‘’
«»
–
︱
┌─┐╔═╗│
╚═╝└─┘║
→
➜
➔
```

## Double whitespaces

In some scripts, there is a known practice of adding **two whitespaces** after the end of a sentence (particularly after these punctuation marks: `. ? !`) instead of one.

Why? **For better readability!**

You can use this regular expression to find single whitespaces to replace *(CASE-INSENSITIVE!!!!)*:

```regexp
(?<=(?<! vs|^int|^ext)[\.\?!])( )(?! |•)
```

If you’re careful about **ellipses**, use this expression:

```regexp
(?<=(?<! vs|^int|^ext|\.)[\.\?!])( )(?! |•)
```

### Unnecessary whitespaces

You can fix unnecessary whitespaces using this expression *(CASE-SENSITIVE!!!!)*:

```regexp
(?<=\.?\.\.)(  )(?=[^A-Z]|(I ))
```

Double-check with this expression *(CASE-SENSITIVE as well)*:

```regexp
(?<=\.?\.\.)(  )
```
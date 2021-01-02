# How to Execute a Script

Here are the contents of a Python script, named `script.py`:
```
print('hello')
```

You can run this on the command line by giving it as an argument to the `python` command:
```
$ python script.py
hello
$
```

But you can't run it by itself:
```
$ script.py
bash: script.py: command not found
$
```

Our command line interpreter (CLI) is called bash.
There are similar ones named sh, ksh, tcsh, etc.
The CLI expects you to enter a command.
So it treats `script.py` as a command.
But the CLI is not allowed to execute a command that lives in the current directory unless you explicitly tell it to look there.
That's a security precaution, but we won't discuss the details, here.
To tell the CLI to look in the current directory:
```
$ ./script.py
```

The dot means, 'current directory'.
The slash separates a directory from a filename (or from another directory).
Now, the CLI can find the command:
```
$ ./script.py
bash: ./script.py:  Permission denied
$
```

This error is related to the permissions on the file, but we won't discuss the details, here.
To add the needed permission:
```
$ chmod u+x script.py
```

Now the script has the correct permission to be run by the user.
```
$ ./script.py
./script.py: line 1: syntax error near unexpected token `'hello''
./script.py: line 1: `print('hello')'
$
```

Before, we used the file as an argument to the `python` command.
The CLI knew what to do with `python`.
And Python knew what to do with the file contents.
But the CLI doesn't know what to do with the contents of the file.
There is a special way to tell the CLI how to treat the file.
That is to add a shebang as the first line of the file.
So, the new script file is:
```py
#!/usr/bin/env python

print('hello')
```

And now:
```
$ ./script.py
hello
$
```



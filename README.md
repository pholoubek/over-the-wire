# over-the-wire

Personal Notes and Solutions For OverTheWire: Bandit

I won't publish answers as long as I don't have need to. Rather will focus on writing down relevant comments and observations.

## Level 0

[link](https://overthewire.org/wargames/bandit/bandit0.html)

```
ssh <username>@<host> -p <port_num>

ls

cat <filename>
```

## Level 1

[link](https://overthewire.org/wargames/bandit/bandit2.html)

Name of the game is **dashed filename** and how to operate with it.
We can either specify the exact location and use **cat** or use **redirection** into the **cat** cmd.

## Level 2

[link](https://overthewire.org/wargames/bandit/bandit3.html)

Name of the game is files with spaces in the filename. When we use **cmd** on some <file name>, then **cmd** will treat <file> <name> as two separate args.\
Instead we have to either escape the whitespace using \ or wrap the <file name> into "" or ''.

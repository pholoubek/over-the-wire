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

Name of the game is files with spaces in the filename. When we use **cmd** on some **\<file name\>**, then **cmd** will treat **\<file\> \<name\>** as two separate args. This will most likely lead to err.\
Instead we have to either escape the whitespace using \ or wrap the **\<file name\>** into " or '.

## Level 3

[link](https://overthewire.org/wargames/bandit/bandit4.html)

Really not much to do other than read a bit on **ls** cmd and use the appropriate flags.

```
cd
ls
```

## Level 4

[link](https://overthewire.org/wargames/bandit/bandit5.html)

Get comfortable with **file** cmd. Pipeline for **ls** into **file \*** doesn't work here because filenames are dashed.

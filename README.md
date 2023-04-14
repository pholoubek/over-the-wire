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

Get comfortable with **file** cmd. Pipeline from **ls** into **file \*** doesn't work here because filenames are dashed.

## Level 5

[link](https://overthewire.org/wargames/bandit/bandit6.html)

```
file <args>
```

The **file** cmd is your friend here. Although, the specification also mentions _human-readable_ attribute, I found the passcode by simply looking for the _size_ and _non-executable_ files.

## Level 6

[link](https://overthewire.org/wargames/bandit/bandit7.html)

```
file <args>
```

Again, **file** cmd is our friend. With a little investigation we find **-group**, **-size** and **-user** flags.

> If someone figured how to hide all the giberish output, pleat DM me.

## Level 7

[link](https://overthewire.org/wargames/bandit/bandit8.html)

```
grep <args> <filename>
```

After some reseach on **strings\* & **sort** cmd(s), **grep\*\* did the job.

## Level 8

[link](https://overthewire.org/wargames/bandit/bandit9.html)

Many solutions but **sort** and **uniq** cmds along with proper flags will do the job.

## Level 9

[link](https://overthewire.org/wargames/bandit/bandit10.html)

The key is not to get bambozzled by the look of the file. It's a hex dump (?) with few human-readable strings. We need to list them.

## Level 10

[link](https://overthewire.org/wargames/bandit/bandit11.html)

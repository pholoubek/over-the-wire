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

Really nothing to do as the solution is written in the task.

## Level 11

[link](https://overthewire.org/wargames/bandit/bandit12.html)

Same as before, the solution is really in the hints. It just needs little tweaking with input into appropriate cmd.

## Level 12

[link](https://overthewire.org/wargames/bandit/bandit13.html)

This challange requires comfort with using

```
man <cmd_name>

file <file_name>

gzip <flags> <file_name>

bzip2 <flags> <file_name>

tar <flags> <file_name>
```

It's of essence to be neat when it comes to decompressing files. Highly recommended to follow the tips on creating dir via

```
mkdir <dir_path/name>
```

and moving the initial file.txt into it.
Remove temp files as you progress

## Level 13

[link](https://overthewire.org/wargames/bandit/bandit14.html)

This level needs a bit of research but the answer is really in the description. However, I highly suggest to research all the relevant commands.

## Level 14

[link](https://overthewire.org/wargames/bandit/bandit15.html)

Requires a bit of research of relevant commands. However, the name of the game are ports and not neccessarily secured communication!

## Level 15

```
openssl s_client <magic_args>
```

combination of `openssl` and `s_client` with some combination of hints provided in the description.

## Level 16

First, we need to scan ports on the **localhost** server by using

```
nc <magic_args>
```

and then _pipeline_ the output into

```
grep <magic_match>
```

> Note! nc <magic_args> output is into stderr not stdout. You must merge stdErr into stdOut output before working with grep cmd

After, we can test ports from the filtered list for SSL service

```
openssl s_client <magic_args>
```

and

```
echo <password> | openssl s_client <magic_args>
```

to see which SSL supported port will give us the desired answer

## Level 17

```
diff <file1> <file2>
```

there's really not much to say

checkpoint: hga5tuuCLF6fFzUpnagiMN8ssu9LFrdg

## Level 18

The magic is within

```
ssh
```


# OverTheWire Bandit Levels 0-2

## Level 0

**Objective:** Connect to the Bandit server using SSH and locate the readme file.

**Commands used:**

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
ls
readme
cat readme
```

**Output:**

```text
readme
Command 'readme' not found
Congratulations on your first steps into the bandit game!!
The password is: [REDACTED]
```

**Concept learned:** SSH connection, listing files using ls, and reading files using cat.

## Level 1

**Objective:** Read a file with a special filename (-).

**Commands used:**

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
ls
cat ./.
cat ./-
```

**Output:**

```text
-
cat: ./.: Is a directory
[Password output: REDACTED]
```

**Concept learned:** Handling special filenames using relative paths and the cat command.

## Level 2

**Objective:** Read a file containing spaces and special characters in its filename.

**Commands used:**

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
ls
cat "spaces in this filename"
cat spaces in this filename
cat --spaces in this filename--
cat "./--spaces in this filename--"
```

**Output:**

```text
--spaces in this filename--
cat: 'spaces in this filename': No such file or directory
cat: spaces: No such file or directory
error: unexpected argument '--spaces' found
cat "./--spaces in this filename--"
[Password output: REDACTED]
```

**Concept learned:** Handling spaces and special characters in filenames using quotation marks and relative paths.


## Security Note

All discovered passwords have been redacted from this public report to protect account security.

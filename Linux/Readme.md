# Linux

### Task1: Commands to navigate directory and create files
`ls`, `cd`, `pwd`, `mkdir`, `touch`, `tree`. 

Use those commands to create a directory structure like below.
```
├── one
│   ├── one_a
│   └── one_b
├── three
│   └── three_suba
│       └── three_suba_suba
│           └── three_filea
└── two
    ├── two_suba
    │   └── two_filea
    └── two_subb
        └── two_fileb
```
Use `rm -f filename` command to remove a file. Use `rm -rf directoryname` to remove a directory and all files in it.

### Task2: Learn some basic bash command, `echo` command and `>>`. 
```bash
for i in `seq 1 100`; do echo $i; done # this prints 1, 2, ..., 100 to terminal.
```
```bash
for i in `seq 1 100`; do echo $i >> myfile; done # this create a file named myfile and writes `1, 2, ..., 100` in the file, one number per line.
```

### Task3: Learn commands to read files.
`more`, `cat`, `tail`, `head`, `less`.
1. see the first 10 lines of a file, `head -10 myfile`.
2. print the whole content of a file to standard output (terminal), `cat myfile`.
3. see the last 10 lines of a file `tail -10 myfile`.
4. read the file by `more myfile`. (type `q` to quit)
5. read the file by `less myfile`. (type `q` to quit)

### Task4: Learn basics of `vim`.

### Task5: Learn basics of `grep`.
Find all lines of a file that contain a pattern.
```bash
grep "10" myfile
```

### Task6: Learn basics of `sed`.
Replace a pattern with another pattern, e.g. replace all `10` with `xx`.
```bash
sed -i 's/10/xx/g' myfile
```
Use `cat` to check whether the file has changed.

### Task7: Learn basics of `awk` and pipelining.
First create a file with two columns.
```bash
for i in `seq 1 100`; do echo $i XXX >> mynewfile; done # this creates a file named mynewfile with two columns
```
Check the content of the file by
```bash
cat mynewfile
```
Show the first column of the file by
```bash
awk '{print $1}' mynewfile
```
Show the last 10 rows of the first column by
```bash
awk '{print $1}' mynewfile | tail -10
```

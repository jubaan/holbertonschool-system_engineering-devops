# Holberton School - Command line for the win

This is my personal project containing the solutions to the CMD CHALLENGE game. The table below presents the command-line solutions for each challenge.

## Challenges

| Number | Challenge                                | Command                                                                                 |
|--------|------------------------------------------|-----------------------------------------------------------------------------------------|
| 1      | Hello World                              | `echo "hello world"`                                                                   |
| 2      | Current Working Directory                | `pwd`                                                                                  |
| 3      | List Files                               | `ls`                                                                                   |
| 4      | Print File Contents                      | `cat access.log`                                                                       |
| 5      | Last Lines                               | `tail -n 5 access.log`                                                                 |
| 6      | Create File                              | `touch take-the-command-challenge`                                                     |
| 7      | Create Directory                         | `mkdir -p tmp/files`                                                                   |
| 8      | Copy File                                | `cp take-the-command-challenge tmp/files/`                                             |
| 9      | Move File                                | `mv take-the-command-challenge tmp/files/`                                             |
| 10     | Create Symlink                           | `ln -s tmp/files/take-the-command-challenge take-the-command-challenge`                |
| 11     | Delete Files                             | `rm -rf * .*`                                                                          |
| 12     | Remove Files with Extension              | `rm **/*.doc`                                                                          |
| 13     | Find String in a File                    | `grep "GET" access.log`                                                                |
| 14     | Search for Files Containing String       | `grep -l "500" *`                                                                      |
| 15     | Search for Files by Extension            | `find . -name "access.log*" -type f`                                                   |
| 16     | Search for String in Files Recursively   | `grep -h "500" **/access.log*`                                                         |
| 17     | Extract IP Addresses                     | `grep -Eo '[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}' **/access.log*`             |
| 18     | Count Files                              | `ls -l | wc -l`                                                                        |
| 19     | Simple Sort                              | `sort access.log`                                                                      |
| 20     | Count String in Line                     | `grep "GET" access.log | wc -l`                                                        |
| 21     | Split on a Char                          | `tr ';' '\n' < split-me.txt`                                                           |
| 22     | Print Number Sequence                    | `echo {1..100} " "`                                                                    |
| 23     | Replace Text in Files                    | `sed -i 's/challenges are difficult//g' **/*.txt`                                      |
| 24     | Sum All Numbers                          | `awk '{sum+=$1} END {print sum}' sum-me.txt`                                           |
| 25     | Just the Files                           | `find . -type f -printf "%f\n"`                                                        |
| 26     | Remove Extensions from Files             | `find . -type f -name "*.*" -exec sh -c 'f="{}"; mv -- "$f" "${f%.*}"' \;`             |
| 27     | Replace Spaces in Filenames              | `ls | tr " " "."`                                                                      |
| 28     | Dirs Containing Files with Extension     | `find . -type f -name "*.tf" -exec dirname {} \; | uniq`                               |
| 29     | Files Starting with a Number             | `find . -type f -name "[0-9]*" -printf "%f\n"`                                         |
| 30     | Print Nth Line                           | `sed -n '25p' faces.txt`                                                               |
| 31     | Reverse README                           | `tac reverse-me.txt`                                                                   |
| 32     | Remove Duplicate Lines                   | `awk '!seen[$0]++' faces.txt`                                                          |
| 33     | Find Primes                              | `grep -Eo '[0-9]+' random-numbers.txt | factor | awk 'NF==2 {print $2}' | sort -u | wc -l` |
| 34     | Print Common Lines                       | `cat access.log.* | awk '{print $1}' | sort | uniq -d`                                 |
| 35     | Print Line Before                        | `grep -h -B1 404 **/access.log* | grep -vE '404|--'`                                   |
| 36     | Print Files if Different                 | `find . -type f -name "*.bin" -exec diff base.bin {} \; | awk '{print $5}' | sed 's|./||'` |
| 37     | Nested Dirs                              | `cat "./.../  /. .the flag.txt"`                                                       |
| 38     | Find Tabs in a File                      | `grep -c $'\t' file-with-tabs.txt`                                                     |
| 39     | Remove Files without Extension           | `find . -type f ! -name "*.txt" ! -name "*.exe" -delete`                               |
| 40     | Remove Files with a Dash                 | `rm -- -*`                                                                             |
| 41     | Print Sorted by Key                      | `sort -u -k2 -n ps-ef1 ps-ef2`                                                         |
| 42     | IPv4 Listening Ports                     | `grep "LISTEN" netstat.out | grep -oP "tcp\s+.*:\K\d+"|sort -nr`                       |

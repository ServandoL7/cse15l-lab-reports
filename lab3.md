# Lab Report 3
**Four Commands with grep**

Option 1: Case insensitive search
- Example 1
```
$grep -i "blood" ar149.txt
```
- Output:
![Image](O1E1.png)
- Example 2
```
$grep -i "gene" 1471-244X-2-9.txt
```
- Output:
![Image](O1E2.png)

Option 2: Displaying the count of number of matches
- Example 1
```
grep -c "bio" ar140.txt
grep -c "a" ar140.txt
grep -c "blood" ar140.txt
```
- Output:
- ![Image](O2E1.png)
- Example 2
```
grep -c "plane" chapter-12.txt
grep -c "plane" chapter-2.txt
grep -c "plane" chapter-7.txt
```
- Output:
![Image](O2E2.png)

Option 3: Displaying only the matched pattern
- Example 1
```
grep -o "plane" chapter-1.txt
```
- Output:
![Image](O3E1.png)
- Example 2
```
grep -o "crash" chapter-7.txt
```
- Output:
![Image](O3E2.png)

Option 4: Show line number while displaying the output using grep -n
- Example 1
```
grep -n "plane" chapter-13.3.txt
grep -n "plane" chapter-5.txt
```
- Output:
![Image](O4E1.png)
- Example 2
```
grep -n "cost" water_fees.txt
grep -n "cost" predatory_loans.txt
```
- Output:
![Image](O4E2.png)


All commands shown were and can be found on this [Link](https://www.geeksforgeeks.org/grep-command-in-unixlinux/#)

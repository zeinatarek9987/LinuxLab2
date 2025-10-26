# Lab 2 – Linux Basics 2
**Name:** Zeina Tarek Zayan , Id:223102281
  

---

## Part A – Linux Commands

### 1. Create a new directory
```bash
mkdir Lab2
cp words numbers Lab2/
paste words numbers > MergeContent
head -n 3 MergeContent
sort MergeContent > SortedMergedContent
tr 'a-z' 'A-Z' < SortedMergedContent > UppercaseSortedMergedContent
grep -n "^w.*[0-9]$" MergeContent
sed 's/I/O/g' MergeContent > NewMergeContent
paste MergeContent NewMergeContent
---

## Part B – Linux Permissions (Theory Explanation)

Since GitHub Codespaces does not allow creating new Linux users, the following commands are written as theory.

### 1. Create a new group
```bash
sudo groupadd penguins
sudo useradd -m -g penguins -c "Tux the penguin (1)" tux1
sudo useradd -m -g penguins -c "Tux the penguin (2)" tux2
sudo passwd tux1
sudo passwd tux2
ls -ld /home/tux1
chmod o+rx /home/tux1
mkdir /home/tux1/bin
cp /bin/ls /home/tux1/bin/my_ls
chmod 640 /home/tux1/bin/my_ls
chmod 755 /home/tux1/bin/my_ls


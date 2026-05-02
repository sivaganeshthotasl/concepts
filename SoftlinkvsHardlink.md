### 🆔 Inode 🆔 ###

It contains:

   **→**        ``File size``
   
   **→**      ``Permissions (read/write/execute)``
   
   **→**      ``Owner``
        
   **→**    ``Disk location``
        

        
🔧 Example 

```
echo "Hello World" > file1.txt
```

Check inode:

```
ls -i file1.txt
```

Output:

```
123456 file1.txt
```
👉 123456 is the inode number (unique ID of the file) 





**🟡 Soft Link vs 🔵 Hard Link**

**let’s do a hands-on lab so you actually see how soft links and hard links behave**

**Step 1: Create a file**

```
mkdir /tmp/link-demo
cd /tmp/link-demo

echo "Hello DevOps" > file1.txt
```

Check:

```
ls -li
```

👉 Note the inode number of file1.txt

**Step 2: Create a Hard Link**

```
ln file1.txt file2.txt
```

Check:

```
ls -li
```

👉 Observe: file1.txt and file2.txt have same inode and Link count will be 2

**Test Hard Link behavior**

Modify one file:

```
echo "Hard link test" >> file2.txt
```

Check:

```
cat file1.txt
```

👉 Output will include:

``
Hello DevOps
``

``
Hard link test
``

✔ Both files share same data


Delete original file:

```
rm file1.txt
```

Check:

```
cat file2.txt
```

👉 Still works ✅


**Step 3: Create a Soft Link**

```
ln -s file2.txt softlink.txt
```

Check:

```
ls -li
```

👉 Observe:

---> oftlink.txt has different inode

---> Shows arrow:

``softlink.txt -> file2.txt``

**Test Soft Link behavior**

Read file:

```
cat softlink.txt
```

👉 Works ✅

Delete original file:

```
rm file2.txt
```

Now try:

```
cat softlink.txt
```

👉 You get:

``No such file or directory ❌``

**How to Identify file types**

```
ls -l
```

``-rw-r--r--``  → normal file / hard link

``l``          → soft link

Example:

``lrwxrwxrwx softlink.txt -> file2.txt``


👉 Hard link is used to create another name for the same file for backup

👉 Soft link (symlink) is used to create a reference (pointer) to a file or directory so it can be accessed from a different path.






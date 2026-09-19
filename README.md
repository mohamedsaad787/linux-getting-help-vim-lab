# linux-getting-help-vim-lab
## Section 1 – Documentation & Command Help

### 1. `tail` Manual

```bash
man tail
```

Search:

```text
/follow
```

Exit:

```text
q
```

---

### 2. Search for `zip`

```bash
man -k zip
```

**Result:**
```text
ظهور نتائج الـ manual pages المرتبطة بكلمة zip
```

---

### 3. Help for `cd`

```bash
help cd
```

**Result:**
```text
عرض الـ built-in help الخاص بأمر cd
```

---

### 4. Locate `passwd`

```bash
whereis passwd
```

**Result:**
```text
ظهور مسار passwd binary ومسار الـ manual page
```

---

# Section 2 – Data Generation & Vim Editing

### 1. Create `audit.txt`

```bash
ls -l /etc | head -n 10 > audit.txt
```

Verify:

```bash
cat audit.txt
```

**Result:**
```text
أول 10 أسطر من ls -l /etc
```

---

### 2. Open at Last Line

```bash
vim +$ audit.txt
```

**Result:**
```text
audit.txt opened in Vim with the cursor on the last line
```

---

### 3. Delete Line 1

```text
gg
dd
```

**Result:**
```text
Line 1 deleted
```

---

### 4. Copy Line 2 and Paste at Bottom

```text
yy
G
p
```

**Result:**
```text
Line 2 copied and pasted at the bottom
```

---

### 5. Visual Block Delete

```text
gg
Ctrl + v
4j
9l
d
```

**Result:**
```text
First 10 characters deleted from lines 1–5
```

---

### 6. Visual Line Delete

```text
gg
2j
Shift + v
d
```

**Result:**
```text
Line 3 deleted
```

---

### 7. Save and Exit

```text
Esc
:wq
```

**Result:**
```text
File saved and Vim closed
```

---

# Section 3 – File Appending & Backup

### 1. Append 12 Dashes

```bash
echo "------------" >> audit.txt
```

Verify:

```bash
tail -n 3 audit.txt
```

**Result:**
```text
------------
```

---

### 2. Create Backup

```bash
cp audit.txt audit_backup.txt
```

Verify:

```bash
ls -l audit.txt audit_backup.txt
```

**Result:**
```text
audit.txt
audit_backup.txt
```

---

# Final Result

```text
audit.txt
audit_backup.txt
```

## Git Note

#### Menu:
[Branch Delete](https://github.com/mobaarok/markdown/blob/master/git-note.md#to-delete-branch)
[short](#to-delete-branch)

### গিটের ভার্শন চেক করতেঃ
```
git --version
```

### গিট কনফিগার করাঃ
```
git config --global user.name "your-name"
git config --global user.email "your-mail-name"
```

### প্রজেক্টে গিট ইনিশিয়ালাইজ(initialized) করাঃ
```
git init
```

### স্ট্যাটাস চেক করাঃ
```
git status
```

### লগ চেক করাঃ
```
git log
//or 
git log --oneline
```

### ফাইল ট্র্যাক বা এড করাঃ
```
git add filename
```

### সব ফাইল ট্র্যাক বা এড করাঃ
```
git add --all
//or
git add .
```

### কমিট করাঃ 
```
git commit -m "added some file"
```

### পূর্বের কমিট করা ভার্শনে ফিরে যেতেঃ
```
git checkout commmit-id
```

### ব্রাঞ্চ তৈরি করতেঃ
```
git branch branch-name
```
###  ব্রাঞ্চের লিস্ট দেখতেঃ
```
git branch
```

### ব্রাঞ্চ-এ চেক অউট করতেঃ 
```
git checkout branch-name
```

###  নতুন ব্রাঞ্চ তৈরি করে সাথে সাথে ওই রাঞ্-এ  চেকআউট করতেঃ
```
git checkout -b branch-name
```

### [রাঞ্চ ডিলিট করত:]{#to-delete-branch}
```
git branch -D branch-name
```

#### ব্রাঞ্ছ 
```
git merge branch-name
```

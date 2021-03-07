# Git Note

### Menu:

[Branch Delete](https://github.com/mobaarok/markdown/blob/master/git-note.md#to-delete-branch) [short](git-note.md#to-delete-branch)

## গিটের ভার্শন চেক করতেঃ

```text
git --version
```

## গিট কনফিগার করাঃ

```text
git config --global user.name "your-name"
git config --global user.email "your-mail-name"
```

## প্রজেক্টে গিট ইনিশিয়ালাইজ\(initialized\) করাঃ

```text
git init
```

## স্ট্যাটাস চেক করাঃ

```text
git status
```

## লগ চেক করাঃ

```text
git log
//or 
git log --oneline
```

## ফাইল ট্র্যাক বা এড করাঃ

```text
git add filename
```

## সব ফাইল ট্র্যাক বা এড করাঃ

```text
git add --all
//or
git add .
```

## কমিট করাঃ

```text
git commit -m "added some file"
```

## পূর্বের কমিট করা ভার্শনে ফিরে যেতেঃ

```text
git checkout commmit-id
```

## ব্রাঞ্চ তৈরি করতেঃ

```text
git branch branch-name
```

## ব্রাঞ্চের লিস্ট দেখতেঃ

```text
git branch
```

## ব্রাঞ্চ-এ চেক অউট করতেঃ

```text
git checkout branch-name
```

## নতুন ব্রাঞ্চ তৈরি করে সাথে সাথে ওই রাঞ্-এ  চেকআউট করতেঃ

```text
git checkout -b branch-name
```

## \[রাঞ্চ ডিলিট করত:\] <a id="to-delete-branch"></a>

```text
git branch -D branch-name
```

### ব্রাঞ্ছ

```text
git merge branch-name
```


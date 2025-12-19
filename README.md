# aws-cli
cli how to create
Sure 😊
I’ll explain **AWS CLI creation/setup** in a **simple, safe, step-by-step way**.

---

# ✅ What “create CLI” really means

You **do NOT create AWS CLI in AWS**.
You **install AWS CLI on your machine** and then **configure it** with credentials.

So there are **2 parts**:

1. Install AWS CLI
2. Configure AWS CLI

---

# 1️⃣ Install AWS CLI

## 🖥️ Option A: Windows (most common)

### Step 1: Download installer

* Go to **AWS Console → search “AWS CLI install”**
* Download **Windows x64 MSI**

### Step 2: Install

* Double-click installer
* Next → Next → Finish

### Step 3: Verify

Open **Command Prompt** or **PowerShell**:

```bash
aws --version
```

✔️ You should see something like:

```
aws-cli/2.x.x Python/3.x
```

---

## 🐧 Option B: Linux / CloudShell

Already installed ✔️
Just check:

```bash
aws --version
```

---

## 🍎 Option C: macOS

```bash
brew install awscli
aws --version
```

---

# 2️⃣ Create IAM user for CLI (IMPORTANT)

### Step 1: IAM → Users → Create user

* Username: `cli-user`
* Access type: **Programmatic access**

### Step 2: Attach policy (learning-safe)

For practice:

```
AdministratorAccess
```

(You can reduce later)

### Step 3: Download credentials

You’ll get:

* **Access Key ID**
* **Secret Access Key**

⚠️ Save them — secret key is shown only once.

---

# 3️⃣ Configure AWS CLI

Run this on your machine or CloudShell:

```bash
aws configure
```

Enter values:

```
AWS Access Key ID:     <paste key>
AWS Secret Access Key: <paste secret>
Default region name:   us-east-1
Default output format: json
```

✔️ CLI is now ready.

---

# 4️⃣ Test AWS CLI (very important)

```bash
aws sts get-caller-identity
```

Expected output:

```json
{
  "Account": "654654362568",
  "Arn": "arn:aws:iam::654654362568:user/cli-user",
  "UserId": "AIDA..."
}
```

If this works → **CLI configured correctly** ✅

---

# 🔐 Safety tips (so you don’t get scared later)

### ✔️ Good practices

* Use **one CLI user only**
* Delete access keys if not needed
* Never share keys

### ❌ Avoid

* Hardcoding keys in code
* Uploading keys to GitHub

---

# 🧠 Common confusion (clearing it)

| Question                       | Answer                         |
| ------------------------------ | ------------------------------ |
| Is CloudShell same as AWS CLI? | CloudShell **already has CLI** |
| Do I need Docker for CLI?      | ❌ No                           |
| Does CLI cost money?           | ❌ No                           |
| Can CLI create paid resources? | ✅ Yes (be careful)             |

---

# ✅ Minimal “fear-free” CLI commands to try

```bash
aws s3 ls
aws iam list-users
aws ec2 describe-regions
```

All are **safe & free**.

---

## 🌱 Next (if you want)

I can:

* Give you **AWS CLI cheat sheet**
* Teach **safe CLI practice labs**
* Explain **CLI vs Console vs SDK**
* Prepare **AWS interview CLI questions**

Just tell me 👍

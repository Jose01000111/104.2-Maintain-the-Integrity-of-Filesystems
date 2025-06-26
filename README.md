# 🛠️ 104.2 Maintain the Integrity of Filesystems

## ✅ What I Did in This Lab
I explored commands like df, du, fsck, and tune2fs to inspect, analyze, and repair ext-based and XFS filesystems. I created a broken loopback filesystem on purpose to simulate real-world repair scenarios using e2fsck and xfs_repair.

I’ve included some helpful links to guide you through the lab and for studying afterward:

[EXAM OBJECTIVE 104.2](https://www.lpi.org/our-certifications/exam-101-102-objectives/#104.2_Maintain_the_integrity_of_filesystems)

[OBJ.104.2 NOTES]()

[OBJ. 104.2 LAB]()

---

## 1️⃣ Check Disk Usage and Inodes
🔹View disk space and inode usage

🔹Check disk usage for specific directories

## 2️⃣ Simulate and Detect Filesystem Problems
🔹Create and mount a test ext4 filesystem using a loop device

🔹Force an unclean shutdown to simulate corruption

🔹Run filesystem check

## 3️⃣ Repair and Tune Filesystems
🔹Fix detected filesystem issues

🔹Use tune2fs to check last check time and force check interval

## 4️⃣ Work with XFS Filesystems
🔹Create and mount a test XFS filesystem

🔹Run xfs repair tools

---

## 🧠 What I Learned
In this lab, I learned how to inspect and monitor disk and inode usage, simulate filesystem corruption, and safely repair ext4 and XFS filesystems. I now understand when to use fsck vs xfs_repair, and how to schedule routine checks with tune2fs. This gave me hands-on experience with real admin tasks critical for Linux system maintenance. 🐧💾

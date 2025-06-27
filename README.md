# 🛠️ 104.2 Maintain the Integrity of Filesystems

## ✅ What I Did in This Lab
I explored commands like df, du, fsck, and tune2fs to inspect, analyze, and repair ext-based and XFS filesystems. I created a broken loopback filesystem on purpose to simulate real-world repair scenarios using e2fsck and xfs_repair.

I’ve included some helpful links to guide you through the lab and for studying afterward:

[EXAM OBJECTIVE 104.2](https://www.lpi.org/our-certifications/exam-101-102-objectives/#104.2_Maintain_the_integrity_of_filesystems)

[OBJ.104.2 NOTES](https://1drv.ms/w/c/354f1c8d534fbced/EX-TVs6Qv_5Dqwo0O10_9d0BlzoEQxHypsHsM2ivdF9P6A?e=lsPWIW)

[OBJ. 104.2 LAB](https://1drv.ms/w/c/354f1c8d534fbced/EcROq1N9bmZIlNo6gvoMbuoBnuJ4m34KcYRUJgFWolrWwQ?e=xDklyO)

---

## 1️⃣ Check Disk Usage and Inodes
🔹View disk space and inode usage

![fARfmfh](https://github.com/user-attachments/assets/2495410b-9fcf-4f14-b3f3-9552b335a704)

![vu2i1ao](https://github.com/user-attachments/assets/0f586979-56cc-43f8-b051-533df032c971)

🔹Check disk usage for specific directories

![Dtf00Op](https://github.com/user-attachments/assets/cbda6414-d9e8-4f10-9e6b-527177fb4d7e)

## 2️⃣ Simulate and Detect Filesystem Problems
🔹Create and mount a test ext4 filesystem using a loop device

![7RhPy6Y](https://github.com/user-attachments/assets/a965e61f-1282-4011-8469-37787309badb)

🔹Force an unclean shutdown to simulate corruption

![rmeBuKd](https://github.com/user-attachments/assets/bf281ad6-4877-431c-a21b-acb8958d5393)

🔹Run filesystem check

![cGk0zyz](https://github.com/user-attachments/assets/d1730af0-555d-4988-9393-3d8f168c19de)

## 3️⃣ Repair and Tune Filesystems
🔹Fix detected filesystem issues

![GgAmkVV](https://github.com/user-attachments/assets/7e7c02a7-0bd3-4dc9-a6dd-99eb6e3820b5)

🔹Use tune2fs to check last check time and force check interval

![5WkxtaZ](https://github.com/user-attachments/assets/eb61399b-f1dd-4c97-bf93-5897331978ec)

## 4️⃣ Work with XFS Filesystems
🔹Create and mount a test XFS filesystem

![0c169e2d-f8cb-4017-9bbf-d1cc443d3fb7](https://github.com/user-attachments/assets/a2094f25-4ff8-4b82-92fc-861766d2bc93)

🔹Run xfs repair tools

![E4OaUuN](https://github.com/user-attachments/assets/37231e99-8c17-4357-af3d-34f252bf10b6)

---

## 🧠 What I Learned
In this lab, I learned how to inspect and monitor disk and inode usage, simulate filesystem corruption, and safely repair ext4 and XFS filesystems. I now understand when to use fsck vs xfs_repair, and how to schedule routine checks with tune2fs. This gave me hands-on experience with real admin tasks critical for Linux system maintenance. 🐧


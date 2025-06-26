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

bash
Copy
Edit
df -hT          # View disk usage in human-readable format
df -i           # View inode usage
🔹Check disk usage for specific directories

bash
Copy
Edit
du -sh /var/log/
du -ah /home | sort -rh | head -n 10
## 2️⃣ Simulate and Detect Filesystem Problems
🔹Create and mount a test ext4 filesystem using a loop device

bash
Copy
Edit
dd if=/dev/zero of=/tmp/testfs.img bs=1M count=100
mkfs.ext4 /tmp/testfs.img
mkdir /mnt/testfs
mount -o loop /tmp/testfs.img /mnt/testfs
🔹Force an unclean shutdown to simulate corruption

bash
Copy
Edit
touch /mnt/testfs/breakme.txt
sync
umount /mnt/testfs   # Skip sync or force unmount to simulate issue
🔹Run filesystem check

bash
Copy
Edit
e2fsck /tmp/testfs.img
## 3️⃣ Repair and Tune Filesystems
🔹Fix detected filesystem issues

bash
Copy
Edit
e2fsck -y /tmp/testfs.img
🔹Use tune2fs to check last check time and force check interval

bash
Copy
Edit
tune2fs -l /tmp/testfs.img | grep -E 'Check interval|Last checked'
tune2fs -c 10 -i 5d /tmp/testfs.img   # Set max mount count and interval
## 4️⃣ Work with XFS Filesystems
🔹Create and mount a test XFS filesystem

bash
Copy
Edit
mkfs.xfs /tmp/testfs.img
mount -o loop /tmp/testfs.img /mnt/testfs
umount /mnt/testfs
🔹Run xfs repair tools

bash
Copy
Edit
xfs_repair /tmp/testfs.img   # Run repair tool for XFS
xfs_db /tmp/testfs.img       # View internal XFS metadata

## 🧠 What I Learned
In this lab, I learned how to inspect and monitor disk and inode usage, simulate filesystem corruption, and safely repair ext4 and XFS filesystems. I now understand when to use fsck vs xfs_repair, and how to schedule routine checks with tune2fs. This gave me hands-on experience with real admin tasks critical for Linux system maintenance. 🐧💾

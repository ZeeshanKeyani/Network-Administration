# 🔥 Subnetting in One Shot – The Ultimate Guide [2025 Edition]
![Visitors](https://visitor-badge.laobi.icu/badge?page_id=subnetting-one-shot-guide)  

![CCNA Badge](https://img.shields.io/badge/For-CCNA%20%7C%20CEH-blue?style=flat-square)  
![IPv4 Badge](https://img.shields.io/badge/IP-IPv4%20%7C%20IPv6-orange?style=flat-square)  
![Difficulty Badge](https://img.shields.io/badge/Difficulty-Beginner%20to%20Pro-yellow?style=flat-square)  


## 📌 Meta Description
Learn subnetting in one shot with this **complete A–Z guide**. Step-by-step explanations, subnet mask cheat sheets, CIDR notation, VLSM, and solved examples. Perfect for **CCNA, CEH, networking interviews, and IT pros**.

## 🏆 Introduction: Why Subnetting Matters
💡 In the world of networking, **subnetting** is one of the most feared yet most important topics.  

👉 Whether you are preparing for **CCNA**, **CEH**, or working as a network engineer, mastering subnetting is a must.  

✨ The truth: subnetting is **not rocket science**. Once you learn shortcuts and patterns, you can solve subnetting problems in seconds.  

This guide gives you **subnetting in one shot** — from **basics to advanced** — with **tables, formulas, GIFs, and solved examples**.  

## ⚡ What is Subnetting?
Subnetting = dividing a large IP network into **smaller, manageable sub-networks**.  

📌 Think of it like dividing a **city** into smaller **sectors** for better management.  

✅ Without subnetting → One giant network (slow, messy).  
✅ With subnetting → Smaller networks (fast, secure, efficient).  

![Subnetting GIF Placeholder](subnetting-split.gif)

## 📚 Basics of IP Addressing
- IPv4 = **32 bits** (4 octets, each 8 bits).  
- Example: `192.168.1.10` → Binary: `11000000.10101000.00000001.00001010`  

👉 IP = **Network ID + Host ID**  

📌 Example:  
192.168.1.0/24
Network = 192.168.1.0
Host range = 192.168.1.1 – 192.168.1.254
Broadcast = 192.168.1.255

![IP Addressing GIF](ip-bits.gif)

## 🏷️ IP Address Classes
⚠️ Classful addressing is old, but helps in understanding.  

| Class | Range       | Default Mask      | Hosts (approx) |
|-------|-------------|-------------------|----------------|
| A     | 0 – 127     | 255.0.0.0         | 16 million     |
| B     | 128 – 191   | 255.255.0.0       | 65,000+        |
| C     | 192 – 223   | 255.255.255.0     | 254            |

🔒 **Private IPs**  
- 10.0.0.0 – 10.255.255.255  
- 172.16.0.0 – 172.31.255.255  
- 192.168.0.0 – 192.168.255.255  

## 🧩 Subnet Mask and CIDR
- Subnet mask defines **Network vs Host bits**.  
- Example: `/24` = `255.255.255.0`  

👉 CIDR (Classless Inter-Domain Routing) = modern notation.  

📌 Example:  
- `/26` → 255.255.255.192  
- `/30` → 255.255.255.252  

![CIDR GIF](cidr-mask.gif)

## 📐 Subnetting Formulas
⚡ Key formulas:  
1. **Number of Subnets** = `2^n` (n = borrowed bits)  
2. **Hosts per Subnet** = `2^h – 2` (h = host bits left)  
3. **Block Size** = `256 – subnet mask value`  

✅ Example:  
- /26 → Mask = 255.255.255.192  
- Block size = 64  
- Hosts = `2^6 – 2 = 62`  

## 🚀 Block Size Method (Fastest Trick)
**Question:** Subnet `192.168.1.0/26`  

1. Mask = 255.255.255.192  
2. Block size = 64  
3. Subnets:  
   - 192.168.1.0 – 63  
   - 192.168.1.64 – 127  
   - 192.168.1.128 – 191  
   - 192.168.1.192 – 255  
4. Hosts = 62 each  

🔥 **Shortcut:** Always use block size for subnet ranges.  

![Block Size Method GIF](block-size.gif)

## 📊 Subnetting Cheat Table

| CIDR | Subnet Mask       | Block Size | Hosts/Subnet |
|------|-------------------|------------|--------------|
| /24  | 255.255.255.0     | 1          | 254          |
| /25  | 255.255.255.128   | 128        | 126          |
| /26  | 255.255.255.192   | 64         | 62           |
| /27  | 255.255.255.224   | 32         | 30           |
| /28  | 255.255.255.240   | 16         | 14           |
| /29  | 255.255.255.248   | 8          | 6            |
| /30  | 255.255.255.252   | 4          | 2            |

👉 Each step halves the host count.  

## 📝 Solved Example
**Question:** Subnet `172.16.0.0/20`  

1. Mask = 255.255.240.0  
2. Block size = 16  
3. Ranges:  
   - 172.16.0.0 – 172.16.15.255  
   - 172.16.16.0 – 172.16.31.255  
   - 172.16.32.0 – 172.16.47.255 …  
4. Hosts = `2^12 – 2 = 4094`  

![Subnet Range GIF](subnet-ranges.gif)


## 🎯 VLSM (Variable Length Subnet Masking)
👉 VLSM = Subnetting inside a subnet → saves IPs.  

**Example:**  
- Sales (50 hosts) → /26  
- HR (20 hosts) → /27  
- Admin (10 hosts) → /28  

⚡ Efficient IP allocation = No wastage.  

![VLSM GIF](vlsm.gif)



## 🌐 IPv6 Subnetting
- IPv6 = 128-bit, written in hex.  
- Always subnetted as `/64`.  

✅ Example:  
`2001:db8::/64` → trillions of hosts 🚀  

❌ No broadcast in IPv6 → only **network + interface ID**.  



## 🔑 Fast Practice Hacks
✔ Memorize cheat table.  
✔ Use block size trick.  
✔ Subtract 2 hosts (network + broadcast).  
✔ In exams → write table first, then solve.  



## ⚠️ Common Mistakes
- Forgetting to subtract 2 hosts.  
- Mixing **block size** with **subnet size**.  
- Wrong network ID alignment.  
- Confusing usable IP with broadcast.  


## 📚 Practice Questions
1. Subnet mask of /23?  
2. Hosts in /19?  
3. Divide `192.168.10.0/24` into 4 subnets.  
4. A company needs 500 hosts → Which mask?  



## 🏁 Conclusion
Subnetting = **foundation of networking**.  

With this **one-shot guide**, you now know:  
- IP basics & classes  
- CIDR & masks  
- Subnet formulas & block size trick  
- Subnetting cheat table  
- VLSM & IPv6  


## ✍️ Author

> 👨‍💻 **Written by: Zeeshan Keyani**  
> ![Author Badge](https://img.shields.io/badge/Author-Zeeshan%20Keyani-blue?style=for-the-badge)  
> Passionate about Networking, Cybersecurity, and DevOps 🚀  
> Follow for more guides on **CCNA, CEH, and IT skills mastery**.  

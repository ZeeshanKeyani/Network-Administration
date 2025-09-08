# 🔥 Subnetting in One Shot – The Ultimate Guide [2025 Edition]

## 📌 Meta Description
Learn subnetting in one shot with this complete A–Z guide. Step-by-step explanations, subnet mask cheat sheets, CIDR notation, VLSM, and solved examples. Perfect for CCNA, networking interviews, and IT pros.

---

## 🏆 Introduction: Why Subnetting Matters
In the world of networking, **subnetting** is one of the most feared yet most important topics. Whether you are preparing for **CCNA**, **CEH**, or working as a network engineer, mastering subnetting is a must.  

But here’s the truth: subnetting is **not rocket science**. Once you learn a few shortcuts and patterns, you can solve subnetting problems in seconds.  

This guide will give you **subnetting in one shot** — from **basics to advanced** — with **step-by-step explanations, tables, GIF-based visual guides, and solved examples**.  

---

## ⚡ What is Subnetting?
Subnetting is the process of dividing a large IP network into smaller, manageable sub-networks (subnets).  

👉 Think of it like dividing a **city** into smaller **sectors** for better management.  

- Without subnetting → One giant network (slow, messy).  
- With subnetting → Multiple smaller networks (faster, secure, efficient).  

![Subnetting GIF Placeholder](subnetting-split.gif)

---

## 📚 Basics of IP Addressing
- IPv4 = **32 bits** (4 octets, each 8 bits).  
- Written as: `192.168.1.10` → Binary: `11000000.10101000.00000001.00001010`  

👉 IP is divided into **Network ID** + **Host ID**.  

![IP Addressing GIF](ip-bits.gif)

---

## 🏷️ IP Address Classes (Legacy Knowledge)
Although CIDR has replaced classful addressing, classes still help in understanding.  

- **Class A** → 0–127 → Default mask: 255.0.0.0 → Millions of hosts  
- **Class B** → 128–191 → Default mask: 255.255.0.0 → Thousands of hosts  
- **Class C** → 192–223 → Default mask: 255.255.255.0 → 254 hosts  

Private IP ranges (used inside LANs):  
- 10.0.0.0 – 10.255.255.255  
- 172.16.0.0 – 172.31.255.255  
- 192.168.0.0 – 192.168.255.255  

---

## 🧩 Subnet Mask and CIDR
- Subnet mask defines which part is **network** and which part is **host**.  
- Example: `/24` = `255.255.255.0` → 24 bits for network, 8 bits for hosts.  

👉 CIDR (Classless Inter-Domain Routing) is the modern way of writing subnet masks.  

![CIDR GIF](cidr-mask.gif)

---

## 📐 Subnetting Formulas You Must Know
1. **Number of Subnets** = \( 2^n \) (n = borrowed bits)  
2. **Hosts per Subnet** = \( 2^h - 2 \) (h = remaining host bits, subtract 2 for network & broadcast)  
3. **Block Size** = \( 256 - \text{subnet mask value} \)  

**Example:**  
- /26 → 255.255.255.192 → Block size = 256 – 192 = **64**  
- Hosts = 2^6 – 2 = **62**  

---

## 🚀 Subnetting with the Block Size Method
The **fastest method** to subnet in exams and real life.  

**Example:**  
IP = `192.168.1.0/26`  

1. Mask = 255.255.255.192  
2. Block size = 64  
3. Subnets:  
   - 192.168.1.0 – 192.168.1.63  
   - 192.168.1.64 – 192.168.1.127  
   - 192.168.1.128 – 192.168.1.191  
   - 192.168.1.192 – 192.168.1.255  
4. Hosts per subnet = 62  

![Block Size Method GIF](block-size.gif)

---

## 📊 Subnetting Cheat Table (Quick Reference)

| CIDR | Subnet Mask       | Block Size | Hosts/Subnet |
|------|-------------------|------------|--------------|
| /24  | 255.255.255.0     | 1          | 254          |
| /25  | 255.255.255.128   | 128        | 126          |
| /26  | 255.255.255.192   | 64         | 62           |
| /27  | 255.255.255.224   | 32         | 30           |
| /28  | 255.255.255.240   | 16         | 14           |
| /29  | 255.255.255.248   | 8          | 6            |
| /30  | 255.255.255.252   | 4          | 2            |

👉 Notice: each step halves the hosts.

---

## 📝 Solved Subnetting Example
**Question:** Subnet `172.16.0.0/20`  

1. Mask = 255.255.240.0  
2. Block size = 256 – 240 = 16  
3. Ranges:  
   - 172.16.0.0 – 172.16.15.255  
   - 172.16.16.0 – 172.16.31.255  
   - 172.16.32.0 – 172.16.47.255 …  
4. Hosts per subnet = 2^12 – 2 = **4094**  

![Subnet Range GIF](subnet-ranges.gif)

---

## 🎯 VLSM (Variable Length Subnet Masking)
VLSM = subnetting inside a subnet, giving different subnet sizes as needed.  

**Example:**  
- Sales dept (needs 50 hosts) → /26  
- HR dept (needs 20 hosts) → /27  
- Admin dept (needs 10 hosts) → /28  

👉 Saves IP addresses and avoids wastage.  

![VLSM GIF](vlsm.gif)

---

## 🌐 IPv6 Subnetting (Quick Look)
IPv6 = 128-bit addressing, written in hex.  
Always subnetted as `/64`.  

- Example: `2001:db8::/64` → 18 quintillion hosts 😱  

No broadcast addresses, only **network + interface ID**.  

---

## 🔑 Fast Practice Hacks
1. Memorize the subnet cheat table.  
2. Use block size trick for quick calculations.  
3. Always subtract **2 hosts** (network + broadcast).  
4. Write the table on exam rough sheet → subnet any question in < 30 sec.  

---

## 📌 Common Mistakes to Avoid
- Forgetting to subtract 2 from host calculation.  
- Mixing block size with subnet size.  
- Not aligning subnet boundaries correctly.  
- Confusing network ID with first usable IP.  

---

## 📚 Subnetting Practice Questions
1. What is the subnet mask of /23?  
2. How many hosts are available in /19?  
3. Divide 192.168.10.0/24 into 4 equal subnets.  
4. A company needs 500 hosts → which subnet mask should you use?  

---

## 🏁 Conclusion
Subnetting is the **backbone of networking**. At first, it seems confusing, but once you know **block size, formulas, and the cheat table**, it becomes second nature.  

With this **one shot subnetting guide**, you now have everything:  
- Basics of IP and classes  
- CIDR and masks  
- Formulas and block size trick  
- Subnetting tables and solved examples  
- VLSM and IPv6  

Practice a few problems daily, and subnetting will become your **superpower in networking exams and jobs**.
```



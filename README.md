# 🌐 Hyperlocal Disaster-to-Commerce (D2C) Mesh
**AI-Driven Community Flood Nowcasting, Clearance-Aware Rescue Routing & Decentralized SME Relief Network**

[![Hackathon](https://img.shields.io/badge/AI_FOR_ALL-Hackathon-rose?style=for-the-badge)](https://example.com)
[![Primary Track](https://img.shields.io/badge/Core_Track_6-Resilient_Communities-06b6d4?style=for-the-badge)](https://example.com)
[![Support Track](https://img.shields.io/badge/Track_5-Smart_Mobility-f59e0b?style=for-the-badge)](https://example.com)
[![Support Track](https://img.shields.io/badge/Track_2-SME_&_Local_Economy-10b981?style=for-the-badge)](https://example.com)

---

## 📌 ภาพรวมโครงการ (Project Overview)
**Hyperlocal D2C Mesh** คือแพลตฟอร์ม AI ที่บูรณาการ 3 แทร็กการแข่งขันเข้าด้วยกัน เพื่อเปลี่ยนระบบเตือนภัยน้ำท่วมแบบตั้งรับ (Passive Warning) ให้เป็นระบบบริหารจัดการวิกฤตและเศรษฐกิจหมุนเวียนในชุมชนแบบครบวงจร (Active Crisis-to-Commerce Ecosystem):

1. 🛡️ **Track 6 — Resilient Communities (แกนหลัก):** พยากรณ์น้ำท่วมระดับซอยย่อยล่วงหน้า $3\text{–}6\text{ ชั่วโมง}$ ด้วยโมเดล **Spatio-Temporal GNN** ร่วมกับระบบ **Zero-Hardware Virtual Water Gauge** ที่ใช้ Computer Vision วัดความลึกของน้ำจากภาพถ่ายชาวบ้านและกล้อง CCTV หน้าร้านชำ เทียบกับวัตถุมาตรฐานในชุมชน (เช่น ขอบฟุตบาทสูง $15\text{ cm}$ และล้อรถ)
2. 🚑 **Track 5 — Smart Mobility & Cities (ตัวซัพพอร์ต):** คำนวณเส้นทางอพยพและลำเลียงเสบียงแบบพลวัตตามขีดจำกัดความสูงของยานพาหนะ (**Clearance-Aware Dynamic Routing**) แยกเส้นทางสำหรับรถเล็ก ($\le 15\text{ cm}$), รถกระบะยกสูง ($\le 45\text{ cm}$), และเรือท้องแบน ($\ge 25\text{ cm}$)
3. 🏪 **Track 2 — SME & Local Economy (ตัวตบให้เข้าที่):** เปลี่ยนร้านโชห่วยและร้านชำในจุดที่น้ำไม่ท่วมให้เป็น **Micro-Relief Station** รับแลกคูปอง **Smart E-Voucher** จากงบช่วยเหลือของภาครัฐ/เงินบริจาค ช่วยให้ชาวบ้านได้รับเสบียงทันทีโดยไม่ต้องรอของแจกจากส่วนกลาง และสร้างรายได้หมุนเวียนให้ SME ท้องถิ่นตั้งแต่วินาทีแรกที่เกิดวิกฤตจนถึงช่วงฟื้นฟูหลังน้ำลด

---

## 📂 โครงสร้างไฟล์ในโปรเจกต์ (Repository Structure)

```text
├── README.md           # เอกสารแนะนำโครงการ คู่มือการทดสอบระบบ และตารางเทียบเกณฑ์ตัดสิน
├── idea_proposal.md    # เอกสารนำเสนอแนวคิดฉบับสมบูรณ์ (ส่งตรวจในหมวด Idea Markdown)
└── index.html          # เว็บแอปพลิเคชันต้นแบบ Command Center (ส่งตรวจในหมวด HTML Prototype)
```

---

## 🚀 คู่มือการรันและทดสอบ Prototype (`index.html`)

ไฟล์ `index.html` ถูกพัฒนาขึ้นในรูปแบบ **Single-File Web Application** ที่รวม HTML5, Tailwind CSS และ Vanilla JavaScript ไว้ในไฟล์เดียวอย่างสมบูรณ์ สามารถเปิดใช้งานได้ทันทีโดยไม่ต้องติดตั้งไลบรารีหรือรันเซิร์ฟเวอร์เพิ่มเติม

### วิธีเปิดใช้งาน
1. ดับเบิลคลิกไฟล์ `index.html` เพื่อเปิดผ่านเว็บเบราว์เซอร์สมัยใหม่ (Chrome, Edge, Firefox, Safari)
2. หรือเปิดผ่านหน้าต่าง Preview ในระบบตรวจงานของกรรมการได้ทันที

### 🎮 ฟีเจอร์ Interactive ที่แนะนำให้กรรมการทดลองกด (Step-by-Step Demo Guide)

| ลำดับการทดสอบ | สิ่งที่ต้องทำบนหน้าจอ Dashboard | ผลลัพธ์และการทำงานของระบบ (UI Feedback) |
| :--- | :--- | :--- |
| **1. จำลองอนาคตน้ำท่วม (Track 6)** | เลื่อนแถบ **Forecast Horizon Slider** ด้านซ้ายบน จาก `T+0 ชม.` ➔ `T+3 ชม.` ➔ `T+6 ชม.` ➔ `น้ำลด` | • มวลน้ำบนแผนที่ SVG ขยายตัวตามความลึกจริง<br>• ตารางระดับน้ำรายซอยเปลี่ยนสีตามความวิกฤต<br>• แบนเนอร์ AI แจ้งเตือนจำนวนครัวเรือนท้ายซอย 3 ที่ถูกตัดขาด |
| **2. ทดสอบ AI วัดน้ำจากกล้อง (Track 6)** | คลิกปุ่ม **"📷 ดู AI วัดน้ำจากภาพ"** เหนือตารางรายชื่อซอย | • เปิดหน้าต่างจำลอง **Virtual Water Gauge** แสดงการจับภาพขอบฟุตบาท ($15\text{ cm}$) และล้อมอเตอร์ไซค์ ($40\text{ cm}$) เพื่อคำนวณความลึกน้ำโดยไม่ต้องพึ่งเซนเซอร์ราคาแพง |
| **3. สลับยานพาหนะกู้ภัย (Track 5)** | ลองตั้งเวลาที่ `T+3 ชม.` หรือ `T+6 ชม.` แล้วคลิกสลับปุ่ม **🛵 รถเล็ก** / **🛻 กระบะยกสูง** / **🚤 เรือท้องแบน** | • เส้นประนำทางบนแผนที่เปลี่ยนเส้นทางอัตโนมัติ (เช่น รถเล็กถูกบังคับอ้อมไปใช้ทางเลี่ยงเนินสูง ในขณะที่กระบะยกสูงยังลุยผ่านซอย 2 ได้) |
| **4. เบิกเสบียงผ่านร้านชำ (Track 2)** | คลิกปุ่ม **"🎟️ กดแลก E-Voucher"** บนการ์ดร้านค้า SME ด้านขวา | • สต็อกเสบียงของร้านลดลงทีละชุด กองทุนคูปองถูกตัดยอด $\text{฿}300$ และยอด **เงินหมุนเวียนใน SME ท้องถิ่น** เพิ่มขึ้นทันที<br>• *พิเศษ:* หากเลื่อนเวลาไปที่ `T+6 ชม.` ร้านลุงพล (SME #3) จะถูกน้ำท่วมหน้าร้าน $48\text{ cm}$ ระบบจะล็อกปุ่มเบิกของและแจ้งเตือนให้ไปเบิกจากร้านเจ๊หมวย (SME #2 บนที่ดอน) แทน |
| **5. สลับโหมดหน้าแล้ง (Sustainability)** | คลิกปุ่ม **"☀️ สลับดู Peace-Time Mode"** ที่มุมขวาบนของ Header | • แสดงการทำงานของแอปในช่วงเวลาปกติ (ไม่มีน้ำท่วม) ซึ่งทำหน้าที่เป็นระบบรวมออเดอร์ร้านชำและจัดส่งด่วนในชุมชน เพื่อให้ชาวบ้านใช้งานทุกวันและข้อมูลสต็อกเป็นปัจจุบันเสมอ |

---

## 🏆 การตอบโจทย์เกณฑ์การตัดสิน (Judging Criteria Alignment)

### ส่วนที่ 1: Idea (`idea_proposal.md`)
* **1. Novelty and Originality:** นำเสนอแนวคิด *Zero-Hardware Virtual Water Gauge* ลดต้นทุน IoT และเปลี่ยนกระบวนทัศน์การแจกถุงยังชีพเป็นการหมุนเวียนสภาพคล่องผ่าน *Decentralized SME Micro-Relief*
* **2. Problem and Solution Fit:** แก้ปัญหา 3 จุดตายของน้ำท่วมไทย (เตือนภัยกว้างเกินไป / GPS พาไปติดน้ำท่วม / ของบริจาคกระจุกตัวแต่ร้านค้าท้องถิ่นเจ๊ง) ได้ครบใน Loop เดียว
* **3. Impact and Scalability:** ขยายผลได้ทุกชุมชนทั่วประเทศที่มีร้านโชห่วยและกล้องวงจรปิด ลดเวลากู้ภัยหลงซอยและรักษารายได้ผู้ประกอบการรายย่อย
* **4. Technical Feasibility:** สถาปัตยกรรม AI ชัดเจน (YOLOv8 + Depth Estimation + Spatio-Temporal GNN + Dynamic Graph A* Routing) พร้อมสมการคำนวณต้นทุนเส้นทางตามความสูงรถ
* **5. Sustainability and Viability:** มีโมเดล **Dual-Mode Operation (Peace-Time vs. Crisis Mode)** ป้องกันการลบแอปทิ้งหลังน้ำลด พร้อมโมเดลรายได้แบบ B2G (อปท.), CSR Pre-funded Pool และ B2B Risk Data API

### ส่วนที่ 2: HTML Prototype (`index.html`)
* **1. Visual Aesthetic and User Experience:** ออกแบบในธีม *Tactical Dark Mode Command Center* แบ่งสัดส่วน 3 คอลัมน์ตาม 3 แทร็กอย่างชัดเจน อ่านง่ายและใช้งานได้ในหน้าจอเดียว
* **2. Micro-interaction and UI Feedback:** มี Animation การไหลของเส้นทางนำทาง, การขยายตัวของมวลน้ำ, วงแหวนเรดาร์แจ้งเตือนจุดอับสัญญาณ และ Toast Notification ตอบสนองทุกการคลิก
* **3. Code Execution and Stability:** เขียนด้วย Clean Vanilla JavaScript จัดการ State ของเวลา ยานพาหนะ และสต็อกร้านค้าได้อย่างแม่นยำ ปราศจาก Runtime Error
* **4. Content Readability and Basic Organization:** ใช้ฟอนต์ `Kanit` สำหรับภาษาไทยคู่กับ `JetBrains Mono` สำหรับตัวเลขวิศวกรรม จัดกลุ่มข้อมูลด้วย Card & Badge ที่มีสีสื่อความหมายตามระดับความรุนแรง
* **5. HTML Syntax and Document Formatting:** โครงสร้างโค้ดใช้ **Semantic HTML5** (`<header>`, `<nav>`, `<main>`, `<aside>`, `<section>`, `<article>`) พร้อมระบุ ARIA attributes และจัดย่อหน้าอย่างเป็นระเบียบ
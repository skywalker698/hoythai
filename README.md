# Lucky Draw (PWA)

หน้าแอปติดตั้งลงมือถือ/คอมพิวเตอร์ ครอบเว็บ Google Apps Script ไว้ใน iframe (โครงเดียวกับ hubdoc)

## ขึ้น GitHub Pages
1. สร้าง repository ใหม่ แล้วอัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ไว้ที่ root
2. Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save
3. เปิด `https://<ชื่อผู้ใช้>.github.io/<ชื่อ repo>/`

## ติดตั้ง
- Android/Chrome/Edge: มีหน้าต่างและปุ่ม "ติดตั้งเลย" ให้กดอัตโนมัติ
- iOS: แชร์ → เพิ่มไปยังหน้าจอโฮม (แอปมีหน้าสอนขึ้นให้เอง)

## แก้ไข
- ลิงก์ Apps Script: `src` ของ `<iframe id="frame">` ใน `index.html`
- ชื่อแอป: `index.html`, `manifest.webmanifest`
- ทุกครั้งที่แก้ไฟล์ ให้เปลี่ยนเลข `V` ใน `sw.js` (ตอนนี้ lucky-draw-v1) ผู้ใช้จะเห็นแถบ "อัปเดต"

## หมายเหตุฝั่ง Apps Script
`doGet` ต้องมี `.setXFrameOptionsMode(HtmlService.XFrameOptionsMode.ALLOWALL)` และตั้ง Deploy เป็น Anyone ไม่งั้น iframe จะไม่แสดง

วิธีสร้าง APK (ไม่ต้องลง Android Studio)

1) สมัคร/ล็อกอิน github.com แล้วสร้าง Repository ใหม่ (Public หรือ Private ก็ได้)
2) อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ขึ้น repository
   (ต้องมีโฟลเดอร์ .github/workflows/build-apk.yml, www/index.html, package.json, capacitor.config.json)
3) เปิดแท็บ Actions -> เลือก "Build APK" -> กด Run workflow (หรือรอให้รันเองหลังอัปโหลด)
4) รอประมาณ 3-6 นาที เมื่อขึ้นเครื่องหมายถูกสีเขียว เปิดงานนั้นแล้วดาวน์โหลดไฟล์ "calendar-apk" (เป็น zip ข้างในคือ app-debug.apk)
5) ติดตั้ง app-debug.apk บนมือถือ (อนุญาต "ติดตั้งแอปจากแหล่งที่ไม่รู้จัก")

ถ้ามี Android Studio: รัน npm install, npx cap add android, npx cap sync, npx cap open android แล้ว Build > Build APK
แก้หน้าตาแอป: แก้ไฟล์ www/index.html แล้วรัน workflow ใหม่

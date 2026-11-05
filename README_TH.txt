T8R APP - โปรเจกต์ Android

แอปนี้เป็น WebView wrapper สำหรับเปิดเว็บไซต์:
https://charming-sable-8dfcb9.netlify.app

การ Build APK:
1) เปิดโฟลเดอร์นี้ด้วย Android Studio รุ่นที่รองรับ Android Gradle Plugin 8.7.3
2) รอให้ Gradle Sync เสร็จ
3) เลือก Build > Build Bundle(s) / APK(s) > Build APK(s)
4) ไฟล์จะอยู่ที่ app/build/outputs/apk/debug/app-debug.apk

หรือใช้ GitHub Actions:
1) สร้าง repository ใหม่บน GitHub แล้วอัปโหลดไฟล์ทั้งหมดใน ZIP นี้
2) ไปที่แท็บ Actions แล้วรอ workflow "Build T8R APP APK" ทำงาน
3) เปิดผลการทำงานล่าสุดและดาวน์โหลด Artifact ชื่อ T8R-APP-debug
4) แตก ZIP เพื่อรับไฟล์ app-debug.apk

ข้อควรทราบ:
- ต้องมีอินเทอร์เน็ตเพื่อเปิดเว็บไซต์
- ตัวแอปไม่ได้คัดลอกฐานข้อมูลหรือระบบของเว็บไซต์มาไว้ในเครื่อง
- หากเว็บไซต์ต้องเข้าสู่ระบบหรือจำกัดสิทธิ์ ต้องเปิดสิทธิ์ให้มือถือเข้าถึงได้
- การดึงหน้าเว็บไซต์จากระบบตรวจสอบนี้ได้รับ HTTP 401 Unauthorized จึงยังยืนยันไม่ได้ว่าเว็บไซต์เปิดสาธารณะได้ หากมือถือแสดง 401 ให้ตรวจสอบการตั้งค่าการเข้าถึงของ Netlify
- เป็น Debug APK สำหรับทดสอบ ไม่ใช่ไฟล์เผยแพร่ Play Store ที่ผ่านการลงนาม release

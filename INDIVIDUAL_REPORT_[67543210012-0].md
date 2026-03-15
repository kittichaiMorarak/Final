# รายงานรายบุคคล (Individual Report)

รายวิชา: ENGSE207 Software Architecture\
โปรเจกต์: Final Lab Set 1 --- Microservices + HTTPS + Logging

------------------------------------------------------------------------

# สมาชิกคนที่ 1

ชื่อ: กิตติชัย โมรารักษ์
รหัสนักศึกษา: 67543210012-0

## หน้าที่ความรับผิดชอบ

รับผิดชอบการออกแบบสถาปัตยกรรมระบบและการตั้งค่าโครงสร้างโปรเจกต์ รวมถึงการตั้งค่า
Docker และ API Gateway เพื่อให้ทุก service สามารถทำงานร่วมกันได้

## งานที่ดำเนินการ

### 1. ออกแบบสถาปัตยกรรมระบบ

ออกแบบระบบในรูปแบบ Microservices โดยแบ่งบริการออกเป็น - Auth Service - Task
Service - Log Service - Frontend - PostgreSQL Database

และสร้างแผนภาพ Architecture ด้วย draw.io

### 2. ตั้งค่า Docker Compose

สร้างไฟล์ `docker-compose.yml` เพื่อรันทุก service พร้อมกันใน environment เดียว

service ที่ตั้งค่า ได้แก่ - nginx - frontend - auth-service - task-service -
log-service - postgres

### 3. ตั้งค่า Nginx API Gateway

กำหนดให้ Nginx ทำหน้าที่เป็น - Reverse Proxy - TLS Termination - Rate
Limiting - Routing request ไปยัง service ต่าง ๆ

Routing ที่ตั้งค่า เช่น

/api/auth → auth-service\
/api/tasks → task-service\
/api/logs → log-service\
/ → frontend

### 4. ตั้งค่า HTTPS

สร้าง Self-signed Certificate และตั้งค่า TLS ใน Nginx
เพื่อให้ระบบสามารถเข้าถึงผ่าน HTTPS ได้

### 5. ทดสอบระบบ

ทดสอบระบบผ่าน Browser และ Postman เช่น - Login - Create Task - Update
Task - Delete Task - ตรวจสอบ JWT - ตรวจสอบ Log API

------------------------------------------------------------------------


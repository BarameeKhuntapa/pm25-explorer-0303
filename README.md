# PM2.5 Explorer

ระบบสำรวจคุณภาพอากาศ PM2.5 ของประเทศไทย (รายวิชา 1145100 Data Science Toolbox)

## วิธีติดตั้ง

### ด้วย conda (Miniforge)
```bash
conda env create -f environment.yml
conda activate dstoolbox
```

### หรือด้วย uv
```bash
uv sync
```

## ผู้จัดทำ
- นายบารมี ขันเทพา รหัสนักศึกษา 67114540303

## แหล่งข้อมูลและเงื่อนไขการใช้งาน
- **แหล่งที่มา:** ระบบรายงานสถานการณ์คุณภาพอากาศประเทศไทย (Air4Thai) กองจัดการคุณภาพอากาศและเสียง กรมควบคุมมลพิษ กระทรวงทรัพยากรธรรมชาติและสิ่งแวดล้อม (<http://air4thai.pcd.go.th/services/getNewAQI_JSON.php>)
- **การตรวจสอบ `robots.txt`:** ตรวจสอบ `http://air4thai.pcd.go.th/robots.txt` ด้วย `urllib.robotparser.RobotFileParser` พบสถานะ 404 Not Found (`can_fetch` คืนค่า `True`) ไม่มีข้อจำกัดการเข้าถึงสำหรับ User-Agent ของโครงงานนักศึกษา ทั้งนี้ควรดึงข้อมูลอย่างสุภาพ (ระบุ `User-Agent` ที่ชัดเจนและดึงไม่เกินชั่วโมงละ 1 ครั้ง)
- **เงื่อนไขการใช้งาน:** ใช้เพื่อการศึกษาและวิเคราะห์ข้อมูลในรายวิชา 1145100 Data Science Toolbox โดยอ้างอิงแหล่งที่มาจากกรมควบคุมมลพิษเสมอ
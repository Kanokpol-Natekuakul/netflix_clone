# Netflix Clone

เว็บแอปพลิเคชัน Netflix Clone ที่พัฒนาด้วย React และ Vite พร้อมระบบ Authentication และการดึงข้อมูลภาพยนตร์จาก TMDB API

## ✨ ฟีเจอร์หลัก

- 🎬 **แสดงภาพยนตร์** - ดึงข้อมูลภาพยนตร์จาก The Movie Database (TMDB) API
- 🔐 **ระบบเข้าสู่ระบบ** - การสมัครสมาชิกและเข้าสู่ระบบด้วย Firebase Authentication
- 🎥 **เล่นตัวอย่างหนัง** - ดูตัวอย่างภาพยนตร์จาก YouTube
- 📱 **Responsive Design** - รองรับการใช้งานบนอุปกรณ์ต่างๆ
- 🎭 **หมวดหมู่ภาพยนตร์** - แยกประเภทภาพยนตร์ตามความนิยม เรท็ติ้ง และการเข้าฉาย

## 🛠 เทคโนโลยีที่ใช้

- **Frontend Framework**: React 19.1.1
- **Build Tool**: Vite 7.1.2
- **Routing**: React Router DOM 7.8.0
- **Authentication**: Firebase 12.1.0
- **Notifications**: React Toastify 11.0.5
- **Styling**: CSS3 พร้อม Google Fonts (Poppins)
- **API**: The Movie Database (TMDB) API

## 📁 โครงสร้างโปรเจค

```
src/
├── components/
│   ├── Footer/          # คอมโพเนนต์ส่วนท้าย
│   ├── Navbar/          # แถบเมนูด้านบน
│   └── TitleCards/      # การ์ดแสดงภาพยนตร์
├── pages/
│   ├── Home/            # หน้าหลัก
│   ├── Login/           # หน้าเข้าสู่ระบบ
│   └── Player/          # หน้าเล่นวิดีโอ
├── assets/              # รูปภาพและไฟล์สื่อ
├── firebase.js          # การตั้งค่า Firebase
├── App.jsx              # คอมโพเนนต์หลัก
└── main.jsx             # จุดเริ่มต้นแอปพลิเคชัน
```

## 🚀 การติดตั้งและรัน

### ขั้นตอนที่ 1: Clone Repository
```bash
git clone <your-repository-url>
cd netflix-clone
```

### ขั้นตอนที่ 2: ติดตั้ง Dependencies
```bash
npm install
```

### ขั้นตอนที่ 3: ตั้งค่า Environment Variables
สร้างไฟล์ `.env` ในโฟลเดอร์หลัก และเพิ่มข้อมูลต่อไปนี้:

```env
# Firebase Configuration
VITE_FIREBASE_API_KEY=your_firebase_api_key
VITE_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_FIREBASE_PROJECT_ID=your_firebase_project_id
VITE_FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
VITE_FIREBASE_MESSAGING_SENDER_ID=your_messaging_sender_id
VITE_FIREBASE_APP_ID=your_firebase_app_id
```

### ขั้นตอนที่ 4: รันแอปพลิเคชัน
```bash
npm run dev
```

แอปพลิเคชันจะเปิดที่ `http://localhost:5173`

## 📋 คำสั่งที่ใช้ได้

- `npm run dev` - รันเซิร์ฟเวอร์พัฒนา
- `npm run build` - สร้างไฟล์สำหรับ production
- `npm run preview` - ดูตัวอย่าง build ที่สร้างแล้ว
- `npm run lint` - ตรวจสอบโค้ดด้วย ESLint

## 🎯 การใช้งาน

### 1. หน้าแรก (Home)
- แสดงภาพยนตร์แบนเนอร์หลัก
- รายการภาพยนตร์แบ่งตามหมวดหมู่:
  - Blockbuster Movies (หนังยอดนิยม)
  - Only on Netflix (เฉพาะ Netflix)
  - Upcoming (ภาพยนตร์ที่จะเข้าฉาย)
  - Top Picks for You (แนะนำสำหรับคุณ)

### 2. การเข้าสู่ระบบ (Login/Signup)
- สมัครสมาชิกใหม่ด้วย อีเมล รหัสผ่าน และชื่อ
- เข้าสู่ระบบด้วยอีเมลและรหัสผ่าน
- ระบบจดจำการเข้าสู่ระบบ

### 3. เล่นวิดีโอ (Player)
- เล่นตัวอย่างภาพยนตร์จาก YouTube
- แสดงข้อมูลภาพยนตร์ (วันที่เผยแพร่, ชื่อ, ประเภท)

## 🔧 การตั้งค่าเพิ่มเติม

### Firebase Setup
1. สร้างโปรเจคใน [Firebase Console](https://console.firebase.google.com)
2. เปิดใช้งาน Authentication (Email/Password)
3. เปิดใช้งาน Firestore Database
4. คัดลอกข้อมูล configuration ไปใส่ในไฟล์ `.env`

### TMDB API Setup
โปรเจคนี้ใช้ TMDB API สำหรับดึงข้อมูลภาพยนตร์ (API Key ถูกฝังไว้ในโค้ดแล้ว)
หากต้องการใช้ API Key ของตัวเอง:
1. สมัครสมาชิกที่ [TMDB](https://www.themoviedb.org/settings/api)
2. แทนที่ Authorization token ในไฟล์ `TitleCards.jsx` และ `Player.jsx`

## 📱 Responsive Design

แอปพลิเคชันรองรับหน้าจอขนาดต่างๆ:
- **Desktop**: > 1024px
- **Tablet**: 800px - 1024px  
- **Mobile**: < 800px
- **Small Mobile**: < 500px

## 🎨 การปรับแต่ง UI

- ใช้ฟอนต์ **Poppins** จาก Google Fonts
- ธีมสีเข้ม (Dark Theme) เหมือน Netflix
- เอฟเฟคการเลื่อนและ hover ที่ลื่นไหล
- แอนิเมชันและทรานซิชั่น

## ⚠️ ข้อควรระวัง

- ไฟล์ `.env` ต้องอยู่ใน `.gitignore` เพื่อความปลอดภัย
- API Key ของ TMDB ควรเก็บใน environment variables
- ตรวจสอบ Firebase Security Rules สำหรับ production

## 🚀 การ Deploy

### Vercel (แนะนำ)
```bash
npm run build
# อัปโหลดโฟลเดอร์ dist ไปยัง Vercel
```

### Netlify
```bash
npm run build
# อัปโหลดโฟลเดอร์ dist ไปยัง Netlify
```

## 🤝 การพัฒนาต่อ

ฟีเจอร์ที่สามารถเพิ่มได้:
- ระบบค้นหาภาพยนตร์
- รายการโปรด (Watchlist)
- รีวิวและการให้คะแนน
- หน้าโปรไฟล์ผู้ใช้
- หลายภาษา (i18n)

## 📄 License

โปรเจคนี้เป็น Open Source สำหรับการเรียนรู้และพัฒนา

---

**หมายเหตุ**: โปรเจคนี้สร้างขึ้นเพื่อการศึกษา ไม่ใช่เพื่อการใช้งานเชิงพาณิชย์

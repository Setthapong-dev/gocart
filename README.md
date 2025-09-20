# 🛒 GoCart - Full Stack E-commerce Platform

GoCart เป็นแพลตฟอร์ม E-commerce แบบ Full Stack ที่พัฒนาด้วย Next.js 15, Prisma, และ PostgreSQL พร้อมระบบจัดการร้านค้าและผู้ดูแลระบบ

## 🌐 Live Demo

**เว็บไซต์ Live:** [https://gocart-rust.vercel.app/](https://gocart-rust.vercel.app/)

คุณสามารถทดสอบฟีเจอร์ต่างๆ ได้ทันทีที่เว็บไซต์ live!

## ✨ ฟีเจอร์หลัก

### 👥 สำหรับลูกค้า
- 🛍️ **ช้อปปิ้งออนไลน์** - ดูสินค้าและสั่งซื้อได้ง่าย
- 🛒 **ตะกร้าสินค้า** - จัดการสินค้าในตะกร้า
- 📦 **ระบบสั่งซื้อ** - สั่งซื้อสินค้าพร้อมการชำระเงิน
- ⭐ **รีวิวสินค้า** - ให้คะแนนและรีวิวสินค้า
- 🎫 **ระบบคูปอง** - ใช้คูปองส่วนลด
- 📍 **จัดการที่อยู่** - เพิ่มและจัดการที่อยู่จัดส่ง

### 🏪 สำหรับเจ้าของร้าน
- 🏬 **สร้างร้านค้า** - สร้างร้านค้าออนไลน์ของคุณเอง
- 📦 **จัดการสินค้า** - เพิ่ม แก้ไข และจัดการสินค้า
- 📊 **แดชบอร์ด** - ดูสถิติการขายและรายได้
- 📋 **จัดการคำสั่งซื้อ** - ติดตามและจัดการคำสั่งซื้อ
- 🤖 **AI Assistant** - ช่วยสร้างคำอธิบายสินค้าด้วย AI

### 👨‍💼 สำหรับผู้ดูแลระบบ
- ✅ **อนุมัติร้านค้า** - ตรวจสอบและอนุมัติร้านค้าใหม่
- 🎫 **จัดการคูปอง** - สร้างและจัดการคูปองส่วนลด
- 📊 **แดชบอร์ดแอดมิน** - ดูสถิติภาพรวมของระบบ
- 🏪 **จัดการร้านค้า** - เปิด/ปิดร้านค้า

## 🛠️ เทคโนโลยีที่ใช้

### Frontend
- **Next.js 15** - React Framework
- **Tailwind CSS** - CSS Framework
- **Redux Toolkit** - State Management
- **React Hot Toast** - Notifications
- **Lucide React** - Icons

### Backend
- **Next.js API Routes** - Server-side API
- **Prisma** - Database ORM
- **PostgreSQL** - Database (Neon)
- **Clerk** - Authentication
- **Stripe** - Payment Processing

### External Services
- **ImageKit** - Image Management
- **OpenAI** - AI Integration
- **Inngest** - Background Jobs
- **Vercel** - Deployment

## 🚀 การติดตั้งและรันโปรเจค

### ข้อกำหนดเบื้องต้น
- Node.js 18+ 
- npm หรือ yarn
- PostgreSQL Database

### 1. Clone โปรเจค
```bash
git clone <repository-url>
cd gocart_full_stack
```

### 2. ติดตั้ง Dependencies
```bash
npm install
```

### 3. ตั้งค่า Environment Variables
สร้างไฟล์ `.env` และเพิ่มตัวแปรต่อไปนี้:

```env
# Database
DATABASE_URL="your_postgresql_connection_string"
DIRECT_URL="your_direct_postgresql_connection_string"

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your_clerk_publishable_key"
CLERK_SECRET_KEY="your_clerk_secret_key"

# Stripe Payment
STRIPE_SECRET_KEY="your_stripe_secret_key"
STRIPE_WEBHOOK_SECRET="your_stripe_webhook_secret"

# ImageKit
IMAGEKIT_PUBLIC_KEY="your_imagekit_public_key"
IMAGEKIT_PRIVATE_KEY="your_imagekit_private_key"
IMAGEKIT_URL_ENDPOINT="your_imagekit_url_endpoint"

# OpenAI (Optional)
OPENAI_API_KEY="your_openai_api_key"
OPENAI_BASE_URL="your_openai_base_url"

# Inngest
INNGEST_EVENT_KEY="your_inngest_event_key"
INNGEST_SIGNING_KEY="your_inngest_signing_key"

# Admin
ADMIN_EMAIL="your_admin_email"
NEXT_PUBLIC_CURRENCY_SYMBOL="$"
```

### 4. ตั้งค่าฐานข้อมูล
```bash
# Generate Prisma Client
npx prisma generate

# Push schema to database
npx prisma db push
```

### 5. รันโปรเจค
```bash
npm run dev
```

เปิดเบราว์เซอร์ไปที่ [http://localhost:3000](http://localhost:3000)

## 📁 โครงสร้างโปรเจค

```
gocart_full_stack/
├── app/                    # Next.js App Router
│   ├── (public)/          # Public pages
│   ├── admin/             # Admin dashboard
│   ├── store/             # Store management
│   └── api/               # API routes
├── components/            # React components
├── lib/                   # Utilities and configurations
│   ├── features/          # Redux slices
│   └── prisma.js          # Database connection
├── prisma/                # Database schema
├── assets/                # Static assets
└── configs/               # External service configs
```

## 🔧 คำสั่งที่มีประโยชน์

```bash
# Development
npm run dev                 # รัน development server
npm run build              # Build สำหรับ production
npm run start              # รัน production server

# Database
npx prisma studio          # เปิด Prisma Studio
npx prisma db push         # Push schema changes
npx prisma generate        # Generate Prisma client

# Linting
npm run lint               # รัน ESLint
```

## 📱 การใช้งาน

### สำหรับลูกค้า
1. เข้าสู่ระบบด้วย Clerk
2. ดูสินค้าในหน้า Shop
3. เพิ่มสินค้าลงตะกร้า
4. ชำระเงินผ่าน Stripe
5. ติดตามคำสั่งซื้อ

### สำหรับเจ้าของร้าน
1. สร้างร้านค้าใหม่
2. รอการอนุมัติจากแอดมิน
3. เพิ่มสินค้าและจัดการร้านค้า
4. ติดตามคำสั่งซื้อและรายได้

### สำหรับแอดมิน
1. เข้าสู่ระบบด้วยบัญชีแอดมิน
2. อนุมัติร้านค้าใหม่
3. จัดการคูปองและระบบ

## 🤝 การมีส่วนร่วม

เรายินดีรับการมีส่วนร่วมจากทุกคน! กรุณา:

1. Fork โปรเจค
2. สร้าง Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit การเปลี่ยนแปลง (`git commit -m 'Add some AmazingFeature'`)
4. Push ไปยัง Branch (`git push origin feature/AmazingFeature`)
5. เปิด Pull Request

## 📄 License

โปรเจคนี้ใช้ MIT License - ดูรายละเอียดในไฟล์ [LICENSE](LICENSE)

## 📞 ติดต่อ

หากมีคำถามหรือต้องการความช่วยเหลือ กรุณาติดต่อ:
- Email: contact@example.com
- Website: [https://gocart-rust.vercel.app/](https://gocart-rust.vercel.app/)

---

⭐ หากโปรเจคนี้มีประโยชน์ กรุณาให้ดาวน์โหลด (Star) ให้เรา!
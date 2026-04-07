# Taleb Backend - التعليم الإلكتروني

منصة تعليمية متكاملة توفر حلولاً شاملة للطلاب والمعلمين والآباء.

## 🚀 البدء السريع

### المتطلبات
- Node.js >= 14
- PostgreSQL >= 13
- Redis >= 6
- Docker (اختياري)

### التثبيت

```bash
# استنساخ المشروع
git clone https://github.com/yourusername/taleb-backend.git
cd taleb-backend

# تثبيت الحزم
npm install

# إعداد المتغيرات البيئية
cp .env.example .env
```

### بدء الخادم

```bash
# بيئة التطوير
npm run dev

# بيئة الإنتاج
npm start
```

### مع Docker

```bash
docker-compose up -d
```

## 📚 الميزات الرئيسية

- ✅ نظام المصادقة والتفويض
- ✅ إدارة الواجبات والتسليمات
- ✅ نظام الامتحانات والنتائج
- ✅ إدارة الموارد التعليمية
- ✅ نظام الإشعارات
- ✅ إدارة الدرجات

## 🔌 API Endpoints

### المصادقة
- `POST /api/v1/auth/register` - التسجيل
- `POST /api/v1/auth/login` - الدخول
- `GET /api/v1/auth/profile` - الملف الشخصي
- `PUT /api/v1/auth/profile` - تحديث الملف الشخصي
- `POST /api/v1/auth/change-password` - تغيير كلمة المرور

### الطلاب
- `GET /api/v1/students/dashboard` - لوحة التحكم
- `GET /api/v1/students/assignments` - الواجبات
- `POST /api/v1/students/assignments/:id/submit` - تسليم واجب
- `GET /api/v1/students/grades` - الدرجات
- `GET /api/v1/students/exams` - الامتحانات
- `GET /api/v1/students/resources` - الموارد

### المعلمون
- `GET /api/v1/teachers/dashboard` - لوحة التحكم
- `POST /api/v1/teachers/assignments` - إنشاء واجب
- `GET /api/v1/teachers/assignments/:id/submissions` - التسليمات
- `PUT /api/v1/teachers/submissions/:id/grade` - تقييم
- `POST /api/v1/teachers/exams` - إنشاء امتحان
- `POST /api/v1/teachers/resources` - رفع مورد

## 📝 أمثلة الطلبات

### التسجيل
```bash
curl -X POST http://localhost:5000/api/v1/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "email": "student@example.com",
    "password": "password123",
    "firstName": "Ahmed",
    "lastName": "Ali",
    "role": "student"
  }'
```

### الدخول
```bash
curl -X POST http://localhost:5000/api/v1/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "student@example.com",
    "password": "password123"
  }'
```

### الحصول على لوحة التحكم
```bash
curl -X GET http://localhost:5000/api/v1/students/dashboard \
  -H "Authorization: Bearer YOUR_TOKEN"
```

## 🏗️ البنية

```
src/
├── config/       - إعدادات قاعدة البيانات والخادم
├── controllers/  - منطق التطبيق
├── models/       - نماذج قاعدة البيانات
├── routes/       - نقاط نهاية API
├── middleware/   - وسيط معالجة الطلبات
├── utils/        - دوال مساعدة
└── app.js        - ملف التطبيق الرئيسي
```

## 🔐 الأمان

- تشفير كلمات المرور مع bcrypt
- JWT للمصادقة
- CORS محدود
- Rate limiting
- Helmet للحماية من الثغرات

## 📦 التكنولوجيا

- **Express.js** - إطار العمل
- **Sequelize** - ORM
- **PostgreSQL** - قاعدة البيانات
- **Redis** - التخزين المؤقت
- **JWT** - المصادقة
- **Multer** - رفع الملفات

## 📄 الترخيص

MIT

## 👤 المؤلف

Taleb Team

## 💬 التواصل

للمساعدة والاستفسارات: support@taleb.tn
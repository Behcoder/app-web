# 🛒 Seify Market - اپلیکیشن فروشگاه آنلاین

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-3.35.2+-blue?logo=flutter)
![Version](https://img.shields.io/badge/Version-1.6.24-green)
![Platform](https://img.shields.io/badge/Platform-Android%20|%20iOS%20|%20Windows-orange)
![License](https://img.shields.io/badge/License-Private-red)

</div>

## 📋 توضیحات کلی

Seify Market یک اپلیکیشن فروشگاه آنلاین مدرن است که برای فروش انواع محصولات صنعتی از جمله:

- 🔧 لوله‌های فولادی و پلاستیکی
- ⚙️ اتصالات و فیتینگ‌ها  
- 🚿 شیرآلات و تجهیزات بهداشتی
- 🔩 انواع آهن‌آلات و یراق‌آلات
- 🏗️ تجهیزات ساختمانی

## ✨ ویژگی‌های کلیدی

### 🛍️ تجربه خرید
- **جستجوی پیشرفته** محصولات با فیلترهای مختلف
- **دسته‌بندی هوشمند** محصولات
- **نمایش تصاویر با کیفیت** در گالری تعاملی
- **مشاهده جزئیات کامل** محصولات
- **قیمت‌گذاری شفاف** با نمایش تخفیف‌ها

### 🎨 رابط کاربری
- **طراحی Modern Material Design**
- **پشتیبانی کامل از زبان فارسی**
- **اعداد فارسی** در تمام بخش‌ها
- **Responsive Design** برای تمام اندازه صفحه‌ها
- **Navigation ساده** و کاربرپسند

### 🔧 قابلیت‌های فنی
- **API Integration** با WooCommerce
- **Image Caching** برای بهبود عملکرد
- **Error Handling** پیشرفته
- **Multi-Platform Support** (Android, iOS, Windows)
- **Offline Support** محدود

## 🚀 راه‌اندازی پروژه

### پیش‌نیازها

```bash
# نسخه‌های مورد نیاز
Flutter SDK: 3.35.2+
Dart SDK: 3.5.0+
Android SDK: API 21+
iOS: 11.0+
```

### مراحل نصب

1. **کلون کردن پروژه**
```bash
git clone [repository-url]
cd seify_market
```

2. **نصب Dependencies**
```bash
flutter pub get
```

3. **تنظیم فایل محیط (.env)**
```env
WOO_CONSUMER_KEY=ck_your_consumer_key_here
WOO_CONSUMER_SECRET=cs_your_consumer_secret_here
API_BASE_URL=https://seify.ir/wp-json/wc/v3
```

4. **اجرای اپلیکیشن**
```bash
# برای Android
flutter run -d android

# برای iOS
flutter run -d ios

# برای Windows
flutter run -d windows
```

## 📦 ساخت نسخه Production

### Android
```bash
# APK
flutter build apk --release

# App Bundle (برای Google Play)
flutter build appbundle --release
```

### iOS
```bash
flutter build ios --release
```

### Windows
```bash
flutter build windows --release
```

## 🏗️ ساختار پروژه

```
lib/
├── main.dart                 # ورودی اصلی اپ
├── pages/                    # صفحات اپلیکیشن
│   ├── contact_us_page.dart
│   ├── gallery_page.dart
│   ├── search_page.dart
│   └── static_content_page.dart
├── utils/                    # ابزارها و کمکی‌ها
│   ├── price_formatter.dart
│   └── persian_number_formatter.dart
└── assets/
    ├── img/                  # تصاویر
    └── fonts/               # فونت‌ها

zz_beb/                      # مستندات پروژه
├── ERROR_HANDLING_GUIDE.md
└── DEPLOYMENT_README.md
```

## 🔧 تنظیمات مهم

### API Configuration
- **Base URL:** `https://seify.ir/wp-json/wc/v3`
- **Authentication:** WooCommerce Consumer Key/Secret
- **Rate Limiting:** محدودیت درخواست‌های API

### Performance Optimization
- **Image Loading:** Lazy loading با fallback assets
- **API Caching:** کش کردن محدود برای بهبود سرعت
- **Memory Management:** بهینه‌سازی مصرف حافظه

## 🧪 تست و کیفیت

### اجرای تست‌ها
```bash
# تست‌های واحد
flutter test

# آنالیز کد
flutter analyze

# بررسی سلامت Flutter
flutter doctor
```

### کیفیت کد
- **Code Style:** استاندارد Dart/Flutter
- **Comments:** کامنت‌های فارسی برای وضوح بیشتر
- **Error Handling:** مدیریت جامع خطاها

## 📱 پلتفرم‌های پشتیبانی شده

| پلتفرم | وضعیت | حداقل نسخه |
|---------|--------|-------------|
| Android | ✅ آماده | API 21 (Android 5.0) |
| iOS | ✅ آماده | iOS 11.0 |
| Windows | ✅ آماده | Windows 10 |
| Web | ⚠️ محدود | مرورگرهای مدرن |

## 🔒 امنیت

- **API Keys** در فایل `.env` نگهداری می‌شوند
- **HTTPS** برای تمام ارتباطات
- **Input Validation** برای امنیت بیشتر
- **Secret Management** در production

## 📄 مستندات بیشتر

- [راهنمای رفع خطا](zz_beb/ERROR_HANDLING_GUIDE.md)
- [راهنمای Deployment](zz_beb/DEPLOYMENT_README.md)

## 🤝 مشارکت

برای مشارکت در پروژه:

1. Fork کنید
2. Branch جدید ایجاد کنید (`git checkout -b feature/amazing-feature`)
3. تغییرات را commit کنید (`git commit -m 'Add amazing feature'`)
4. Push کنید (`git push origin feature/amazing-feature`)
5. Pull Request ایجاد کنید

## 📞 پشتیبانی و تماس

- **وب‌سایت:** [seify.ir](https://seify.ir)
- **ایمیل:** support@seify.ir
- **تلفن:** ۰۲۱-۱۲۳۴۵۶۷۸

## 📊 آمار پروژه

- **خطوط کد:** ~۲۵۰۰ خط
- **صفحات:** ۱۰+ صفحه
- **ویجت‌ها:** ۵۰+ کامپوننت سفارشی
- **Assets:** ۲۰+ تصویر و آیکون

## 🔄 تاریخچه نسخه‌ها

### v1.6.24 (جاری)
- اصلاح نمایش تصاویر محصولات
- تغییر واحد پولی از تومان به ریال
- بهبود UI و UX
- اضافه کردن صفحه تماس با ما به navigation

### v1.6.21
- پیاده‌سازی ویژگی‌های اولیه
- راه‌اندازی API integration
- طراحی رابط کاربری

---

<div align="center">

**ساخته شده با ❤️ برای بازار ایران**

![Made with Flutter](https://img.shields.io/badge/Made%20with-Flutter-blue?logo=flutter)

</div>

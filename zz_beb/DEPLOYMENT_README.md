# راهنمای استقرار اپ Seify Market

## پیش‌نیازها

### محیط توسعه
- Flutter SDK 3.35.2 یا بالاتر
- Dart SDK
- Android Studio / VS Code
- Git

### وابستگی‌های اصلی
```yaml
dependencies:
  flutter:
    sdk: flutter
  http: ^1.1.0
  carousel_slider: ^4.2.1
  url_launcher: ^6.1.12
  flutter_staggered_grid_view: ^0.7.0
```

## مراحل آماده‌سازی برای Production

### ۱. تنظیمات امنیتی

#### فایل .env
```env
WOO_CONSUMER_KEY=your_consumer_key_here
WOO_CONSUMER_SECRET=your_consumer_secret_here
API_BASE_URL=https://seify.ir/wp-json/wc/v3
```

⚠️ **توجه:** فایل `.env` نباید در Git commit شود

#### API Keys
- کلیدهای API در فایل `.env` قرار داده شوند
- از HTTPS برای تمام درخواست‌ها استفاده شود
- کلیدهای محلی از کلیدهای production جدا باشند

### ۲. تنظیمات Build

#### Android Build
```bash
# ایجاد APK برای Release
flutter build apk --release

# ایجاد App Bundle برای Google Play
flutter build appbundle --release
```

#### iOS Build
```bash
# ایجاد build برای iOS
flutter build ios --release
```

#### Windows Build
```bash
# ایجاد build برای Windows
flutter build windows --release
```

### ۳. تنظیمات Version

#### فایل pubspec.yaml
```yaml
version: 1.6.24
```

#### فایل AndroidManifest.xml
- بروزرسانی `versionCode` و `versionName`
- تنظیم permissions مناسب

### ۴. بهینه‌سازی عملکرد

#### تصاویر
- فشرده‌سازی تصاویر assets
- استفاده از فرمت‌های بهینه (WebP)
- پیاده‌سازی lazy loading

#### API Calls
- پیاده‌سازی caching
- محدودیت تعداد درخواست‌ها
- استفاده از pagination

### ۵. تست‌های پیش از انتشار

#### چک‌لیست تست‌ها
- [ ] تست عملکرد در Android
- [ ] تست عملکرد در iOS
- [ ] تست عملکرد در Windows
- [ ] بررسی responsive design
- [ ] تست اتصال به API
- [ ] تست نمایش تصاویر
- [ ] تست navigation
- [ ] تست جستجو
- [ ] تست صفحه محصولات
- [ ] تست صفحه دسته‌بندی‌ها

#### تست‌های امنیتی
- [ ] بررسی API endpoints
- [ ] تست SSL certificate
- [ ] بررسی input validation
- [ ] تست error handling

### ۶. استقرار

#### Google Play Store
1. ایجاد App Bundle
2. آپلود در Play Console
3. تنظیم metadata
4. انتشار در مراحل (Internal → Alpha → Beta → Production)

#### Apple App Store
1. ایجاد iOS build
2. آپلود در App Store Connect
3. تنظیم App Store metadata
4. ارسال برای بررسی

#### سایر پلتفرم‌ها
- Microsoft Store (برای Windows)
- وب‌سایت شرکت (برای دانلود مستقیم)

### ۷. نظارت و نگهداری

#### لاگ‌ها
- پیاده‌سازی crash reporting
- مانیتورینگ API calls
- ردیابی user analytics

#### بروزرسانی‌ها
- برنامه‌ریزی منظم برای بروزرسانی
- نگهداری compatibility با API
- پیگیری feedback کاربران

## دستورات مفید

```bash
# تمیز کردن build cache
flutter clean

# نصب dependencies
flutter pub get

# اجرای تست‌ها
flutter test

# آنالیز کد
flutter analyze

# بررسی Doctor
flutter doctor

# ایجاد release build برای همه پلتفرم‌ها
flutter build apk --release && flutter build appbundle --release && flutter build windows --release
```

## متغیرهای محیط

### Development
```
DEBUG=true
API_URL=https://seify.ir/wp-json/wc/v3
LOG_LEVEL=debug
```

### Production
```
DEBUG=false
API_URL=https://seify.ir/wp-json/wc/v3
LOG_LEVEL=error
```

## نکات مهم

1. **امنیت:** هرگز کلیدهای API را در کد commit نکنید
2. **عملکرد:** همیشه release build را تست کنید
3. **سازگاری:** با API backend هماهنگ باشید
4. **کیفیت:** تمام features را قبل از release تست کنید
5. **مستندات:** تغییرات را در changelog ثبت کنید

## مشکلات شایع و راه حل‌ها

### Build Failures
- پاک کردن build cache
- بروزرسانی Flutter SDK
- بررسی dependencies conflicts

### Performance Issues
- بهینه‌سازی تصاویر
- کاهش API calls
- پیاده‌سازی caching

### UI/UX Issues
- تست در سایزهای مختلف صفحه
- بررسی Persian font rendering
- تست navigation flow

## اطلاعات تماس

برای مشکلات deployment با تیم DevOps تماس بگیرید.
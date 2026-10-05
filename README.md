# سربازان شاه — وب‌سایت اتحاد

این پروژه یک سایت RTL فارسی، موبایل‌فرست و مدرن برای «سربازان شاه» است.

## اجرا
ساده‌ترین روش:
```bash
python -m http.server 8000
```
سپس `http://localhost:8000` را باز کنید.

## اتصال Firebase
1. در Firebase یک پروژه بسازید.
2. Authentication > Sign-in method > Email/Password را فعال کنید.
3. Firestore Database را ایجاد کنید.
4. تنظیمات Web App را در `js/main.js` و `js/admin.js` جایگزین مقادیر `YOUR_*` کنید.
5. یک حساب مدیر بسازید.
6. برای امنیت واقعی، Custom Claim با نام `admin=true` را برای حساب مدیر تنظیم کنید.
7. قواعد `firebase.rules` را روی Firestore منتشر کنید.
8. منطق ورود پنل را به Firebase Auth متصل کنید و قبل از نمایش dashboard با `onAuthStateChanged` و Claim مدیر احراز هویت انجام دهید.

## نکته امنیتی
قرار دادن رمز مدیر داخل JavaScript یا HTML امن نیست. احراز هویت واقعی باید با Firebase Authentication انجام شود و اجازه نوشتن Firestore فقط از طریق Rules به مدیر داده شود.

## ساختار
- صفحات عمومی: `index.html`, `members.html`, `officials.html`, `ranking.html`, `news.html`, `contact.html`, `about.html`
- پنل: `admin/login.html`, `admin/dashboard.html`
- استایل: `css/style.css`
- اسکریپت عمومی: `js/main.js`
- اسکریپت مدیریت: `js/admin.js`
- قواعد Firestore: `firebase.rules`

## قابلیت‌های ظاهری
ذرات طلایی، گرادیانت متحرک، تاج شناور، Glow عنوان، شمارنده آماری، Reveal، Shimmer، Hover آواتار، هاله کارت‌ها، هدر شیشه‌ای هنگام اسکرول و منوی موبایل در پروژه پیاده‌سازی شده‌اند.

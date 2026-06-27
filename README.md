<div align="center">

  <img src="Preview.png" alt="PGClockPRO Preview" width="900">

  <h1>PGClockPRO</h1>

  <p dir="rtl">
    قالب فارسی/انگلیسی، سبک و شیشه‌ای برای صفحه اشتراک کاربران پاسارگارد
  </p>

  <p>
    <img src="https://img.shields.io/badge/PasarGuard-Compatible-005bb5?style=for-the-badge" alt="PasarGuard">
    <img src="https://img.shields.io/badge/Language-FA%20%7C%20EN-8fc7ff?style=for-the-badge" alt="Language">
    <img src="https://img.shields.io/badge/Theme-Dark%20%7C%20Light-1a1a2e?style=for-the-badge" alt="Theme">
    <img src="https://img.shields.io/badge/Mobile-First-70e49d?style=for-the-badge" alt="Mobile">
  </p>

</div>

---

<div dir="rtl" align="right">

## ویژگی‌ها

- طراحی شیشه‌ای، مدرن و مناسب موبایل
- فارسی (پیش‌فرض) و انگلیسی + تم تاریک/روشن
- اطلاعات اشتراک، نمودار مصرف، هشدار حجم/زمان
- کانفیگ‌ها با کپی، QR و دانلود برای وایرگارد 
- اپلیکیشن‌ها از پنل + تشخیص سیستم‌عامل
---

## ⚠️ تغییر برند (اجباری)

قبل از انتشار، در `index.html` عبارت **`DEFAULT_BRAND`** را پیدا کنید (حدود خط **۱۹۶۴**) و مقادیر دمو را عوض کنید:

</div>

```javascript
var DEFAULT_BRAND = {
  name: "نام برند شما",            // خط 1965 — عنوان هدر
  subtitle: {
    fa: "شعار فارسی",              // خط 1967
    en: "English tagline"          // خط 1968
  },
  logoUrl: "https://example.com/logo.png"  // خط 1970 — خالی = آیکن پیش‌فرض
};
```

<div dir="rtl" align="right">

| فیلد | کار |
|------|-----|
| `name` | نام فروشگاه در بالای صفحه |
| `subtitle.fa` / `subtitle.en` | شعار زیر نام (با زبان عوض می‌شود) |
| `logoUrl` | آدرس لوگو (PNG/SVG، HTTPS یا مسیر `/static/logo.png`) |

اختیاری — عنوان تب مرورگر، **خط ۷**:

</div>

```html
<title>نام برند شما</title>
```

<div dir="rtl" align="right">

---

## نصب سریع

فایل را در مسیر قالب قرار دهید:

</div>

```bash
sudo mkdir -p /var/lib/pasarguard/templates/subscription/
sudo wget -N -P /var/lib/pasarguard/templates/subscription/ https://raw.githubusercontent.com/Mrclocks/PGClockPRO/main/index.html
```

<div dir="rtl" align="right">


فایل `.env` را ویرایش کنید:

</div>

```bash
sudo nano /opt/pasarguard/.env
```

```env
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/pasarguard/templates/"
SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
```

<div dir="rtl" align="right">

ریستارت:

</div>

```bash
sudo pasarguard restart
```

<div dir="rtl" align="right">

---

## نصب روی هاست

فایل‌های نسخه هاست را در root آپلود کنید و `BASE_URL` را تنظیم کنید:

</div>

```javascript
const BASE_URL = 'https://panel-URL:PORT';
```

<div dir="rtl" align="right">

برند را در `index.html` مطابق بخش بالا تغییر دهید.

---

## اعلان و اپلیکیشن‌ها

از پنل پاسارگارد: **تنظیمات → اشتراک** — متن اعلان، لینک پشتیبانی و لیست اپ‌ها. نیازی به ویرایش قالب نیست.

---

<div align="center">

**PGClockPRO**

</div>

</div>

# فایل‌های اکسل دیاگ (منبع به‌روزرسانی)

این ریپو منبع فایل‌های اکسل برنامه **Motorcycle Menu Selector** است.

برنامه هنگام باز شدن، فایل `excel_versions.json` را از اینجا می‌خواند و در صورت وجود نسخهٔ جدید، بعد از تأیید کاربر دانلود می‌کند.

## ساختار

```text
├── excel_versions.json     # مانیفست نسخه‌ها (الزامی)
├── Diag_Menu/              # اکسل‌های منوی دیاگ
│   ├── 18_MotorCycle.xlsm
│   ├── 01_IranKhodro.xlsm
│   ├── 02_Saipa.xlsm
│   └── ...
└── Diag_Database/          # اکسل‌های دیتابیس (در صورت نیاز)
```

## نحوهٔ انتشار نسخهٔ جدید

1. فایل اکسل جدید را در پوشهٔ مربوطه بگذارید (جایگزین کنید).
2. مانیفست را بسازید:

```bash
python make_excel_versions.py --diag Diag_Menu --db Diag_Database --version 1.2.0
```

(اسکریپت `make_excel_versions.py` داخل ریپوی برنامه است.)

3. commit و push:

```bash
git add .
git commit -m "Update Excel files to v1.2.0"
git push
```

## آدرس raw برای تنظیمات برنامه

بعد از ساخت ریپو، در تنظیمات برنامه این آدرس را وارد کنید:

```text
https://raw.githubusercontent.com/USERNAME/REPO_NAME/main
```

جای `USERNAME` و `REPO_NAME` را با مقادیر واقعی عوض کنید.

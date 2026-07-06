# 🕷️ Spider Panel

پنل مدیریت VPN با SPA اختصاصی، بدون دیتای فیک، متصل به API واقعی.

## اجرا

```bash
pip install -r requirements.txt
python main.py
```

آدرس: `http://localhost:8000/dashboard`
رمز پیش‌فرض: `123456`

## امکانات

| بخش | وضعیت |
|------|-------|
| **ورود** | صفحه لاگین با احراز هویت سشن |
| **داشبورد** | آمار واقعی از `/stats` — کاربران فعال، کانفیگ‌ها، ترافیک، uptime |
| **کاربران** | ساخت / حذف / فعال‌غیرفعال / ریست مصرف / مشاهده کانفیگ |
| **کانفیگ‌ها** | ساخت لینک VLESS با محدودیت حجم و انقضا |
| **تنظیمات** | تغییر رمز عبور |

## پروتکل‌ها

- VLESS + WebSocket
- XHTTP Packet-Up / Stream-Up / Stream-One
- VLESS / VMess / Trojan / Shadowsocks (برای کاربران)

## ساختار

```
spider-gateway/
├── main.py              # بک‌اند FastAPI
├── relay_vless.py       # VLESS relay
├── xhttp_siz10.py       # XHTTP transport
├── pages.py             # صفحه اشتراک عمومی
├── static/
│   └── index.html       # SPA اصلی (همه صفحات)
└── requirements.txt
```

اپلیکیشن اصلی یخچال هوشمند - نسخه اولیه رابط کاربری

آپلود در GitHub:
1) ZIP را استخراج کن.
2) همه فایل‌های داخل پوشه را در ریشه مخزن آپلود کن (خود ZIP را آپلود نکن).
3) Settings > Pages > Deploy from a branch > main > /(root) > Save.
4) لینک HTTPS را در Chrome باز کن و Install app / Add to Home Screen را بزن.

امکانات: داشبورد دما، ۱۲ جایگاه تخم‌مرغ، مقدار آب/شیر، هشدارها، حالت نمایشی و بخش تنظیم اتصال سرور.

اتصال واقعی هنوز فعال نیست. برای آن باید API امن HTTPS روی سرور راه‌اندازی شود و ESP8266 داده‌ها را به همان سرور بفرستد. اپ هر ۵ ثانیه API را می‌خواند.

نمونه JSON مورد انتظار API:
{
 "eggs": [true,true,false,true,true,true,false,true,true,false,true,true],
 "temperature": 4.2,
 "liquid": {"type":"water","ml":750,"capacityMl":1500},
 "alerts": ["مقدار آب کم است"],
 "updatedAt": "2026-11-10T12:30:00Z"
}
eggs باید ۱۲ مقدار true/false داشته باشد. liquid.type برابر water یا milk است.
برای امنیت از HTTPS و توکن محدود فقط‌خواندنی استفاده کن. توکن در مرورگر قابل مشاهده است؛ کلید مدیریتی سرور را در این اپ عمومی نگذار.

# Persian Markdown Viewer — خواننده و پیش‌نمایش Markdown فارسی

**[🔗 نسخه‌ی آنلاین / Live demo](https://mohammadgh1370.github.io/persian-markdown-viewer/)**

<div dir="rtl">

ابزار آنلاین خواندن و پیش‌نمایش Markdown برای متن‌های **فارسی، انگلیسی و ترکیبی**. متن Markdown را paste می‌کنید یا فایل `.md` را باز می‌کنید و به شکل صفحه‌ای راست‌چین و خوانا می‌بینید؛ بدون نصب، بدون ثبت‌نام و بدون ارسال متن به سرور.

## چرا این ابزار؟

بیشتر نمایشگرهای Markdown برای کل صفحه یک جهت ثابت چپ‌به‌راست در نظر می‌گیرند. در متن فارسی این یعنی پاراگراف‌ها چپ‌چین می‌شوند، بولت‌ها سمت اشتباه می‌افتند و جمله‌ای که با یک نام فایل یا دستور انگلیسی شروع می‌شود به‌هم می‌ریزد. کد و نمودارهای متنی هم کنار فارسی ناهم‌تراز می‌شوند. این ابزار برای حل همین مشکل‌ها ساخته شده است.

## امکانات

- **تشخیص جهت هر بخش:** پاراگراف، عنوان، آیتم لیست، نقل‌قول و سلول جدول جداگانه راست‌به‌چپ یا چپ‌به‌راست می‌شوند.
- **متن ترکیبی فارسی و انگلیسی:** عبارت انگلیسی وسط جمله‌ی فارسی یک واحد چپ‌به‌راست می‌ماند و علائم نگارشی جابه‌جا نمی‌شوند.
- **کد:** بلوک کد و کد درون‌خطی همیشه چپ‌به‌راست‌اند، رنگ‌آمیزی سینتکس دارند و توضیح فارسی داخل کد جداگانه و درست نمایش داده می‌شود.
- **Markdown استاندارد (GFM):** عنوان‌ها، لیست‌های تودرتو، لیست کارها، جدول (با اسکرول افقی)، نقل‌قول، لینک و تصویر.
- **نمودار متنی:** نمودارهای ساخته‌شده با کاراکترهای جعبه‌ای (┌ │ ▶) که متن فارسی دارند، مرتب و هم‌تراز نمایش داده می‌شوند.
- **فهرست مطالب** از روی عنوان‌ها، با نمایش بخش فعلی، قابل بستن، و نوار پیشرفت خواندن.
- **تنظیمات خواندن:** اندازه‌ی متن، عرض خط، فونت (وزیرمتن یا نسخ) و پوسته (خودکار، روشن، تیره، کاغذی).
- **باز کردن فایل:** دکمه‌ی «باز کردن فایل Markdown» یا کشیدن و رها کردن فایل `.md`، `.markdown` یا `.txt`.

## نحوه استفاده

1. متن Markdown را در کادر صفحه paste کنید (با paste در کادر خالی، نمایش خودکار شروع می‌شود) یا یک فایل `.md` باز کنید.
2. اگر متن را به روش دیگری وارد کرده‌اید، «نمایش برای خواندن» را بزنید (یا `Ctrl+Enter`).
3. با فهرست مطالب بین بخش‌ها جابه‌جا شوید و از «تنظیمات خواندن» ظاهر را تغییر دهید.
4. برای عوض کردن متن، «ویرایش متن» را بزنید.

## حریم خصوصی و امنیت

- متن شما به هیچ سروری ارسال نمی‌شود؛ همه‌چیز در مرورگر پردازش می‌شود.
- فقط آخرین متن و تنظیمات خواندن در حافظه‌ی مرورگر (`localStorage`) نگه داشته می‌شود؛ با «پاک کردن» حذف می‌شود.
- خروجی HTML پیش از نمایش با [DOMPurify](https://github.com/cure53/DOMPurify) پاک‌سازی می‌شود.

## اجرای لوکال

این پروژه فقط یک فایل `index.html` است. آن را مستقیم در مرورگر باز کنید، یا با هر وب‌سرور ساده سرو کنید:

```bash
python3 -m http.server 8080
# سپس http://localhost:8080 را باز کنید
```

برای بارگذاری فونت‌ها و کتابخانه‌ها (از CDN) به اینترنت نیاز دارد.

## فناوری‌ها

[marked](https://github.com/markedjs/marked) (تبدیل Markdown)، [DOMPurify](https://github.com/cure53/DOMPurify) (پاک‌سازی خروجی)، [highlight.js](https://highlightjs.org/) (رنگ‌آمیزی کد)، و فونت‌های [Vazirmatn](https://github.com/rastikerdar/vazirmatn)، Noto Naskh Arabic و JetBrains Mono (هر سه با مجوز OFL).

</div>

---

## English

A browser-based Markdown viewer built for **Persian (Farsi) and mixed Persian–English text**. Paste Markdown or open a `.md` file and read it right-to-left. It runs entirely in your browser; your text is never sent to a server.

**Features**

- Text direction detected per paragraph, heading, list item, blockquote and table cell
- English phrases inside Persian sentences stay intact; punctuation does not jump around
- Code blocks and inline code always stay left-to-right, with syntax highlighting; Persian comments inside code are isolated correctly
- GitHub-flavoured Markdown: tables, task lists, nested lists, blockquotes, links, images
- Box-drawing (ASCII) diagrams that contain Persian text are drawn aligned
- Table of contents (collapsible) with a reading-progress bar
- Reading settings: font size, line width, font (Vazirmatn / Naskh), light / dark / sepia themes
- Open or drag-and-drop `.md`, `.markdown`, `.txt` files

**Run locally:** open `index.html` in a browser, or serve the folder with any static server (`python3 -m http.server`). Fonts and libraries are loaded from CDNs, so an internet connection is needed.

**Built with** marked, DOMPurify, highlight.js, and the Vazirmatn, Noto Naskh Arabic and JetBrains Mono fonts (OFL).

# 🎮 بازی تتریس آنلاین | Online Tetris Game

**🇮🇷 فارسی در ادامه | English below ⬇️**

<div dir="rtl">

## 🧩 بازی تتریس آنلاین — ساخته شده با عشق توسط IntellSoft

یک نسخه کامل و کلاسیک از بازی تتریس که به صورت **کاملاً آنلاین** و **بدون نیاز به هیچ نصب یا افزونه‌ای** در مرورگر شما اجرا می‌شود.  
این پروژه با استانداردهای مدرن وب، طراحی واکنش‌گرا (ریسپانسیو) و بهینه‌سازی کامل برای موتورهای جستجو (SEO) توسعه داده شده است.

[![Website](https://img.shields.io/badge/🌐_سایت_سازنده-intellsoft.ir-blue?style=for-the-badge)](https://intellsoft.ir)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)

---

## ✨ ویژگی‌های برجسته

- 🎯 **گیم‌پلی کلاسیک تتریس** — تمام ۷ قطعه استاندارد (I, O, T, S, Z, J, L) با الگوریتم تصادفی کیسه‌ای (Bag Randomizer).
- 📱 **کاملاً ریسپانسیو** — تجربه عالی در موبایل، تبلت و دسکتاپ. دکمه‌های لمسی اختصاصی برای دستگاه‌های موبایل.
- 🔊 **صداهای داخلی مرورگر** — با استفاده از Web Audio API بدون نیاز به فایل صوتی خارجی.
- 🎨 **طراحی مدرن و شیشه‌ای** — افکت‌های درخشش، سایه‌های عمیق و تم تاریک زیبا.
- 🧠 **سیستم امتیازدهی پویا** — پاداش‌های ویژه برای حذف همزمان چند خط و افزایش سطح با سرعت متغیر.
- 🔄 **قابلیت ذخیره قطعه (Hold)** — قطعه فعلی را برای استفاده بعدی ذخیره کنید.
- 👻 **نمایش قطعه شبح (Ghost)** — موقعیت فرود نهایی قطعه را نشان می‌دهد.
- 🏆 **ذخیره بهترین امتیاز** — بالاترین امتیاز شما در Local Storage مرورگر ذخیره می‌شود.
- ⌨️ **پشتیبانی کامل از کیبورد** — کلیدهای جهت‌دار، Space، C، P و R.
- 🧩 **هیچ وابستگی خارجی ندارد** — بدون CDN، بدون کتابخانه اضافی، فقط HTML, CSS و JavaScript خالص.
- 🔍 **بهینه‌سازی شده برای SEO** — متا تگ‌های کامل، Open Graph، Twitter Card و Schema.org JSON-LD.

---

## 🚀 نسخه آنلاین

می‌توانید همین حالا بازی را در مرورگر خود اجرا کنید:  
فایل `index.html` را باز کنید یا از [سایت رسمی IntellSoft](https://intellsoft.ir) دیدن نمایید.

---

## 🛠️ روش‌های برنامه‌نویسی و تکنولوژی‌ها

این پروژه با فلسفه **سادگی و کارایی بالا** توسعه داده شده است. تمام کد در یک فایل HTML تجمیع شده تا اجرای آن در هر محیطی بدون پیکربندی ممکن باشد.

| بخش | تکنولوژی/روش |
|------|---------------|
| **ساختار** | HTML5 Semantic Elements (`<header>`, `<main>`, `<canvas>`, `<footer>`) |
| **ظاهر و ریسپانسیو** | CSS3 با متغیرهای سفارشی (Custom Properties)، Media Queries و Flexbox/Grid |
| **منطق بازی** | JavaScript ES6+ (بدون TypeScript)، برنامه‌نویسی شیء‌گرا و مبتنی بر حلقه بازی (Game Loop) |
| **صدا** | Web Audio API — نوسان‌سازهای ساده برای ساخت افکت‌های صوتی 8 بیتی |
| **رندرینگ** | Canvas 2D API — رسم مستقیم قطعات، صفحه و افکت‌ها |
| **ذخیره‌سازی** | Local Storage برای نگهداری بهترین امتیاز |
| **دسترسی‌پذیری** | رعایت استانداردهای ARIA، پشتیبانی از `prefers-reduced-motion` |
| **SEO** | Structured Data (JSON-LD)، Open Graph، Twitter Cards، متا تگ‌های کامل |

### منطق اصلی بازی
- **مدیریت تخته (Board):** یک آرایه دو بعدی `10x20` که رنگ هر سلول را ذخیره می‌کند.
- **تصادفی‌سازی قطعات:** از الگوریتم "Bag" استفاده می‌شود؛ هر ۷ قطعه یک بار و سپس کیسه جدید تولید می‌شود تا بازیکن هرگز پشت سر هم قطعه تکراری نگیرد.
- **تشخیص برخورد:** بررسی هر سلول ماتریس قطعه با دیوارها، کف و خانه‌های پر تخته.
- **حلقه بازی (Game Loop):** با `requestAnimationFrame` و تایمر متغیر برای سقوط تدریجی. سرعت با بالا رفتن سطح کاهش می‌یابد.
- **سیستم چرخش:** چرخش ۹۰ درجه در جهت عقربه‌های ساعت و تلاش برای wall kick (جابجایی‌های کوچک) در صورت برخورد با دیوار.
- **قطعه شبح:** با شبیه‌سازی سقوط مستقیم و بررسی برخورد، موقعیت نهایی نمایش داده می‌شود.

---

## 📸 پیش‌نمایش

<div align="center">
  <img src="https://via.placeholder.com/600x400/0a0a1a/ffffff?text=Tetris+Online+Game+by+IntellSoft" alt="پیش‌نمایش بازی تتریس آنلاین" style="border-radius:12px; box-shadow:0 0 20px rgba(0,0,0,0.5);" />
  <p><em>تصویر از محیط بازی تتریس آنلاین</em></p>
</div>

---

## 📂 ساختار پروژه
tetris-online/
├── index.html ← تمام کدها (HTML, CSS, JavaScript) در یک فایل
├── README.md ← همین مستند
└── (بدون هیچ فایل دیگری)


---

## ⚡ اجرا در لوکال

نیازی به نصب هیچ چیز نیست!  
فقط فایل `index.html` را با مرورگر دلخواه خود باز کنید.  
بازی به‌طور خودکار راه‌اندازی می‌شود و می‌توانید کلیدهای کیبورد یا دکمه‌های لمسی را استفاده کنید.

---

## 🤝 مشارکت و توسعه

ایده‌ها و پیشنهادات شما همیشه خوش‌آمد است.  
اگر مایل به بهبود بازی هستید، می‌توانید مخزن را Fork کرده و Pull Request ارسال کنید.  
لطفاً پیش از اعمال تغییرات بزرگ، موضوع (Issue) را باز کنید تا درباره آن بحث کنیم.

---

## 📄 مجوز

این پروژه تحت مجوز MIT منتشر شده است.  
شما آزادید که از آن استفاده کنید، تغییر دهید و توزیع نمایید، به شرط آنکه نام و لینک به سازنده اصلی حفظ شود.

---

## 🔗 ارتباط با سازنده

🌐 **وب‌سایت رسمی:** [https://intellsoft.ir](https://intellsoft.ir)  
🐙 **گیت‌هاب:** [github.com/intellsoft-ir](https://github.com/intellsoft-ir) (لینک خود را جایگزین کنید)  
📧 ایمیل: info@intellsoft.ir  

> ساخته شده با ❤️ توسط **IntellSoft** — همراه شما در دنیای نرم‌افزارهای هوشمند

---

</div>

---

# 🎮 Online Tetris Game — Crafted with ❤️ by IntellSoft

A fully classic Tetris game that runs **completely online** in your browser — no installation, no plugins required.  
Developed with modern web standards, fully responsive design, and search engine optimized (SEO) from the ground up.

[![Website](https://img.shields.io/badge/🌐_Creator_Site-intellsoft.ir-blue?style=for-the-badge)](https://intellsoft.ir)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](#)

---

## ✨ Key Features

- 🎯 **Classic Tetris gameplay** — All 7 standard tetrominoes with a Bag Randomizer algorithm.
- 📱 **Fully responsive** — Outstanding experience on mobile, tablet, and desktop. Dedicated touch controls for mobile devices.
- 🔊 **In-browser sounds** — Generated on the fly using Web Audio API, no external audio files needed.
- 🎨 **Modern glassmorphism design** — Glowing effects, deep shadows, and a beautiful dark theme.
- 🧠 **Dynamic scoring system** — Bonuses for multi-line clears (Tetris, etc.) and increasing level with variable speed.
- 🔄 **Hold piece feature** — Store the current piece for later use.
- 👻 **Ghost piece preview** — Shows exactly where the piece will land.
- 🏆 **Persistent high score** — Saved in browser's Local Storage.
- ⌨️ **Full keyboard support** — Arrow keys, Space, C, P, and R.
- 🧩 **Zero external dependencies** — No CDN, no libraries, just pure HTML, CSS, and JavaScript.
- 🔍 **SEO-optimized** — Complete meta tags, Open Graph, Twitter Cards, and JSON-LD structured data.

---

## 🚀 Live Demo

You can play the game right now by opening the `index.html` file in your browser, or visit the official [IntellSoft website](https://intellsoft.ir).

---

## 🛠️ Programming Approaches & Tech Stack

This project follows a philosophy of **simplicity and high performance**. All code is consolidated into a single HTML file for effortless deployment anywhere.

| Aspect | Technology/Method |
|--------|-------------------|
| **Structure** | HTML5 Semantic Elements (`<header>`, `<main>`, `<canvas>`, `<footer>`) |
| **Styling & Responsive** | CSS3 with Custom Properties, Media Queries, Flexbox/Grid |
| **Game Logic** | Vanilla JavaScript ES6+ (no TypeScript), Object-oriented and Game Loop based |
| **Audio** | Web Audio API — Simple oscillators for 8-bit style sound effects |
| **Rendering** | Canvas 2D API — Direct drawing of pieces, board, and effects |
| **Storage** | Local Storage for high score persistence |
| **Accessibility** | ARIA standards, `prefers-reduced-motion` support |
| **SEO** | Structured Data (JSON-LD), Open Graph, Twitter Cards, comprehensive meta tags |

### Core Game Logic
- **Board Management:** A 10x20 two-dimensional array stores the color of each cell.
- **Randomizer:** The "Bag" system is used; all 7 pieces appear once per bag, then a new bag is generated, ensuring no long droughts.
- **Collision Detection:** Checks each cell of the piece matrix against walls, floor, and filled cells of the board.
- **Game Loop:** Uses `requestAnimationFrame` with a variable timer for gradual falling. Speed increases with level.
- **Rotation System:** 90-degree clockwise rotation with wall kick attempts (small offsets) when near walls.
- **Ghost Piece:** Simulates straight-drop to calculate and display the final landing position.

---

## 📸 Preview

<div align="center">
  <img src="https://via.placeholder.com/600x400/0a0a1a/ffffff?text=Tetris+Online+Game+by+IntellSoft" alt="Online Tetris Game Screenshot" style="border-radius:12px; box-shadow:0 0 20px rgba(0,0,0,0.5);" />
  <p><em>Screenshot of the Online Tetris Game</em></p>
</div>

---

## 📂 Project Structure
tetris-online/
├── index.html ← All code (HTML, CSS, JavaScript) in one file
├── README.md ← This documentation
└── (no other files)


---

## ⚡ Running Locally

No installation required!  
Simply open the `index.html` file in any modern browser.  
The game starts automatically, and you can use keyboard or touch controls.

---

## 🤝 Contributing

Ideas and suggestions are always welcome.  
If you'd like to improve the game, feel free to fork the repository and submit a pull request.  
Please open an issue first to discuss any major changes.

---

## 📄 License

This project is licensed under the MIT License.  
You are free to use, modify, and distribute it, provided that credit and a link to the original author are maintained.

---

## 🔗 Connect with the Creator

🌐 **Official Website:** [https://intellsoft.ir](https://intellsoft.ir)  
🐙 **GitHub:** [github.com/intellsoft-ir](https://github.com/intellsoft-ir) (replace with your actual link)  
📧 Email: info@intellsoft.ir  

> Built with ❤️ by **IntellSoft** — your partner in intelligent software solutions

---

⭐ اگر این پروژه را دوست داشتید، حتماً به آن ستاره دهید! | If you liked this project, please give it a star! ⭐

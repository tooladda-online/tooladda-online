<div align="center">

<img src="https://tooladda.online/assets/images/logo.svg" alt="ToolAdda" width="88" height="88" />

# ToolAdda

### 139 free, fast, browser-based tools — no sign-up, no upload, no watermark, no limits.

[![Visit ToolAdda](https://img.shields.io/badge/Visit-tooladda.online-4f46e5?style=for-the-badge&logo=google-chrome&logoColor=white)](https://tooladda.online)
[![Tools](https://img.shields.io/badge/Tools-139-7c3aed?style=for-the-badge)](https://tooladda.online)
[![Repos](https://img.shields.io/badge/Tool%20repos-115-38bdf8?style=for-the-badge&logo=github&logoColor=white)](https://github.com/orgs/tooladda-online/repositories)
[![Price](https://img.shields.io/badge/100%25-Free-10b981?style=for-the-badge)](https://tooladda.online)
[![Client side](https://img.shields.io/badge/Processing-Client--side-f59e0b?style=for-the-badge&logo=javascript&logoColor=white)](#-privacy--the-processing-model)

**This is the main repository of the [`tooladda-online`](https://github.com/tooladda-online) organisation.**
Every other repo in the org is one tool from this site — the full map is [below](#-repository-map).

[🚀 **Open ToolAdda →**](https://tooladda.online) &nbsp;·&nbsp; [📚 Tool guide](https://tooladda.online/blog.html) &nbsp;·&nbsp; [🤖 llms.txt](https://tooladda.online/llms.txt) &nbsp;·&nbsp; [✉️ Contact](https://tooladda.online/contact.html)

</div>

---

## 📌 What ToolAdda is

ToolAdda ([tooladda.online](https://tooladda.online)) is a free online utility platform: PDF tools, image tools,
HR and payroll documents, India-first finance calculators, developer utilities, text processing, chemistry,
SEO, networking and a handful of browser games — **139 tools in total**.

The point of difference is where the work happens. Almost every tool runs **entirely in the visitor's own
browser**: files are read with the File API, processed in JavaScript or WebAssembly on the device, and written
straight back to the downloads folder. There is no upload step, no server-side storage, no account, no email
gate, no trial, no paywalled export and no watermark.

| | |
|---|---|
| ⚡ **Instant** | Static pages, no framework, no hydration — the tool is usable the moment the page paints |
| 🔒 **Private by default** | A salary sheet, a signed contract, a passport photo or a private key never leaves the device |
| 💸 **Free, unlimited** | No sign-up, no quota, no watermark. Ads pay for it; they never gate a feature |
| 📱 **Works everywhere** | Desktop and mobile browsers; 10 tools keep working fully offline |
| 🇮🇳 **India-first finance** | EPF, ESI, state-wise professional tax, GST, both income-tax regimes, PPF, SIP, lakh/crore formatting |

---

## 🔐 Privacy — the processing model

The default is client-side, and the exceptions are stated precisely rather than glossed over. These tools
**must** reach the network, because querying the public internet is their entire purpose:

| Tool | What leaves the browser |
|---|---|
| [DNS Lookup](https://tooladda.online/dns-lookup.html) | The domain, to Google Public DNS (`dns.google`) with a Cloudflare DoH fallback |
| [DNS Propagation Checker](https://tooladda.online/dns-propagation-checker.html) | The domain, to four independent resolvers — Google, Cloudflare, DNS.SB, RethinkDNS |
| [SSL Checker](https://tooladda.online/ssl-checker.html) | The hostname, to the `networkcalc.com` certificate API (CORS-proxy fallback) |
| [Website SEO Checker](https://tooladda.online/website-seo-checker.html) | The submitted URL, fetched through one of three CORS proxies |
| [Internet Speed Test](https://tooladda.online/internet-speed-test.html) | Measurement traffic to Cloudflare's speed endpoints (jsDelivr / httpbin / postman-echo fallbacks) |
| [URL Shortener](https://tooladda.online/url-shortener.html) | The long URL, to public shorteners (da.gd, is.gd, v.gd, TinyURL), possibly via an anonymous CORS proxy — the least private tool on the site |
| Optional "import from URL" fields | The browser fetches the URL the user typed directly; nothing is uploaded to ToolAdda |

Everything else — all PDF, image, resume, payroll, cryptographic-key and calculator tools — completes without
sending user content anywhere. Separately: many tools load their **libraries** from public CDNs (cdnjs,
jsDelivr) — that is code delivery, not user data, but it does mean most tools need connectivity on first load.

### Genuinely offline tools

Ten tools register a narrow-scoped service worker and keep working with no connection after the first visit:

[Flatten PDF](https://tooladda.online/flatten-pdf.html) ·
[Text to Handwriting](https://tooladda.online/text-to-handwriting.html) ·
[Online Notepad](https://tooladda.online/online-notepad.html) ·
[Minesweeper](https://tooladda.online/minesweeper.html) ·
[Poster Printer](https://tooladda.online/poster-printer.html) ·
[Scientific Calculator](https://tooladda.online/scientific-calculator.html) ·
[Salary Slip Generator](https://tooladda.online/salary-slip-generator.html) ·
[Rent Receipt Generator](https://tooladda.online/rent-receipt-generator.html) ·
[Epoch Converter](https://tooladda.online/epoch-converter.html) ·
[Offline Invoice Generator](https://tooladda.online/invoice-generator.html)

> Each worker is registered with an explicit single-page scope (`/flatten-pdf.html`, not `/`), so a cached
> game can never end up serving the rest of the site from a stale cache.

---

## 🗺️ Repository map

The organisation is deliberately flat: **this repo is the site**, and every other repo is **one tool**.

```
tooladda-online/
├── tooladda-online/          ← you are here — the full site, the source of truth
├── qr-code-generator/        ← one repo per tool: landing README + link to the live page
├── image-resizer/
├── salary-slip-generator/
├── … 112 more tool repos
```

- **115 tool repos**, each named after the tool's URL slug (`https://tooladda.online/<slug>.html` →
  `github.com/tooladda-online/<slug>`).
- Each one carries a README describing that single tool — what it does, why it's private, and a direct link
  to the live page. They are discovery surfaces, not forks: the code always lives here.
- Browse them all: **[github.com/orgs/tooladda-online/repositories](https://github.com/orgs/tooladda-online/repositories)**

---

## 🧰 The full tool directory

139 tools, grouped the way the site's own search and navigation group them. Click a category to expand.
A dash in the **Repo** column means that tool does not have its own repo in the org yet.

<details>
<summary><b>Developer</b> — 38 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| ⚙️ .htaccess Generator | [tooladda.online/developer-tools/htaccess-generator.html](https://tooladda.online/developer-tools/htaccess-generator.html) | [`htaccess-generator`](https://github.com/tooladda-online/htaccess-generator) |
| 🍱 Bento Grid Generator | [tooladda.online/css-tools/bento-grid-generator.html](https://tooladda.online/css-tools/bento-grid-generator.html) | — |
| ⏱️ Cron Expression Generator | [tooladda.online/cron-expression-generator.html](https://tooladda.online/cron-expression-generator.html) | [`cron-expression-generator`](https://github.com/tooladda-online/cron-expression-generator) |
| 📐 CSS Flexbox & Grid Playground | [tooladda.online/css-tools/css-flexbox-grid-playground.html](https://tooladda.online/css-tools/css-flexbox-grid-playground.html) | — |
| 🪟 CSS Glassmorphism UI Builder | [tooladda.online/css-tools/css-glassmorphism-ui-builder.html](https://tooladda.online/css-tools/css-glassmorphism-ui-builder.html) | — |
| 🗿 CSS Neumorphic Element Designer | [tooladda.online/css-tools/css-neumorphic-element-designer.html](https://tooladda.online/css-tools/css-neumorphic-element-designer.html) | — |
| 🧩 CSS to Tailwind Converter | [tooladda.online/css-to-tailwind.html](https://tooladda.online/css-to-tailwind.html) | [`css-to-tailwind`](https://github.com/tooladda-online/css-to-tailwind) |
| 📈 CSV to Interactive Chart | [tooladda.online/csv-to-interactive-chart.html](https://tooladda.online/csv-to-interactive-chart.html) | — |
| 🗄️ CSV to JSON Converter | [tooladda.online/csv-to-json-converter.html](https://tooladda.online/csv-to-json-converter.html) | [`csv-to-json-converter`](https://github.com/tooladda-online/csv-to-json-converter) |
| 🌐 DNS Lookup | [tooladda.online/dns-lookup.html](https://tooladda.online/dns-lookup.html) | [`dns-lookup`](https://github.com/tooladda-online/dns-lookup) |
| 🔎 DNS Propagation Checker | [tooladda.online/dns-propagation-checker.html](https://tooladda.online/dns-propagation-checker.html) | [`dns-propagation-checker`](https://github.com/tooladda-online/dns-propagation-checker) |
| 🕐 Epoch / Unix Timestamp Converter | [tooladda.online/epoch-converter.html](https://tooladda.online/epoch-converter.html) | [`epoch-converter`](https://github.com/tooladda-online/epoch-converter) |
| 🎨 Favicon Generator | [tooladda.online/favicon-generator.html](https://tooladda.online/favicon-generator.html) | [`favicon-generator`](https://github.com/tooladda-online/favicon-generator) |
| 🕵️ Image Steganography | [tooladda.online/image-steganography.html](https://tooladda.online/image-steganography.html) | [`image-steganography`](https://github.com/tooladda-online/image-steganography) |
| 🌐 IP Subnet Calculator | [tooladda.online/ip-subnet-calculator.html](https://tooladda.online/ip-subnet-calculator.html) | [`ip-subnet-calculator`](https://github.com/tooladda-online/ip-subnet-calculator) |
| 🧩 JSON Formatter | [tooladda.online/developer-tools/json-formatter.html](https://tooladda.online/developer-tools/json-formatter.html) | [`json-formatter`](https://github.com/tooladda-online/json-formatter) |
| 🧾 JSON to CSV Converter | [tooladda.online/json-to-csv-converter.html](https://tooladda.online/json-to-csv-converter.html) | [`json-to-csv-converter`](https://github.com/tooladda-online/json-to-csv-converter) |
| 🧬 JSON to TypeScript | [tooladda.online/developer-tools/json-to-typescript.html](https://tooladda.online/developer-tools/json-to-typescript.html) | [`json-to-typescript`](https://github.com/tooladda-online/json-to-typescript) |
| 🧩 JSON to XML Converter | [tooladda.online/json-to-xml-converter.html](https://tooladda.online/json-to-xml-converter.html) | [`json-to-xml-converter`](https://github.com/tooladda-online/json-to-xml-converter) |
| 🔁 JSON to YAML | [tooladda.online/developer-tools/json-to-yaml.html](https://tooladda.online/developer-tools/json-to-yaml.html) | [`json-to-yaml`](https://github.com/tooladda-online/json-to-yaml) |
| 🔐 JWT Debugger | [tooladda.online/jwt-debugger.html](https://tooladda.online/jwt-debugger.html) | [`jwt-debugger`](https://github.com/tooladda-online/jwt-debugger) |
| 🔏 JWT Encoder | [tooladda.online/jwt-encoder.html](https://tooladda.online/jwt-encoder.html) | [`jwt-encoder`](https://github.com/tooladda-online/jwt-encoder) |
| 👁️ Markdown Live Previewer | [tooladda.online/developer-tools/markdown-live-previewer.html](https://tooladda.online/developer-tools/markdown-live-previewer.html) | — |
| 📝 Markdown to HTML | [tooladda.online/markdown-to-html.html](https://tooladda.online/markdown-to-html.html) | [`markdown-to-html`](https://github.com/tooladda-online/markdown-to-html) |
| 🗒️ Markdown to Notion | [tooladda.online/developer-tools/markdown-to-notion.html](https://tooladda.online/developer-tools/markdown-to-notion.html) | [`markdown-to-notion`](https://github.com/tooladda-online/markdown-to-notion) |
| 🔐 Password Strength Checker | [tooladda.online/password-strength-checker.html](https://tooladda.online/password-strength-checker.html) | [`password-strength-checker`](https://github.com/tooladda-online/password-strength-checker) |
| 🔐 PEM to PPK Converter | [tooladda.online/pem-to-ppk.html](https://tooladda.online/pem-to-ppk.html) | [`pem-to-ppk`](https://github.com/tooladda-online/pem-to-ppk) |
| 📏 Pixel-Perfect Screen Ruler | [tooladda.online/screen-ruler.html](https://tooladda.online/screen-ruler.html) | [`screen-ruler`](https://github.com/tooladda-online/screen-ruler) |
| 🔐 PPK to PEM Converter | [tooladda.online/ppk-to-pem.html](https://tooladda.online/ppk-to-pem.html) | [`ppk-to-pem`](https://github.com/tooladda-online/ppk-to-pem) |
| 🔤 Regex Tester | [tooladda.online/regex-tester.html](https://tooladda.online/regex-tester.html) | — |
| 🤖 robots.txt Generator & Tester | [tooladda.online/robots-txt-generator.html](https://tooladda.online/robots-txt-generator.html) | [`robots-txt-generator`](https://github.com/tooladda-online/robots-txt-generator) |
| 🎬 Scroll Animation Keyframe Builder | [tooladda.online/css-tools/scroll-animation-keyframe-builder.html](https://tooladda.online/css-tools/scroll-animation-keyframe-builder.html) | — |
| ✨ SVG Optimizer | [tooladda.online/svg-optimizer.html](https://tooladda.online/svg-optimizer.html) | [`svg-optimizer`](https://github.com/tooladda-online/svg-optimizer) |
| 🔗 URL Encoder / Decoder | [tooladda.online/url-encoder-decoder.html](https://tooladda.online/url-encoder-decoder.html) | — |
| 🔗 URL Shortener | [tooladda.online/url-shortener.html](https://tooladda.online/url-shortener.html) | [`url-shortener`](https://github.com/tooladda-online/url-shortener) |
| 🧬 UUID Generator | [tooladda.online/uuid-generator.html](https://tooladda.online/uuid-generator.html) | [`uuid-generator`](https://github.com/tooladda-online/uuid-generator) |
| 📦 XML to JSON Converter | [tooladda.online/xml-to-json-converter.html](https://tooladda.online/xml-to-json-converter.html) | [`xml-to-json-converter`](https://github.com/tooladda-online/xml-to-json-converter) |
| 🧬 YAML to XML Converter | [tooladda.online/developer-tools/yaml-to-xml.html](https://tooladda.online/developer-tools/yaml-to-xml.html) | [`yaml-to-xml`](https://github.com/tooladda-online/yaml-to-xml) |

</details>

<details>
<summary><b>Image</b> — 24 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 📊 Barcode Generator | [tooladda.online/barcode-generator.html](https://tooladda.online/barcode-generator.html) | [`barcode-generator`](https://github.com/tooladda-online/barcode-generator) |
| 🗜️ Compress Image to Exact KB | [tooladda.online/image-compress-to-kb.html](https://tooladda.online/image-compress-to-kb.html) | [`image-compress-to-kb`](https://github.com/tooladda-online/image-compress-to-kb) |
| 📱 Custom QR Code Maker | [tooladda.online/custom-qr-code-maker.html](https://tooladda.online/custom-qr-code-maker.html) | [`custom-qr-code-maker`](https://github.com/tooladda-online/custom-qr-code-maker) |
| 🛡️ EXIF Metadata Remover | [tooladda.online/exif-metadata-remover.html](https://tooladda.online/exif-metadata-remover.html) | — |
| ⚫ Grayscale Image Converter | [tooladda.online/image-grayscale.html](https://tooladda.online/image-grayscale.html) | [`image-grayscale`](https://github.com/tooladda-online/image-grayscale) |
| 📸 HEIC to JPG/PNG Converter | [tooladda.online/heic-converter.html](https://tooladda.online/heic-converter.html) | [`heic-converter`](https://github.com/tooladda-online/heic-converter) |
| 🪄 Image Background Remover | [tooladda.online/image-background-remover.html](https://tooladda.online/image-background-remover.html) | [`image-background-remover`](https://github.com/tooladda-online/image-background-remover) |
| 🌫️ Image Blur Tool | [tooladda.online/image-blur.html](https://tooladda.online/image-blur.html) | [`image-blur`](https://github.com/tooladda-online/image-blur) |
| 🎨 Image Color Picker | [tooladda.online/image-color-picker.html](https://tooladda.online/image-color-picker.html) | [`image-color-picker`](https://github.com/tooladda-online/image-color-picker) |
| 🗜️ Image Compressor | [tooladda.online/image-compressor.html](https://tooladda.online/image-compressor.html) | [`image-compressor`](https://github.com/tooladda-online/image-compressor) |
| ✂️ Image Crop Tool | [tooladda.online/image-crop.html](https://tooladda.online/image-crop.html) | [`image-crop`](https://github.com/tooladda-online/image-crop) |
| 📐 Image Resizer | [tooladda.online/image-resizer.html](https://tooladda.online/image-resizer.html) | [`image-resizer`](https://github.com/tooladda-online/image-resizer) |
| ↻ Image Rotate Tool | [tooladda.online/image-rotate.html](https://tooladda.online/image-rotate.html) | [`image-rotate`](https://github.com/tooladda-online/image-rotate) |
| 🖼️ Images to PDF | [tooladda.online/images-to-pdf.html](https://tooladda.online/images-to-pdf.html) | [`images-to-pdf`](https://github.com/tooladda-online/images-to-pdf) |
| 🖼️ JPG to PNG Converter | [tooladda.online/jpg-to-png.html](https://tooladda.online/jpg-to-png.html) | [`jpg-to-png`](https://github.com/tooladda-online/jpg-to-png) |
| 🪪 Passport Size Photo Maker | [tooladda.online/passport-photo-maker.html](https://tooladda.online/passport-photo-maker.html) | [`passport-photo-maker`](https://github.com/tooladda-online/passport-photo-maker) |
| 🔁 PNG to WebP Converter | [tooladda.online/png-to-webp.html](https://tooladda.online/png-to-webp.html) | [`png-to-webp`](https://github.com/tooladda-online/png-to-webp) |
| 🖨️ Poster Printer | [tooladda.online/poster-printer.html](https://tooladda.online/poster-printer.html) | [`poster-printer`](https://github.com/tooladda-online/poster-printer) |
| 🪪 Printable ID Card Maker | [tooladda.online/cyber-tools/id-card-sheet-generator.html](https://tooladda.online/cyber-tools/id-card-sheet-generator.html) | — |
| ▦ QR & Barcode Label Sheet Generator | [tooladda.online/qr-barcode-label-sheet-generator.html](https://tooladda.online/qr-barcode-label-sheet-generator.html) | — |
| 📱 QR Code Generator | [tooladda.online/qr-code-generator.html](https://tooladda.online/qr-code-generator.html) | [`qr-code-generator`](https://github.com/tooladda-online/qr-code-generator) |
| 🔍 QR Code Scanner | [tooladda.online/qr-code-scanner.html](https://tooladda.online/qr-code-scanner.html) | [`qr-code-scanner`](https://github.com/tooladda-online/qr-code-scanner) |
| ✍️ Signature Resizer | [tooladda.online/signature-resizer.html](https://tooladda.online/signature-resizer.html) | [`signature-resizer`](https://github.com/tooladda-online/signature-resizer) |
| 🖼️ SVG to PNG / JPG / WebP | [tooladda.online/svg-to-png-converter.html](https://tooladda.online/svg-to-png-converter.html) | — |

</details>

<details>
<summary><b>PDF</b> — 19 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 💧 Add Watermark to PDF | [tooladda.online/pdf-watermark.html](https://tooladda.online/pdf-watermark.html) | [`pdf-watermark`](https://github.com/tooladda-online/pdf-watermark) |
| 🎱 Bingo Card Generator | [tooladda.online/bingo-card-generator.html](https://tooladda.online/bingo-card-generator.html) | [`bingo-card-generator`](https://github.com/tooladda-online/bingo-card-generator) |
| 🔍 Compare Two PDFs | [tooladda.online/compare-pdfs.html](https://tooladda.online/compare-pdfs.html) | [`compare-pdfs`](https://github.com/tooladda-online/compare-pdfs) |
| 🪑 Exam Seating Arrangement Planner | [tooladda.online/exam-seating-planner.html](https://tooladda.online/exam-seating-planner.html) | — |
| 🧾 Flatten PDF | [tooladda.online/flatten-pdf.html](https://tooladda.online/flatten-pdf.html) | [`flatten-pdf`](https://github.com/tooladda-online/flatten-pdf) |
| 🧾 HTML to PDF | [tooladda.online/html-to-pdf.html](https://tooladda.online/html-to-pdf.html) | [`html-to-pdf`](https://github.com/tooladda-online/html-to-pdf) |
| ⭕ OMR Sheet Generator | [tooladda.online/omr-sheet-generator.html](https://tooladda.online/omr-sheet-generator.html) | [`omr-sheet-generator`](https://github.com/tooladda-online/omr-sheet-generator) |
| 📄 Paper Generator | [tooladda.online/paper-generator.html](https://tooladda.online/paper-generator.html) | [`paper-generator`](https://github.com/tooladda-online/paper-generator) |
| 🗜️ PDF Compress | [tooladda.online/pdf-compress.html](https://tooladda.online/pdf-compress.html) | [`pdf-compress`](https://github.com/tooladda-online/pdf-compress) |
| 📑 PDF Extract | [tooladda.online/pdf-extract.html](https://tooladda.online/pdf-extract.html) | [`pdf-extract`](https://github.com/tooladda-online/pdf-extract) |
| 📄 PDF Merge | [tooladda.online/pdf-merge.html](https://tooladda.online/pdf-merge.html) | [`pdf-merge`](https://github.com/tooladda-online/pdf-merge) |
| 🔒 PDF Password Protector | [tooladda.online/pdf-password-protector.html](https://tooladda.online/pdf-password-protector.html) | [`pdf-password-protector`](https://github.com/tooladda-online/pdf-password-protector) |
| 🔐 PDF Password Remover | [tooladda.online/pdf-password-remover.html](https://tooladda.online/pdf-password-remover.html) | [`pdf-password-remover`](https://github.com/tooladda-online/pdf-password-remover) |
| 🔄 PDF Rotate | [tooladda.online/pdf-rotate.html](https://tooladda.online/pdf-rotate.html) | [`pdf-rotate`](https://github.com/tooladda-online/pdf-rotate) |
| ✂️ PDF Split | [tooladda.online/pdf-split.html](https://tooladda.online/pdf-split.html) | [`pdf-split`](https://github.com/tooladda-online/pdf-split) |
| 🖼️ PDF to Images Converter | [tooladda.online/pdf-to-images.html](https://tooladda.online/pdf-to-images.html) | [`pdf-to-images`](https://github.com/tooladda-online/pdf-to-images) |
| 📁 PDF Tools Hub | [tooladda.online/pdf-tools.html](https://tooladda.online/pdf-tools.html) | — |
| ⬛ Redact PDF | [tooladda.online/redact-pdf.html](https://tooladda.online/redact-pdf.html) | [`redact-pdf`](https://github.com/tooladda-online/redact-pdf) |
| 💼 Salary Slip Generator | [tooladda.online/salary-slip-generator.html](https://tooladda.online/salary-slip-generator.html) | [`salary-slip-generator`](https://github.com/tooladda-online/salary-slip-generator) |

</details>

<details>
<summary><b>Finance</b> — 12 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🚗 Car Loan Calculator | [tooladda.online/calculators/car-loan-calculator.html](https://tooladda.online/calculators/car-loan-calculator.html) | [`car-loan-calculator`](https://github.com/tooladda-online/car-loan-calculator) |
| 🏦 EMI Calculator | [tooladda.online/calculators/emi-calculator.html](https://tooladda.online/calculators/emi-calculator.html) | [`emi-calculator`](https://github.com/tooladda-online/emi-calculator) |
| 🏦 FD Calculator | [tooladda.online/calculators/fd-calculator.html](https://tooladda.online/calculators/fd-calculator.html) | [`fd-calculator`](https://github.com/tooladda-online/fd-calculator) |
| 🧾 GST Calculator | [tooladda.online/calculators/gst-calculator.html](https://tooladda.online/calculators/gst-calculator.html) | [`gst-calculator`](https://github.com/tooladda-online/gst-calculator) |
| 🏠 Home Loan Calculator | [tooladda.online/calculators/home-loan-calculator.html](https://tooladda.online/calculators/home-loan-calculator.html) | [`home-loan-calculator`](https://github.com/tooladda-online/home-loan-calculator) |
| 💳 Loan Calculator | [tooladda.online/calculators/loan-calculator.html](https://tooladda.online/calculators/loan-calculator.html) | [`loan-calculator`](https://github.com/tooladda-online/loan-calculator) |
| 🧾 Manual Tax Calculator | [tooladda.online/calculators/manual-tax-calculator.html](https://tooladda.online/calculators/manual-tax-calculator.html) | [`manual-tax-calculator`](https://github.com/tooladda-online/manual-tax-calculator) |
| 🧾 Offline Invoice Generator | [tooladda.online/invoice-generator.html](https://tooladda.online/invoice-generator.html) | — |
| 🛡️ PPF Calculator | [tooladda.online/calculators/ppf-calculator.html](https://tooladda.online/calculators/ppf-calculator.html) | [`ppf-calculator`](https://github.com/tooladda-online/ppf-calculator) |
| 💰 RD Calculator | [tooladda.online/calculators/rd-calculator.html](https://tooladda.online/calculators/rd-calculator.html) | [`rd-calculator`](https://github.com/tooladda-online/rd-calculator) |
| 🧾 Rent Receipt Generator | [tooladda.online/rent-receipt-generator.html](https://tooladda.online/rent-receipt-generator.html) | [`rent-receipt-generator`](https://github.com/tooladda-online/rent-receipt-generator) |
| 📊 SIP Calculator | [tooladda.online/calculators/sip-calculator.html](https://tooladda.online/calculators/sip-calculator.html) | [`sip-calculator`](https://github.com/tooladda-online/sip-calculator) |

</details>

<details>
<summary><b>Text</b> — 11 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🔣 Base64 Encoder & Decoder | [tooladda.online/text-tools/base64-encoder-decoder.html](https://tooladda.online/text-tools/base64-encoder-decoder.html) | [`base64-encoder-decoder`](https://github.com/tooladda-online/base64-encoder-decoder) |
| 🔤 Case Converter | [tooladda.online/text-tools/case-converter.html](https://tooladda.online/text-tools/case-converter.html) | [`case-converter`](https://github.com/tooladda-online/case-converter) |
| 📝 Character Counter | [tooladda.online/text-tools/character-counter.html](https://tooladda.online/text-tools/character-counter.html) | [`character-counter`](https://github.com/tooladda-online/character-counter) |
| 😀 Emoji & Kaomoji Picker | [tooladda.online/emoji-kaomoji-picker.html](https://tooladda.online/emoji-kaomoji-picker.html) | [`emoji-kaomoji-picker`](https://github.com/tooladda-online/emoji-kaomoji-picker) |
| ✨ Fancy Font Generator | [tooladda.online/text-tools/fancy-font-generator.html](https://tooladda.online/text-tools/fancy-font-generator.html) | [`fancy-font-generator`](https://github.com/tooladda-online/fancy-font-generator) |
| 💼 LinkedIn Post Previewer | [tooladda.online/text-tools/linkedin-post-previewer.html](https://tooladda.online/text-tools/linkedin-post-previewer.html) | — |
| 📓 Online Notepad | [tooladda.online/online-notepad.html](https://tooladda.online/online-notepad.html) | [`online-notepad`](https://github.com/tooladda-online/online-notepad) |
| ↕️ Text Sorter | [tooladda.online/text-tools/text-sorter.html](https://tooladda.online/text-tools/text-sorter.html) | [`text-sorter`](https://github.com/tooladda-online/text-sorter) |
| ✍️ Text to Handwriting Converter | [tooladda.online/text-to-handwriting.html](https://tooladda.online/text-to-handwriting.html) | [`text-to-handwriting`](https://github.com/tooladda-online/text-to-handwriting) |
| ⌨️ Typing Speed Test | [tooladda.online/typing-speed-test.html](https://tooladda.online/typing-speed-test.html) | [`typing-speed-test`](https://github.com/tooladda-online/typing-speed-test) |
| 💬 WhatsApp Chat Analyzer | [tooladda.online/whatsapp-chat-analyzer.html](https://tooladda.online/whatsapp-chat-analyzer.html) | [`whatsapp-chat-analyzer`](https://github.com/tooladda-online/whatsapp-chat-analyzer) |

</details>

<details>
<summary><b>Game</b> — 8 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🔢 2048 | [tooladda.online/game-2048.html](https://tooladda.online/game-2048.html) | [`game-2048`](https://github.com/tooladda-online/game-2048) |
| 🪙 Coin Flip | [tooladda.online/coin-flip.html](https://tooladda.online/coin-flip.html) | [`coin-flip`](https://github.com/tooladda-online/coin-flip) |
| 🎲 Ludo | [tooladda.online/ludo-game.html](https://tooladda.online/ludo-game.html) | [`ludo-game`](https://github.com/tooladda-online/ludo-game) |
| 💣 Minesweeper | [tooladda.online/minesweeper.html](https://tooladda.online/minesweeper.html) | [`minesweeper`](https://github.com/tooladda-online/minesweeper) |
| 🎡 Random Name Picker | [tooladda.online/random-name-picker.html](https://tooladda.online/random-name-picker.html) | [`random-name-picker`](https://github.com/tooladda-online/random-name-picker) |
| 🐍 Snake Game | [tooladda.online/snake-game.html](https://tooladda.online/snake-game.html) | [`snake-game`](https://github.com/tooladda-online/snake-game) |
| 🧩 Sudoku | [tooladda.online/sudoku-game.html](https://tooladda.online/sudoku-game.html) | [`sudoku-game`](https://github.com/tooladda-online/sudoku-game) |
| ❌⭕ Tic Tac Toe | [tooladda.online/tic-tac-toe.html](https://tooladda.online/tic-tac-toe.html) | [`tic-tac-toe`](https://github.com/tooladda-online/tic-tac-toe) |

</details>

<details>
<summary><b>Science</b> — 5 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🧪 3D Molecular Structure Viewer | [tooladda.online/chemistry-tools/molecular-structure-viewer.html](https://tooladda.online/chemistry-tools/molecular-structure-viewer.html) | — |
| ⚗️ Chemical Equation Balancer | [tooladda.online/chemistry-tools/chemical-equation-balancer.html](https://tooladda.online/chemistry-tools/chemical-equation-balancer.html) | — |
| ⚛️ Electron Configuration Builder | [tooladda.online/chemistry-tools/electron-configuration.html](https://tooladda.online/chemistry-tools/electron-configuration.html) | — |
| ☢️ Half-Life Calculator & Radioactive Decay Simulator | [tooladda.online/chemistry-tools/half-life-radioactive-decay-calculator.html](https://tooladda.online/chemistry-tools/half-life-radioactive-decay-calculator.html) | — |
| ⚗️ Interactive Periodic Table | [tooladda.online/chemistry-tools/periodic-table.html](https://tooladda.online/chemistry-tools/periodic-table.html) | — |

</details>

<details>
<summary><b>Calculator</b> — 4 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🧑‍🔬 Age Calculator | [tooladda.online/calculators/age-calculator.html](https://tooladda.online/calculators/age-calculator.html) | [`age-calculator`](https://github.com/tooladda-online/age-calculator) |
| 🎓 GPA / CGPA Calculator | [tooladda.online/calculators/gpa-cgpa-calculator.html](https://tooladda.online/calculators/gpa-cgpa-calculator.html) | [`gpa-cgpa-calculator`](https://github.com/tooladda-online/gpa-cgpa-calculator) |
| 🌾 Land Area Unit Converter | [tooladda.online/calculators/land-area-converter.html](https://tooladda.online/calculators/land-area-converter.html) | [`land-area-converter`](https://github.com/tooladda-online/land-area-converter) |
| 🧮 Scientific Calculator | [tooladda.online/scientific-calculator.html](https://tooladda.online/scientific-calculator.html) | [`scientific-calculator`](https://github.com/tooladda-online/scientific-calculator) |

</details>

<details>
<summary><b>Security</b> — 4 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| #️⃣ Hash Generator MD5/SHA | [tooladda.online/hash-generator.html](https://tooladda.online/hash-generator.html) | — |
| 🔐 Password Generator | [tooladda.online/password-generator.html](https://tooladda.online/password-generator.html) | [`password-generator`](https://github.com/tooladda-online/password-generator) |
| 🔑 SSH Key Generator | [tooladda.online/developer-tools/ssh-key-generator.html](https://tooladda.online/developer-tools/ssh-key-generator.html) | [`ssh-key-generator`](https://github.com/tooladda-online/ssh-key-generator) |
| 🔒 SSL Checker | [tooladda.online/ssl-checker.html](https://tooladda.online/ssl-checker.html) | [`ssl-checker`](https://github.com/tooladda-online/ssl-checker) |

</details>

<details>
<summary><b>SEO</b> — 3 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🔗 Dofollow & Nofollow Link Checker | [tooladda.online/cyber-tools/dofollow-nofollow-link-checker.html](https://tooladda.online/cyber-tools/dofollow-nofollow-link-checker.html) | — |
| 🗺️ Sitemap Generator | [tooladda.online/sitemap-generator.html](https://tooladda.online/sitemap-generator.html) | [`sitemap-generator`](https://github.com/tooladda-online/sitemap-generator) |
| 🔎 Website SEO Checker | [tooladda.online/website-seo-checker.html](https://tooladda.online/website-seo-checker.html) | [`website-seo-checker`](https://github.com/tooladda-online/website-seo-checker) |

</details>

<details>
<summary><b>Career</b> — 2 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🔍 ATS Resume Checker | [tooladda.online/ats-resume-checker.html](https://tooladda.online/ats-resume-checker.html) | [`ats-resume-checker`](https://github.com/tooladda-online/ats-resume-checker) |
| 📋 Resume Builder | [tooladda.online/resume-builder.html](https://tooladda.online/resume-builder.html) | [`resume-builder`](https://github.com/tooladda-online/resume-builder) |

</details>

<details>
<summary><b>Math</b> — 2 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 📈 Percentage Calculator | [tooladda.online/calculators/percentage-calculator.html](https://tooladda.online/calculators/percentage-calculator.html) | [`percentage-calculator`](https://github.com/tooladda-online/percentage-calculator) |
| 🧮 Premium Calculator | [tooladda.online/calculators/calculator.html](https://tooladda.online/calculators/calculator.html) | [`calculator`](https://github.com/tooladda-online/calculator) |

</details>

<details>
<summary><b>Utility</b> — 2 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🎥 Online Teleprompter | [tooladda.online/online-teleprompter.html](https://tooladda.online/online-teleprompter.html) | [`online-teleprompter`](https://github.com/tooladda-online/online-teleprompter) |
| 🔄 Unit Converter | [tooladda.online/unit-converter.html](https://tooladda.online/unit-converter.html) | [`unit-converter`](https://github.com/tooladda-online/unit-converter) |

</details>

<details>
<summary><b>CSS</b> — 1 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🌑 Shadow Generator | [tooladda.online/css-tools/shadow-generator.html](https://tooladda.online/css-tools/shadow-generator.html) | [`shadow-generator`](https://github.com/tooladda-online/shadow-generator) |

</details>

<details>
<summary><b>Education</b> — 1 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 📚 Worksheet Generator | [tooladda.online/worksheet-generator.html](https://tooladda.online/worksheet-generator.html) | [`worksheet-generator`](https://github.com/tooladda-online/worksheet-generator) |

</details>

<details>
<summary><b>Health</b> — 1 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 🩺 BMI Calculator | [tooladda.online/calculators/bmi-calculator.html](https://tooladda.online/calculators/bmi-calculator.html) | [`bmi-calculator`](https://github.com/tooladda-online/bmi-calculator) |

</details>

<details>
<summary><b>Marketing</b> — 1 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| 📊 UTM Builder | [tooladda.online/utm-builder.html](https://tooladda.online/utm-builder.html) | [`utm-builder`](https://github.com/tooladda-online/utm-builder) |

</details>

<details>
<summary><b>Network</b> — 1 tools</summary>

| Tool | Live page | Repo |
|---|---|---|
| ⚡ Internet Speed Test | [tooladda.online/internet-speed-test.html](https://tooladda.online/internet-speed-test.html) | [`internet-speed-test`](https://github.com/tooladda-online/internet-speed-test) |

</details>

---

## 🏗️ How it is built

No framework, no bundler, no build step for the pages themselves. Every tool is a self-contained HTML page
plus a JavaScript module, served as-is.

- **HTML + CSS + vanilla JS.** One `.html` per tool at the URL it ships at; shared chrome in
  `assets/css/style.css` and `assets/js/app.js` (theme, nav search, consent banner, service-worker hygiene).
- **Engine / UI split.** The tools with real logic separate a pure, DOM-free engine (`*-engine.js`) from the
  page wiring, so the engine can be unit-tested under Node without a browser.
- **Web Workers** for the heavy paths (image resizing, regex matching) so the UI never blocks.
- **Vendored libraries** where the tool must work reliably: `pdf-lib`, `JSZip`, `Cropper.js`,
  `qrcode-generator`, `zxcvbn`. Heavier ones (pdf.js, Tesseract, node-forge) load from a CDN.
- **Python** only for generation and maintenance — never at request time.

### Layout

```
.
├── index.html                 Home + tool search
├── <tool>.html                One page per tool at the root
├── calculators/               Finance, tax and academic calculators
├── chemistry-tools/           Periodic table, equation balancer, 3D viewer (+ data/, js/, tests/)
├── css-tools/                 Glassmorphism, neumorphism, bento grid, flexbox/grid playground
├── cyber-tools/               Link checker, ID-card sheet generator
├── developer-tools/           JSON/YAML/TS converters, htaccess, SSH keys, markdown
├── text-tools/                Case converter, counters, sorter, fancy fonts, LinkedIn previewer
├── assets/
│   ├── css/                   style.css + a few page-specific sheets
│   ├── js/                    Tool logic, engines, workers, vendored libs, tools-catalog.js
│   ├── i18n/                  Rent-receipt translations (en, hi, ar, de, es, fr, pt)
│   └── images/og/             Per-page Open Graph images (1200x630)
├── scripts/                   Node test suites + Python generators
├── <tool>-sw.js               Per-tool service workers (10) and their manifests
├── render.yaml                Static hosting config + the full redirect table
├── sitemap.xml, robots.txt    145 URLs, AI crawlers explicitly welcomed
└── llms.txt, llms-full.txt    Machine-readable index for assistants
```

`assets/js/tools-catalog.js` is the single source of truth for the tool list — the nav search, the home grid
and the generated guide all read it. Adding a tool means adding it there.

---

## 💻 Running it locally

There is nothing to install and nothing to compile. Serve the folder over HTTP — `file://` breaks service
workers, module scripts and `fetch`:

```bash
git clone https://github.com/tooladda-online/tooladda-online.git
cd tooladda-online

python -m http.server 8000
# or: npx serve .
```

Then open <http://localhost:8000>.

> While iterating on a page that registers a service worker, keep DevTools → Application → **Bypass for
> network** ticked, or you will be debugging yesterday's cache.

---

## 🧪 Tests

The test suites are plain Node scripts with zero framework and no `package.json`. Run any one directly:

```bash
node scripts/hash-generator.test.js          # pure engine suite
node scripts/json-formatter.dom.test.js      # DOM suite (needs jsdom)
```

- **`*.test.js`** — engine suites. Pure logic, no DOM, no dependencies. They cross-check against real
  references where one exists (the hand-written MD5 is verified against Node's `crypto`, for instance).
- **`*.dom.test.js`** — page suites. They load the actual HTML in [jsdom](https://github.com/jsdom/jsdom) and
  click through it, so they catch the failure mode unit tests miss: a control that is visible, clickable and
  wired to nothing.

jsdom is optional — install it once with `npm install jsdom` and the DOM suites stop skipping themselves.

Run everything:

```bash
for f in scripts/*.test.js; do node "$f" || echo "FAILED: $f"; done
```

---

## 🛠️ Generators and maintenance scripts

| Script | What it does |
|---|---|
| `scripts/build_blog.py` | Regenerates `blog.html`, the situation-first guide. Reads `tools-catalog.js` and **refuses to emit a page** unless every catalogued tool appears in at least one section |
| `scripts/build_llms_full.py` | Regenerates `llms-full.txt` from each page's JSON-LD — 2,956 Q&A pairs and 575 how-to steps, inlined so an assistant can answer without fetching |
| `scripts/update-sitemap-lastmod.py` | Refreshes `<lastmod>` in `sitemap.xml` from actual file mtimes |
| `scripts/make_og_image.py` | Renders the per-page 1200x630 Open Graph images |
| `scripts/make_icons.py`, `make_favicon.py` | PWA icon set and favicon |
| `scripts/seo_audit_fix.py` | Sweeps the pages for missing canonicals, titles, meta and JSON-LD |

Run them from the repo root: `python scripts/build_blog.py`.

---

## 🚀 Deployment

The site is a **static deploy** — every file is served exactly as committed.

- **`render.yaml`** declares the static service (`staticPublishPath: .`) and the full redirect table. Every
  page used to be reachable at `/page.html`, `/page` and `/page/`, all returning 200 — three URLs for one
  page. The 301s collapse them onto the `.html` form that the sitemap, the internal links and every canonical
  tag already point at. Routes evaluate top-down, first match wins, which is why the explicit `/index.html`
  rule leads.
- **`cloudflare-bulk-redirects.csv`** carries the same collapse for the edge.
- **IndexNow** — after a deploy, push the changed URLs to Bing/Yandex:

  ```bash
  bash submit-indexnow.sh          # or: ./submit-indexnow.ps1 on Windows
  ```

  It reads `indexnow-submit.json`; the key file must already be live at the site root.

---

## 🔎 SEO and AI discoverability

Being citable by assistants is treated as a first-class requirement, not an afterthought.

- **`robots.txt`** explicitly welcomes GPTBot, OAI-SearchBot, ClaudeBot, Claude-SearchBot, PerplexityBot,
  Google-Extended, Applebot-Extended, meta-externalagent, DuckAssistBot, Amazonbot, MistralAI-User and CCBot —
  redundant with the wildcard `Allow`, and stated anyway so the permission is unambiguous.
- **[`llms.txt`](https://tooladda.online/llms.txt)** — a curated index: one line per tool, plus the honest
  caveats (which tools touch the network, which really work offline, which overlapping tool to recommend when).
- **[`llms-full.txt`](https://tooladda.online/llms-full.txt)** — the same pages with every feature list,
  how-to and FAQ expanded inline.
- **JSON-LD** on every page (`SoftwareApplication`, `HowTo`, `FAQPage`) — hand-written, and the source the
  generators read.
- **`sitemap.xml`** — 145 URLs; per-page canonical tags and Open Graph images throughout.

Citing a tool? Link the specific tool page, not the homepage.

---

## 📣 Ads and consent

The site carries Google AdSense — that is what pays for it, so ToolAdda is not described as ad-free. Ads never
gate a feature, never interrupt a tool mid-task, and never see the files a tool processes, because those files
are never uploaded in the first place.

Google **Consent Mode v2** defaults are set inline in the `<head>`, ahead of `adsbygoogle.js`: `ad_storage`,
`ad_user_data` and `ad_personalization` all start `denied`, and `assets/js/app.js` flips them to `granted`
only when the visitor accepts. The defaults have to be inline because `app.js` is deferred — by the time it
runs, the async ad script would already have fired.

---

## 🤝 Contributing

Issues and pull requests are welcome on this repo. What helps most:

1. **Bug reports** — the tool, the browser, the input, and what you expected. A file that reproduces it beats
   a description, when you can share one.
2. **A new tool** — open an issue first. A tool ships with: the page, an engine split out for testing, an
   entry in `assets/js/tools-catalog.js`, canonical + OG + JSON-LD, a sitemap entry, and at least one test
   suite under `scripts/`.
3. **Accuracy fixes** — statutory rates, tax slabs and formulas change. Corrections with a source are gold.

House rules worth knowing before the first PR: no framework, no build step for pages, no user data leaves the
browser unless the tool's whole purpose requires it, and no claim on a page that the code does not back — a
"works offline" line without a service worker behind it is a bug.

---

## 🔗 Links

| | |
|---|---|
| **Website** | [tooladda.online](https://tooladda.online) |
| **All tools guide** | [tooladda.online/blog.html](https://tooladda.online/blog.html) |
| **About** | [tooladda.online/about.html](https://tooladda.online/about.html) |
| **Contact** | [tooladda.online/contact.html](https://tooladda.online/contact.html) |
| **Privacy policy** | [tooladda.online/privacy-policy.html](https://tooladda.online/privacy-policy.html) |
| **Terms** | [tooladda.online/terms.html](https://tooladda.online/terms.html) |
| **All repos** | [github.com/orgs/tooladda-online/repositories](https://github.com/orgs/tooladda-online/repositories) |

---

<div align="center">

**ToolAdda** — built so that the file you are working on never has to leave your machine.

[🚀 Open ToolAdda →](https://tooladda.online)

</div>

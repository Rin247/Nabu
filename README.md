# Nabu — Unified Reader for Comics, Ebooks, PDFs & Fanfiction

Nabu is an all-in-one, privacy-focused Android reader for comics, manga, EPUB ebooks, PDFs, web novels, and fanfiction. Built with Kotlin, Jetpack Compose, Material 3, and a high-performance C++/native document rendering core, Nabu delivers a seamless, ad-free reading experience for every text and visual format.

---

## 📚 Key Features & Subsystem Breakdown

### 🎨 Comic & Manga Engine (`reader-comic`)
- **Current**: CBZ, CBR, CBT, CB7, ZIP, and RAR archive extraction with smooth pinch-to-zoom, dual-page layout, right-to-left (manga) reading mode, and webtoon continuous vertical scroll.
- **Planned / Roadmap**: Automatic page splitting, background color blending, page upscaling (Super Resolution), and automatic speech bubble extraction for text zoom.

### 📖 Ebook & EPUB Reader (`reader-epub`)
- **Current**: EPUB 2/3 and MOBI document parsing with custom typography, font sizing, line spacing, margins, dark mode, and table of contents navigation.
- **Planned / Roadmap**: Hyphenation dictionary support, inline dictionary lookup, TTS (Text-to-Speech) audiobook synthesis, and OPDS catalog integration.

### 📄 PDF Document Viewer (`reader-pdf`)
- **Current**: High-speed PDF page rendering, page thumbnails, text selection, and continuous scrolling.
- **Planned / Roadmap**: Vector PDF text search, PDF annotations & highlighting, night mode invert, and text extraction reader mode.

### 🌐 Fanfiction & Web Novel Engine (`reader-web`)
- **Current**: Web novel reader with offline chapter caching, metadata parsing, and reading position sync.
- **Planned / Roadmap**: Automated AO3 (Archive of Our Own), RoyalRoad, and FanFiction.net chapter tracking, novel download queue, and update notifications.

### 🗃️ Library & Catalog Manager (`library`)
- **Current**: Tag-based collection management, read status tracking, reading progress stats, and local file scanner.
- **Planned / Roadmap**: Automated cover art extraction, cloud backup sync (WebDAV / Nextcloud / Google Drive), reading statistics graphs, and extension plugin repository.

---

## 🏗️ Architecture & Technology Stack

- **Platform**: Android 13+ (minSdk 33, targetSdk 37).
- **UI & Layout**: Kotlin, Jetpack Compose, Material 3 dynamic color theme.
- **Document Core**: Native archive parsers (libarchive, unrar, MuPDF / PDFium integration).
- **Architecture**: Modular Clean Architecture (`:core:common`, `:source-api`, `:domain`, `:data`, `:presentation-core`).
- **Licensing**: AGPL-3.0.

---

## 🛠️ Building & Running

### Prerequisites
- **Android Studio** (2026.2.2+) or Gradle CLI
- **JDK 25**

### Build Commands

```bash
# Build Debug APK
./gradlew assembleDebug

# Install on connected device/emulator
./gradlew installDebug
```

---

## 📜 License

Nabu is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.

# FinVAT

## Overview

FinVAT is a robust data watermarking and leak detection platform designed for financial data sharing and anti-leak tracing. It empowers organizations to embed invisible, normalization-proof watermarks into sensitive data, enabling instant detection and attribution of leaks—no matter how the data is copied, edited, or normalized.

---

## Features

- **Invisible Watermarks:** Embed unique, hidden codes in every data object.
- **Normalization-Proof Techniques:** Survive data cleaning, reformatting, and partial edits.
- **Steganography in Strings:** Use zero-width characters, strategic hyphens, and underscores (e.g., `TCS_Ltd_`, `HDFC-Bank`).
- **Subtle Numeric & Date Tweaks:** Add tiny changes at the 5th decimal place or manipulate date formats (e.g., `1234.56001`, `2025/07/06`).
- **Cryptographic Fingerprinting:** Generate a unique `watermarkSeed` using SHA-256 and embed a `fingerprintCode` for tamper-evident tracing.
- **Leak Detection Dashboard:** Upload leaked data and instantly identify the source with colorful, detailed analytics.
- **Unbiased Leak Analysis:** Leaked data contains no company-identifying information, ensuring fair detection.

---

## How It Works

FinVAT uses a blend of advanced techniques to watermark data:

- 🕵️‍♂️ **Invisible Metadata:**  
  Hidden fields like `__wm` are embedded in data objects, acting as digital fingerprints.

- 🪄 **String Steganography:**  
  Information is hidden using zero-width characters, hyphens, and underscores in text fields.

- 🧮 **Subtle Numeric & Date Tweaks:**  
  Floats are tweaked at the 5th decimal place, and date formats are subtly changed.

- 🛡️ **Normalization-Proof Watermarks:**  
  Watermarks survive data cleaning, reformatting, and even partial edits.

- 🔑 **Cryptographic Fingerprinting:**  
  Each record gets a unique SHA-256 `watermarkSeed` and a binary `fingerprintCode`.

> **We hide our marks in plain sight—using a blend of invisible metadata, steganography, cryptographic fingerprints, and subtle data tweaks. Even if the data is copied, normalized, or leaked, FinVAT can trace it back—no matter where it goes.**

---

## Getting Started

1. **Clone the repository**
   ```sh
   git clone https://github.com/adeebkhans/finvat.git
   cd finvat
   ```

2. **Install dependencies**
   ```sh
   cd Backend
   npm install
   cd ../Frontend
   npm install
   ```

3. **Configure environment variables**  
   Copy `.env.example` to `.env` in both `Backend` and `Frontend` folders and update as needed.

4. **Run the backend**
   ```sh
   cd Backend
   npm start
   ```

5. **Run the frontend**
   ```sh
   cd ../Frontend
   npm run dev
   ```

6. **Access the dashboard**  
   Open [http://localhost:5173](http://localhost:5173) in your browser.

---

## License

MIT License

---

*FinVAT — Watermarking financial data, tracing leaks, and protecting

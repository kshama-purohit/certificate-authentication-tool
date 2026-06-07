# Certificate Authentication Tool

A browser-based steganography tool that hides and extracts text within images for certificate authentication — combining LSB (Least Significant Bit) steganography with a modified Caesar cipher.

> Developed as part of a research project at MPSTME, Mumbai by Kshama Purohit, Dakshinya Munjal, Vasu Patel, and Krish Maniar.

---

## How it works

1. A validation message is encrypted using a modified Caesar cipher
2. The encrypted text is converted to binary and embedded into an image by replacing the least significant bit of each pixel's red channel
3. The change is invisible to the human eye — the stego image looks identical to the original
4. To verify a certificate, the signed image is uploaded and the hidden message is extracted and compared against known parameters

---

## Features

- 🖼️ **Hide text** — embed a secret validation key into any certificate image
- 🔍 **Extract text** — retrieve the hidden key from a signed certificate
- 🔒 **Caesar cipher** — configurable shift value for added encryption
- 💾 **Download** — save the encoded image as a PNG
- 🌙 **Dark mode** — automatically adapts to system preference
- 🚫 **No server required** — runs entirely in the browser

---

## Performance

Tested across multiple images and messages using PSNR, SSIM, and embedding rate:

| Image | PSNR | SSIM | Embedding Rate |
|-------|------|------|----------------|
| Certificate | 73.40 | 0.99996 | 0.01 |
| Cat | 65.76 | 0.99979 | 0.05 |
| Human Face | 77.51 | 0.99999 | 0.08 |
| Flower | 64.09 | 0.99995 | 0.06 |

High PSNR and SSIM values close to 1 confirm that the embedded images are visually indistinguishable from the originals.

---

## Usage

1. Open `index.html` in any modern browser
2. Select a certificate image file
3. **To hide text:** enter your validation key, set a shift value, and click *Hide text* — then download the encoded image
4. **To extract text:** upload the encoded certificate, leave the text field blank, and click *Extract text*

---

## Research

The full research paper (`Certificate_Authentication_Tool.pdf`) is included in this repository. It covers:

- A review of 8 existing LSB steganography papers
- The proposed algorithm combining LSB + Caesar cipher
- Performance evaluation (PSNR, SSIM, embedding rate)
- Future scope including object-detection-based hiding and ML-enhanced embedding

---

## Tech stack

- Vanilla HTML, CSS, JavaScript
- Canvas API for pixel-level image manipulation
- No dependencies or build tools required

---

## Live demo

Hosted via GitHub Pages: `https://kshama-purohit.github.io/your-repo-name`

---

## Authors

- Kshama Purohit
- Dakshinya Munjal
- Vasu Patel
- Krish Maniar

B.Tech CSEDS 311, MPSTME, Mumbai

---

## License

This project is for educational and research purposes.

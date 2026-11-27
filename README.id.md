<div align="center">
  <img src="docs/assets/app_icon.png" width="100" alt="Logo Kazeru" />
  <h1>Kazeru</h1>
  <p><sub>dulu bernama KZRS</sub></p>

  <p>
    <a href="https://github.com/kouzen-neo/kzrs/releases/latest"><img src="https://img.shields.io/github/v/release/kouzen-neo/kzrs?style=for-the-badge&color=f0a43a" alt="Rilis terbaru"></a>
    <img src="https://img.shields.io/badge/Windows-10%2F11-0078D4.svg?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
    <img src="https://img.shields.io/badge/macOS-Apple%20Silicon-000000.svg?style=for-the-badge&logo=apple&logoColor=white" alt="macOS">
    <img src="https://img.shields.io/badge/Linux-x86__64-FCC624.svg?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
    <img src="https://img.shields.io/badge/Rust-native-b7410e.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
  </p>

  <p>
    <a href="README.md"><img src="https://img.shields.io/badge/EN-6e7681.svg?style=for-the-badge" alt="English"></a>
    <a href="README.id.md"><img src="https://img.shields.io/badge/ID-0078D4.svg?style=for-the-badge" alt="Bahasa Indonesia"></a>
  </p>
</div>

> **Repositori legacy.** KZRS sekarang bernama **Kazeru**. Rilis baru, unduhan dan catatan perubahan akan pindah ke [kouzen-neo/kazeru](https://github.com/kouzen-neo/kazeru) (belum dipublikasikan). Repositori ini tetap online untuk rilis yang sudah ada, dan app yang terpasang tetap update dari sini sampai pindahan selesai.

Kazeru adalah penerjemah manga dan komik untuk desktop, dibuat dengan Rust. Kazeru menemukan balon
dialog dan teks bebas di halaman dengan AI di perangkat, menerjemahkannya dengan penyedia LLM
pilihanmu (atau yang lokal seperti Ollama atau LM Studio), menghapus tulisan aslinya, lalu
menata terjemahannya kembali di halaman. Ada editor halaman, pembaca, dan ekspor CBZ/PDF.

Repositori ini berisi **rilis** dan catatan perubahan; kode sumbernya privat.

---

## Unduh

Ambil versi terbaru di **[Releases](https://github.com/kouzen-neo/kzrs/releases/latest)**.

| Sistem | File | Cara pasang |
|---|---|---|
| Windows 10/11 (64-bit) | `KZRS-Setup-<versi>-x64.exe` | Jalankan dan ikuti langkahnya (tidak perlu admin). `KZRS-<versi>-x64.msi` adalah aplikasi yang sama untuk IT / PC kantor. |
| Linux x86_64 (Ubuntu 24.04, Debian 13, Fedora 39, Mint 22 atau lebih baru) | `KZRS-<versi>-x86_64.AppImage` | Jadikan executable (`chmod +x`, atau Properties → Allow executing) lalu buka. Ada juga `.tar.gz` dengan `install.sh` untuk menu aplikasi. |
| macOS 13.4 atau lebih baru (Apple Silicon: M1 sampai M5) | `KZRS-<versi>-macos-arm64.dmg` | Buka `.dmg` lalu seret **Kazeru** ke **Applications**. Mac Intel belum didukung. |

Aplikasinya belum ditandatangani (code signing), jadi sistem akan bertanya sekali:

- **Windows**: "Windows protected your PC" → **More info** → **Run anyway**.
- **macOS**: buka Kazeru sekali, lalu **System Settings** → **Privacy & Security** → **Open Anyway**.
- **Linux AppImage**: kalau tidak mau jalan, pasang `libfuse2`, atau jalankan dengan `--appimage-extract-and-run`.

Model OCR dan LaMa (opsional) diunduh dari dalam aplikasi saat pertama kali dibutuhkan
(Settings > Models).

---

## Fitur utama

- **Banyak format masukan**: gambar, folder, ZIP / CBZ, EPUB dan PDF.
- **Vision lokal**: deteksi balon, OCR, inpainting dan penataan teks berjalan di komputermu; yang
  dikirim ke penyedia terjemahan hanya potongan balon dan baris teksnya (satu gambar berisi potongan itu
  per permintaan), tidak pernah halaman utuh atau file-mu.
- **LLM apa saja**: Google Gemini, Anthropic Claude, OpenAI, OpenRouter, Zen, OpenCode Go, atau
  endpoint yang kompatibel dengan OpenAI (Ollama, LM Studio, vLLM...).
- **Hasil rapi**: inpainting LaMa / Telea, pemenggalan baris sesuai balon, teks Jepang vertikal,
  font komik bawaan dan preset gaya.
- **Editor halaman**: geser, ubah ukuran dan gaya kotak, balon dialog yang digambar, tebal /
  miring / warna / font / ukuran di dalam satu baris, Translate area, kuas dengan penghapusnya
  sendiri, restore / hapus, gambar dan layer, edit massal, undo per halaman.
- **Pembaca dan ekspor**: mode halaman atau webtoon, membuka PDF / CBZ / ZIP / EPUB dari file
  manager, ekspor ke CBZ atau PDF.
- **Agen AI (Pro)**: server MCP dan CLI, supaya Claude Code, OpenCode atau Codex bisa
  memeriksa dan memperbaiki halaman untukmu.

---

## Gratis dan Pro

Kazeru gratis dipakai. Paket dan beli kode Pro dengan QRIS di website: [kazeru.kouzen.my.id/id/supporter](https://kazeru.kouzen.my.id/id/supporter/).

---

## Masukan

Bug dan ide: [Issues](https://github.com/kouzen-neo/kzrs/issues), atau [Discord](https://discord.gg/CdZUeMQQK).

Perubahan tiap versi: [CHANGELOG.md](CHANGELOG.md).

---

## Lisensi

Freeware proprietary. Hak cipta dilindungi.

<div align="center">
  <img src="docs/assets/app_icon.png" width="100" alt="Logo KZRS" />
  <h1>KZRS</h1>

  <p>
    <a href="https://github.com/kouzen-neo/kzrs/releases/latest"><img src="https://img.shields.io/github/v/release/kouzen-neo/kzrs?style=for-the-badge&color=f0a43a" alt="Rilis terbaru"></a>
    <img src="https://img.shields.io/badge/Windows-10%2F11-0078D4.svg?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
    <img src="https://img.shields.io/badge/macOS-segera%20hadir-6e7681.svg?style=for-the-badge&logo=apple&logoColor=white" alt="macOS segera hadir">
    <img src="https://img.shields.io/badge/Linux-x86__64-FCC624.svg?style=for-the-badge&logo=linux&logoColor=black" alt="Linux">
    <img src="https://img.shields.io/badge/Rust-native-b7410e.svg?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
  </p>

  <p>
    <a href="README.md"><img src="https://img.shields.io/badge/EN-6e7681.svg?style=for-the-badge" alt="English"></a>
    <a href="README.id.md"><img src="https://img.shields.io/badge/ID-0078D4.svg?style=for-the-badge" alt="Bahasa Indonesia"></a>
  </p>
</div>

KZRS adalah penerjemah manga dan komik untuk desktop, dibuat dengan Rust. KZRS menemukan balon
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
| macOS (Apple Silicon) | Segera hadir | |

Aplikasinya belum ditandatangani (code signing), jadi sistem akan bertanya sekali:

- **Windows**: "Windows protected your PC" → **More info** → **Run anyway**.
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
- **Editor halaman**: geser, ubah ukuran dan gaya kotak, kuas / restore / hapus, gambar dan
  layer, edit massal, undo per halaman.
- **Pembaca dan ekspor**: mode halaman atau webtoon, ekspor ke CBZ atau PDF.
- **Agen AI (Supporter)**: server MCP dan CLI, supaya Claude Code, OpenCode atau Codex bisa
  memeriksa dan memperbaiki halaman untukmu.

---

## Tangkapan layar

<p align="center"><img src="docs/assets/screenshots/translate.webp" width="900" alt="Translate"></p>
<p align="center"><sub>Translate: masukkan halaman, pilih bahasa dan AI, lalu tekan Translate.</sub></p>

<p align="center"><img src="docs/assets/screenshots/progress.webp" width="900" alt="Tiap halaman menunjukkan sejauh mana prosesnya selama chapter diterjemahkan."></p>
<p align="center"><sub>Tiap halaman menunjukkan sejauh mana prosesnya selama chapter diterjemahkan.</sub></p>

<p align="center"><img src="docs/assets/screenshots/editor.webp" width="900" alt="Editor"></p>
<p align="center"><sub>Editor: tiap balon adalah kotak teks yang bisa diketik ulang, diubah gayanya atau digeser.</sub></p>

<p align="center"><img src="docs/assets/screenshots/projects.webp" width="900" alt="Projects"></p>
<p align="center"><sub>Projects: tiap hasil terjemahan disimpan, bisa dibaca, diedit atau diekspor lagi.</sub></p>

<p align="center"><img src="docs/assets/screenshots/reader.webp" width="900" alt="Reader"></p>
<p align="center"><sub>Reader: mode halaman atau webtoon, bisa berdampingan dengan versi aslinya.</sub></p>

---

## Gratis dan Supporter

KZRS gratis dengan **10 halaman terjemahan** dan **5 halaman manual (khusus editor) per hari**.
Mengedit, membaca dan mengekspor hasil yang sudah ada tidak dibatasi. Tidak perlu akun.

Kode **Supporter** menghapus batas harian dan membuka command line serta tool agen AI (MCP) untuk
Claude Code, OpenCode dan Codex. Satu kode berlaku di satu komputer.

| Paket | Harga |
|---|---|
| Supporter · 1 tahun | Rp 20.000 |
| Supporter · 3 tahun | Rp 50.000 (hemat Rp 10.000) |

### Cara mendapatkan kode

1. Kirim pesan ke **Ardyan** di [Facebook](https://www.facebook.com/share/1FZ2SXJmeL/) dan sebutkan
   paket yang kamu mau: 1 tahun atau 3 tahun.
2. Bayar lewat **QRIS** (aplikasi bank atau e-wallet apa saja: GoPay, OVO, DANA, ShopeePay, m-banking).
3. Kirim bukti pembayaran di Facebook. Kode kamu (`KZRS-XXXX-XXXX-XXXX`) dikirim lewat pesan.
4. Di KZRS, buka *Supporter activation* (muncul saat pertama dibuka, atau klik chip di kanan bilah
   atas), tempel kodenya lalu tekan **Activate**.

Ganti komputer? Hapus perangkat lama di *Supporter activation*, lalu aktifkan kodenya di komputer baru.

<div align="center">
  <img src="docs/assets/qris.jpg" width="320" alt="QRIS: ARDYAN DEV, DIGITAL &amp; KREATIF" />
  <p><sub>QRIS · ARDYAN DEV, DIGITAL &amp; KREATIF</sub></p>
</div>

---

## Masukan

Bug dan ide: [Issues](https://github.com/kouzen-neo/kzrs/issues), atau [Facebook](https://www.facebook.com/share/1FZ2SXJmeL/).

Perubahan tiap versi: [CHANGELOG.md](CHANGELOG.md).

---

## Lisensi

Freeware proprietary. Hak cipta dilindungi.

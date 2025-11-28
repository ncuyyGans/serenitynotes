# SerenityNotes

Blog pribadi minimalis untuk berbagi catatan buku, kutipan berkesan, jurnal perjalanan, dan refleksi pelajaran hidup. Dikelola dengan Netlify CMS untuk kemudahan pengelolaan konten.

## Fitur

- **Desain Minimalis** - Fokus pada tipografi dan keterbacaan
- **Netlify CMS** - Admin panel untuk mengelola posting tanpa edit kode
- **Responsive** - Mobile-friendly layout
- **SEO-Ready** - Meta tags dan struktur yang optimal
- **4 Kategori** - Book Notes, Quotes, Travel, Reflections

## Deploy ke Netlify

### Cara Deploy (Drag & Drop)

1. **Buat ZIP dari folder ini**
   - Seleksi semua file di dalam folder `serenitynotes`
   - Buat file ZIP (misalnya: `serenitynotes.zip`)

2. **Upload ke Netlify**
   - Buka [Netlify](https://app.netlify.com)
   - Login atau buat akun baru (gratis)
   - Drag & drop file ZIP ke area "Want to deploy a new site without connecting to Git?"
   - Tunggu proses deployment selesai (biasanya 1-2 menit)

3. **Setup Netlify Identity & Git Gateway**

   Setelah site berhasil di-deploy, Anda perlu mengaktifkan Netlify Identity untuk bisa login ke admin panel:

   a. Di dashboard Netlify, pilih site Anda
   b. Klik **Identity** di menu atas
   c. Klik **Enable Identity**
   d. Scroll ke bawah, klik **Settings and usage**
   e. Scroll ke bagian **Services**, klik **Enable Git Gateway**
   f. Kembali ke tab **Identity**, klik **Invite users**
   g. Masukkan email Anda dan klik **Send**
   h. Cek email Anda dan klik link konfirmasi
   i. Set password untuk akun admin Anda

4. **Akses Admin Panel**
   - Buka `https://[your-site-name].netlify.app/admin`
   - Login dengan email dan password yang sudah Anda set
   - Mulai membuat posting baru!

### Cara Membuat Post Baru via CMS

1. Login ke `/admin`
2. Klik **New Posts** di Collections
3. Isi form:
   - **Title** - Judul posting
   - **Publish Date** - Tanggal publikasi
   - **Draft** - Centang jika ingin menyimpan sebagai draft
   - **Category** - Pilih kategori (book-notes, quotes, travel, reflections)
   - **Tags** - Tambahkan tag (opsional)
   - **Cover Image** - Upload gambar cover (opsional)
   - **Excerpt** - Ringkasan singkat untuk preview
   - **Body** - Konten utama (Markdown supported)
4. Klik **Publish** atau **Save Draft**
5. Post akan otomatis muncul di website Anda

## Struktur File

```
serenitynotes/
├── index.html              # Homepage dengan daftar posting
├── about.html              # Halaman About Me
├── contact.html            # Halaman Contact (form statis)
├── post.html               # Template untuk single post
├── posts/                  # Folder berisi halaman post individual
│   ├── book-notes.html
│   ├── quote.html
│   ├── travel-jakarta.html
│   └── reflection.html
├── admin/                  # Netlify CMS admin panel
│   ├── index.html
│   └── config.yml
├── content/posts/          # Markdown files untuk setiap post
│   ├── 2025-01-10-book-notes.md
│   ├── 2025-02-05-quote.md
│   ├── 2025-03-12-travel-jakarta.md
│   └── 2025-04-07-reflection.md
├── assets/                 # Folder untuk images & uploads
│   └── uploads/
├── css/
│   └── style.css           # Styling minimalis
├── js/
│   └── main.js             # JavaScript minimal untuk navigasi
├── LICENSE                 # License file
└── README.md               # Dokumentasi ini
```

## Kustomisasi

### Mengubah Warna

Edit file `css/style.css` dan ubah variabel warna:
- `#2b6cb0` - Warna aksen/link (biru)
- `#222` - Warna teks utama
- `#6b6b6b` - Warna teks sekunder
- `#ffffff` - Background putih

### Mengubah Font

Edit di bagian `<head>` pada file HTML, ganti Google Fonts URL untuk menggunakan font lain.

### Menambah Kategori Baru

1. Edit `admin/config.yml`
2. Tambahkan kategori baru di `options` field `category`
3. Tambahkan CSS untuk kategori baru di `css/style.css` (misal: `.category-new-category`)

## Menghubungkan dengan GitHub (Opsional)

Jika Anda ingin version control yang lebih baik:

1. Push folder ini ke GitHub repository
2. Di Netlify, klik **Site settings** > **Build & deploy**
3. Klik **Link repository**
4. Pilih repository GitHub Anda
5. Set build command: (kosongkan untuk static site)
6. Set publish directory: `/`
7. Deploy!

Setelah terhubung dengan GitHub, setiap perubahan yang Anda buat via CMS akan otomatis membuat commit ke repository.

## Tips

- **Backup konten**: Export posts dari CMS secara berkala
- **Optimasi gambar**: Compress gambar sebelum upload untuk performa lebih baik
- **Custom domain**: Di Netlify, bisa setup custom domain di Domain settings
- **HTTPS**: Netlify otomatis menyediakan SSL certificate gratis

## Support & Dokumentasi

- [Netlify Docs](https://docs.netlify.com/)
- [Netlify CMS Docs](https://www.netlifycms.org/docs/)
- [Markdown Guide](https://www.markdownguide.org/)

## License

MIT License - Copyright (c) 2025 Surya

---

**Dibuat dengan ❤️ untuk berbagi cerita dan pelajaran hidup**

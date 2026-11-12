# Kasir Toko - jadi aplikasi

Isi aplikasi (www/index.html) sama dengan versi 1.3.22; hanya ditambah manifest, service worker, dan ikon.

## Cara A - Pasang langsung dari Chrome (PWA), paling cepat
1. Taruh folder `www` di hosting https (GitHub Pages / Netlify / Cloudflare Pages, gratis).
2. Buka alamatnya di Chrome HP > menu titik tiga > "Pasang aplikasi" / "Tambahkan ke layar utama".
3. Setelah terpasang, aplikasi jalan offline.

## Cara B - APK sungguhan tanpa Android Studio (lewat GitHub)
1. Buat repo GitHub (privat boleh), unggah seluruh isi folder ini (termasuk `.github`).
2. Tab Actions > "Build APK" > Run workflow. Tunggu sekitar 5-10 menit.
3. Unduh artefak `Kasir_Toko_apk` > ekstrak > `app-debug.apk` > pasang di HP
   (izinkan "pasang dari sumber tidak dikenal").

## Cara C - Di komputer sendiri (Node 20+, JDK 21, Android Studio)
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android      # Build > Build APK

## Penting
- APK debug cukup untuk dipakai sendiri. Untuk rilis/Play Store, buat keystore dan build release; SIMPAN keystore-nya.
- Data di browser TIDAK ikut pindah ke APK. Sebelum pindah, ekspor cadangan di versi lama lalu impor di aplikasi baru.
- Cetak thermal Bluetooth dan scan barcode belum ada; bisa ditambahkan sebagai plugin Capacitor.
- Uji di HP: tombol bagikan/unduh file (nota, Excel, cadangan) di WebView Android.

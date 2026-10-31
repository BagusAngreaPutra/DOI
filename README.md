# Resolver simulasi doi-reg.org

Link: https://doi-reg.org/10.2498.jbmh.v10i2.2330

Upload index.php, config.php dan .htaccess ke document root domain doi-reg.org di hosting PHP/Apache. Arahkan DNS domain ke hosting, lalu aktifkan SSL/HTTPS. Domain saja belum menjalankan PHP.

Pastikan nama file aturan adalah `.htaccess` (dengan titik di depan), bukan `htaccess`. Jika URL DOI mendapat 404 tetapi `/index.php/10.21324/jpip.v19i2.98212` berhasil, periksa keberadaan `.htaccess` di document root dan pengaturan rewrite hosting.

Alamat tujuan artikel ada di config.php. Jalur /UNPAD/ mengikuti .cpanel.yml proyek. Hapus /UNPAD jika jurnal dipasang di root domain.

Kode dikenal dialihkan HTTP 302; kode lain mendapat HTTP 404. Kode ini merupakan simulasi, bukan DOI terdaftar. Tambahkan pemetaan di config.php untuk artikel berikutnya.

Uji lokal dari root proyek: php -S 127.0.0.1:8091 -t . index.php

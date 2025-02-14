# Belajar Integrasi DOKU Payment Gateway dengan Laravel 11

Project ini dibuat untuk pembelajaran dan testing integrasi pembayaran menggunakan DOKU Payment Gateway di Laravel 11.

## Teknologi yang Digunakan

-   PHP 8.2
-   Laravel 11
-   DOKU Payment Gateway
-   MySQL

## Instalasi

```bash
# Clone project
git clone https://github.com/tronout28/doku-payment.git

# Masuk ke direktori project
cd laravel-doku-payment

# Install dependensi
composer install

# Install DOKU Jokul Library
composer require doku/jokul-php-library

# Setup environment
cp .env.example .env
php artisan key:generate

# Jalankan migrasi database
php artisan migrate
```

## Konfigurasi DOKU

Tambahkan konfigurasi berikut di file `.env`:

```env
DOKU_CLIENT_ID=client_id_anda
DOKU_SECRET_KEY=secret_key_anda
DOKU_ENV=development
```

## Fitur yang Dipelajari

-   Membuat api dari sisi backend beserta snapnya
-   Integrasi dengan DOKU Payment
-   Mengupdate status pembayaran
-   Membuat invoice sederhana

## Endpoints API

-   POST `/api/doku/payment` - Membuat pembayaran baru
-   POST `/api/doku/notification` - Menerima notifikasi dari DOKU
-   GET `/api/transactions` - Mendapatkan list transaksi
-   GET `/api/transactions/{id}` - Detail transaksi

## Notes

Project ini dibuat untuk keperluan pembelajaran dan testing. Untuk penggunaan production, diperlukan konfigurasi tambahan terutama terkait keamanan.

## Referensi

-   [Dokumentasi DOKU](https://www.doku.com/API)
-   [Laravel Documentation](https://laravel.com/docs/11.x)

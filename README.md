<p align="center"><img src="https://statamic.com/assets/branding/Statamic-Logo+Wordmark-Rad.svg" width="400" alt="Statamic Logo" /></p>

## About Statamic 3

Statamic 3 is the flat-first, Laravel + Git powered CMS designed for building beautiful, easy to manage websites.

> **Note:** This repository contains the code for the Statamic application. To contribute to the core package, visit the [Statamic core package repository][cms-repo].


## Important Links

- [Statamic Main Site](https://statamic.com)
- [Statamic 3 Documentation][docs]
- [Statamic 3 Core Package Repo][cms-repo]
- [Statamic 3 Migrator](https://github.com/statamic/migrator)
- [Statamic Discord][discord]

# Requirement
- PHP 8.x.x
- composer
- Xampp/Laragon

# Instalasi Bootsrap 5 Pada Laravel Statamic 

## 1. Create Project Statamic
```
statamic new name-project
```

## 2. Install Laravel UI Untuk Bootstrap 5:
```
composer require laravel/ui
```

## 3. Membuat Autentikasi Dengan Bootstrap 5
```
php artisan ui bootstrap
```

## 4. Install NPM Dan NPM Run Build Untuk Menjalankan Bootstrap 5
```
npm install
```
```
npm run build
```

## 5. Pasang/Tambahkan Source Dibawah Pada halaman yang akan menggunakan Bootstrap 5
```
{{ vite src="resources/js/app.js|resources/sass/app.scss" }}
```

## 6. Jalankan Project 
```
php artisan serve
```

# Setting package.json (Bila terjadi error pada langkah no. 4)

## Membuat Dependensi Baru
```
npm install --save-dev vite laravel-vite-plugin
```

## Buka file package.json. Hapus semua yang ada pada scripts{} Ubah dengan kode dibawah ini:
```
"scripts": {
    "dev": "vite",
    "build": "vite build"
},
```

## Karena Vite adalah pengganti webpack, kita dapat menghapus laravel-mix dan menghapus file webpack.mix.js dari aplikasi sebelumnya:
```
npm remove laravel-mix && rm webpack.mix.js
```

### Tampilan package.json setelah di setting
```
{
    "private": true,
    "scripts": {
        "dev": "vite",
        "build": "vite build"
    },
    "devDependencies": {
        "@popperjs/core": "^2.11.6",
        "axios": "^0.25",
        "bootstrap": "^5.2.3",
        "laravel-vite-plugin": "^0.7.4",
        "lodash": "^4.17.19",
        "postcss": "^8.1.14",
        "sass": "^1.56.1",
        "vite": "^4.2.1"
    }
}
```

## Buat File Baru Dengan Nama  app.js Pada Folder resouces/js/ (Hanya Khusus Pada Project Laravel Statamic Sedangkan Pada Laravel Biasa Sudah Ada Tidak Harus Buat Lagi). Kemuadian Isi File Dengan Source:
```
require('./bootstrap');
```

## Jalankan Kembali Langkah No. 4 (npm run build)

# Tampilan Aplikasi Hasil Deploy Fly.io
https://fly-statamic-bio-bootstrap.fly.dev/

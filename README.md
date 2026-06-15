# Odoo

[![Build Status](https://runbot.odoo.com/runbot/badge/flat/1/master.svg)](https://runbot.odoo.com/runbot)
[![Tech Doc](https://img.shields.io/badge/master-docs-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/documentation/master)
[![Help](https://img.shields.io/badge/master-help-875A7B.svg?style=flat&colorA=8F8F8F)](https://www.odoo.com/forum/help-1)
[![Nightly Builds](https://img.shields.io/badge/master-nightly-875A7B.svg?style=flat&colorA=8F8F8F)](https://nightly.odoo.com/)

Odoo is a suite of web based open source business apps.

The main Odoo Apps include an [Open Source CRM](https://www.odoo.com/page/crm),
[Website Builder](https://www.odoo.com/app/website),
[eCommerce](https://www.odoo.com/app/ecommerce),
[Warehouse Management](https://www.odoo.com/app/inventory),
[Project Management](https://www.odoo.com/app/project),
[Billing &amp; Accounting](https://www.odoo.com/app/accounting),
[Point of Sale](https://www.odoo.com/app/point-of-sale-shop),
[Human Resources](https://www.odoo.com/app/employees),
[Marketing](https://www.odoo.com/app/social-marketing),
[Manufacturing](https://www.odoo.com/app/manufacturing),
[...](https://www.odoo.com/)

Odoo Apps can be used as stand-alone applications, but they also integrate seamlessly so you get
a full-featured [Open Source ERP](https://www.odoo.com) when you install several Apps.

## Getting started with Odoo

For a standard installation please follow the [Setup instructions](https://www.odoo.com/documentation/master/administration/install/install.html)
from the documentation.

### Langkah-langkah Instalasi Lokal

Ikuti langkah-langkah berikut untuk menginstal dan menjalankan aplikasi ini secara lokal:

1. **Persyaratan Sistem:**
   - Pastikan **Python** (versi 3.12 atau lebih baru) telah terinstal di sistem Anda.
   - Pastikan **PostgreSQL** telah terinstal dan berjalan. Buat user dan database untuk aplikasi Odoo.

2. **Membuat Virtual Environment:**
   Buat virtual environment baru bernama `odoo-venv` menggunakan terminal:
   ```cmd
   python -m venv odoo-venv
   ```

3. **Aktivasi Virtual Environment:**
   Aktifkan virtual environment tersebut melalui terminal.
   Jika menggunakan PowerShell:
   ```powershell
   .\odoo-venv\Scripts\Activate.ps1
   ```
   Jika menggunakan Command Prompt:
   ```cmd
   .\odoo-venv\Scripts\activate.bat
   ```

4. **Instalasi Dependencies:**
   Setelah virtual environment aktif, update `pip` terlebih dahulu dengan perintah:
   ```cmd
   python -m pip install --upgrade pip
   ```
   Kemudian instal semua library yang dibutuhkan:
   ```cmd
   pip install -r requirements.txt
   ```

5. **Konfigurasi Database:**
   Salin file konfigurasi bawaan dari folder `debian` ke direktori utama dengan perintah:
   ```cmd
   cp .\debian\odoo.conf .\odoo.conf
   ```
   Selanjutnya, buka dan sesuaikan file konfigurasi `odoo.conf` tersebut. Pastikan kredensial PostgreSQL Anda (`db_host`, `db_port`, `db_user`, dan `db_password`) sudah sesuai.

6. **Menjalankan Aplikasi:**
   Jalankan server Odoo menggunakan file konfigurasi yang sudah disiapkan dengan perintah:
   ```cmd
   python odoo-bin -c odoo.conf
   ```

7. **Akses Aplikasi:**
   Buka web browser dan akses alamat `http://localhost:8069` untuk membuka halaman aplikasi Odoo Anda.

To learn the software, we recommend the [Odoo eLearning](https://www.odoo.com/slides),
or [Scale-up, the business game](https://www.odoo.com/page/scale-up-business-game).
Developers can start with [the developer tutorials](https://www.odoo.com/documentation/master/developer/howtos.html).

## Security

If you believe you have found a security issue, check our [Responsible Disclosure page](https://www.odoo.com/security-report)
for details and get in touch with us via email.

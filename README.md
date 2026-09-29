# OTW-TL (On The Way - Timur Leste) 🚗🛵

**OTW-TL** adalah *Minimum Viable Product* (MVP) platform *ride-hailing* (serupa Gojek/Grab) yang dirancang khusus untuk kebutuhan transportasi digital di Timor Leste. 

Sistem ini dikembangkan secara *full-stack* menggunakan **Java Quarkus** pada sisi backend dan **Next.js** pada sisi frontend, serta dilengkapi dengan kalkulasi tarif per kilometer, integrasi peta digital, dan gerbang pembayaran (*payment gateway*).

---

## 🏗️ Tech Stack & Arsitektur

### **Backend**
* **Framework:** Java Quarkus (High-performance, Cloud-native Java)
* **Database:** PostgreSQL
* **Fitur Utama:**
  * Modul kalkulasi tarif otomatis berdasarkan jarak ($/km)
  * REST API untuk manajemen transaksi, *order*, dan *user/driver*

### **Frontend**
* **Framework:** Next.js (React Framework, App/Pages Router)
* **Styling & UI:** TypeScript / HTML / CSS

### **Integrasi Pihak Ketiga**
* **Google Maps API:** Untuk geolokasi, pencarian rute, dan perhitungan jarak rute.
* **Payment Gateway (Sandbox):** Midtrans / Xendit *(Siap dihubungkan ke penyedia layanan pembayaran)*.

---

## 📁 Struktur Repositori

```text
Dimata_bootcamp/
├── app-taksol/      # Layanan utama Backend (Java Quarkus)
├── taksol/          # Konfigurasi / modul pendukung Backend
├── taksol-fe/       # Aplikasi Client Frontend (Next.js)
└── docs/            # Dokumentasi arsitektur & API


Fitur Utama (MVP)
Pemesanan Perjalanan (Ride Ordering): Menentukan titik penjemputan dan tujuan menggunakan integrasi Google Maps.

Kalkulasi Tarif Otomatis: Perhitungan estimasi biaya perjalanan secara real-time berdasarkan jarak per kilometer.

Pembayaran Digital (Sandbox): Simulasi transaksi pembayaran aman sebelum pesanan diproses.

Backend Berperforma Tinggi: Pemrosesan logika bisnis dan kueri database yang ringan berkat arsitektur Java Quarkus.



🛠️ Cara Menjalankan Proyek (Local Development)
Prasyarat
Java JDK 17+ & Maven

Node.js 18+ & npm/pnpm

PostgreSQL Database

Google Maps API Key

1. Backend (Java Quarkus)
cd taksol
# Jalankan mode pengembangan
./mvnw quarkus:dev

2. Frontend (Next.js)
cd taksol-fe
# Install dependensi
npm install

# Jalankan server pengembangan
npm run dev


Catatan Proyek
Status: Archived / Discontinued MVP.
Proyek ini dibangun sebagai bukti konsep (PoC) dan fondasi sistem ride-hailing untuk Timor Leste.
Pengembangan saat ini telah dihentikan, namun repositori ini berfungsi sebagai referensi arsitektur full-stack microservices/monolith-decoupled.


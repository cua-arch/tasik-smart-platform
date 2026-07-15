# Tasik Smart Platform (TSP)

> Government Digital Platform untuk mendukung transformasi digital Pemerintah Kota Tasikmalaya.

## Tentang Proyek

Tasik Smart Platform (TSP) adalah platform digital berbasis web yang dirancang untuk mendukung implementasi SPBE (Sistem Pemerintahan Berbasis Elektronik) dan Satu Data Indonesia di lingkungan Pemerintah Kota Tasikmalaya.

Implementasi pertama platform ini adalah **Tasik Smart Food Hub (TSFH)** yang mendukung layanan sektor:

- Ketahanan Pangan
- Pertanian
- Perikanan
- Pelayanan Publik
- Dashboard Eksekutif
- GIS (Geographic Information System)

Platform dikembangkan menggunakan pendekatan **Modular Monolith**, sehingga mudah dikembangkan menjadi arsitektur terdistribusi apabila diperlukan di masa depan.

---

# Arsitektur Teknologi

| Layer | Teknologi |
|--------|-----------|
| Frontend | Vue 3 + TypeScript |
| Backend | Laravel 12 |
| Database | PostgreSQL 17 + PostGIS |
| Authentication | Keycloak |
| Cache | Redis |
| Storage | MinIO |
| Reverse Proxy | Nginx |
| Container | Docker Compose |
| API | REST + OpenAPI 3.1 |

---

# Struktur Repository

```
tasik-smart-platform/
│
├── backend/
├── frontend/
├── infrastructure/
├── database/
├── docs/
├── api/
├── deployment/
├── scripts/
├── .github/
│
├── docker-compose.yml
├── .env.example
├── README.md
└── LICENSE
```

---

# Modul

## Core Platform

- Authentication
- User Management
- Role & Permission
- Organization
- Workflow
- Notification
- Audit Trail
- File Management
- Dashboard Engine

## Master Data

- Kecamatan
- Kelurahan
- Petani
- Nelayan
- Kelompok Tani
- Pokdakan
- Komoditas
- Satuan

## Agriculture

- Lahan
- Produksi
- Alsintan
- Pupuk
- Bibit

## Fisheries

- Kolam
- Produksi
- Budidaya

## Food Security

- Harga
- Stok
- Distribusi
- Cadangan Pangan

## Public Service

- Pengajuan
- Pengaduan
- Konsultasi

## GIS

- Layer
- Polygon
- Point
- Dashboard Peta

---

# Persyaratan

- Docker Desktop / Docker Engine
- Docker Compose
- Git

---

# Menjalankan Proyek

```bash
git clone https://github.com/<organization>/tasik-smart-platform.git

cd tasik-smart-platform

docker compose up -d
```

Setelah seluruh container aktif:

| Service | URL |
|----------|-----|
| Frontend | http://localhost |
| Backend API | http://localhost/api |
| Swagger | http://localhost/swagger |
| Keycloak | http://localhost:8080 |
| Mailpit | http://localhost:8025 |
| MinIO | http://localhost:9001 |
| pgAdmin | http://localhost:5050 |

---

# Dokumentasi

Seluruh dokumentasi proyek tersedia pada folder:

```
docs/
```

Dokumentasi meliputi:

- Project Charter
- Software Requirements Specification (SRS)
- Business Rules
- Architecture
- BPMN
- ERD
- API Specification
- Deployment Guide
- User Manual

---

# Standar Pengembangan

- Conventional Commits
- GitHub Flow
- OpenAPI 3.1
- PSR-12
- Laravel Pint
- PHPStan
- Pest
- ESLint
- Prettier
- Vitest

---

# Lisensi

Internal Government Project.

Hak cipta © Pemerintah Kota Tasikmalaya.

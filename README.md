# MICROSERVICES ARCHITECTURE

# Kenapa Perlu Belajar Microservices?
- Kekinian
- Ekosistem Pendukung(docker, kubenetes, kafka, elasticsearh, dll)
- Banyak Digunakan di Tech Company
- Sudah Jadi Pengetahuan Wajib untuk Senior Engineer

---

# Arsitektur Monolith
## Apa itu Arsitektur Monolith?
- Single Deployment Unit
- Dimana semua fitur dibuat dalam sebuah aplikasi besar

## Arsitektur Monolith
[https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g65395d66ab_1_14#slide=id.g65395d66ab_1_14](https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g65395d66ab_1_14#slide=id.g65395d66ab_1_14)

# Mulailah dari Aplikasi Monolith
- kalo bikin awal aplikasi pakai arsitektur monolith dulu
- kalo dibutuhin baru di buat microservice

## Kelebihan Arsitektur Monolith
- Mudah di Develop
- Mudah di Deploy
- Mudah di Test
- Mudah di Scale

## Masalah di Arsitektur Monolith
- Mengintimidasi Developer yang baru bergabung
- Scaling development dengan banyak Developer agak menyulitkan
- Butuh kontrak panjang dengan teknologi yang digunakan (bahasa pemrograman, database, dan lain-lain)
- Scaling pada bagian tertentu tidak bisa dilakukan
- Running app Monolith sangat berat(bisa sampai 15 menit restart app kalau app sudah gede banget)

---

# Arsitektur Microservices
## Apa itu Arsitektur Microservices
- Aplikasi-aplikasi kecil yang saling bekerja sama.
- Fokus mengerjakan satu pekerjaan dengan baik
- Independent, dapat di deploy dan diubah tanpa tergantung dengan aplikasi lain
- Setiap komponen pada sistem dibuat dalam service
- Komunikasi antar service biasanya melalui network-call(http api, dll)

## Arsitektur Microservices
[https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g6f889abcc1_0_19#slide=id.g6f889abcc1_0_19](https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g6f889abcc1_0_19#slide=id.g6f889abcc1_0_19)

## Kelebihan Arsitektur Microservices
- Mudah dimengerti, karena relative kecil ukuran service nya
- Lebih mudah di develop, di maintain, di test dan di deploy
- Lebih mudah bergonta-ganti teknologi
- Mudah di scale sesuai kebutuhan
- Bisa dikerjakan dalam tim-tim kecil

## Masalah di Arsitektur Microservices
- Distributed system
- Komunikasi antar service yang rawan error
- Testing interaksi antar service lebih sulit

## Pembagian Aplikasi Microservices
[https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g6f8f962e73_1_17#slide=id.g6f8f962e73_1_17](https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g6f8f962e73_1_17#slide=id.g6f8f962e73_1_17)
- per tim pegang 1 service/business domain

## Seberapa Kecil Aplikasi Microservices?
- Single responsibility
- Sekecil mungkin sehingga bisa dimengerti oleh satu orang
- Bisa di kerjakan sejumlah X developer


## Kapan pilih arsitektur?
### Monolith
- Simplicity
- Consistency
- Easy to Refactor

### Microservices
- Partial Deployment
- Availability
- Multiple Platform
- Easy to Scale

---

# Database per Service
- tiap service punya database masing masing

## Decentralized Database
[arch\database-per-service.excalidraw.png](arch\database-per-service.excalidraw.png)


## Kenapa Harus Database per Service?
- Memastikan bahwa antar service tidak ketergantungan
- Tiap service bisa menggunakan aplikasi database sesuai dengan kebutuhan
- Service tidak perlu tahu kompleksitas internal database service lain

## Contoh Database per Service
[arch\database-per-service.excalidraw.png](arch\database-per-service.excalidraw.png)

---

# Shared Database

## Shared Database
[arch\shared-database.excalidraw.png](arch\shared-database.excalidraw.png)

## Kapan Harus Shared Database?
- Ketika melakukan transisi dari aplikasi Monolith ke Microservices
- Ketika bingung memecahkan data antar Service
- Ketika dikejar waktu, sehingga tidak ada waktu untuk bikin API

## Contoh Shared Database
[arch\shared-database.excalidraw.png](arch\shared-database.excalidraw.png)


---

# NoSQL
## Apa itu NoSQL?
- NoSQL bukanlah NO (TIDAK/BUKAN) SQL
- NoSQL singkatan dari Not Only SQL
- yang berarti bukan sql saja yang bisa di buat database/simpan data

## Jenis-Jenis NoSQL
- Document Oriented Database
- Key-Value  Database
- Column Families Database
- Graph Database
- Search Database
- Time Series Database
- Dan lain-lain

## Contoh NoSQL Database
- MongoDB : Document Oriented Database 
- Elasticsearch : Search Database
- Redis : Key-Value Database
- Apache Cassandra : Column Families Database
- Neo4J : Graph Database
- InfluxDB : Time Series Database

## Kenapa Butuh Tahu NoSQL?
- Agar bisa disesuaikan dengan kebutuhan
- Bisa mencari alternatif cara mengolah data
- Mempercepat dalam proses penulisan atau pencarian

## Contoh Kasus
[arch\nosql-case.excalidraw.png](arch\nosql-case.excalidraw.png)




















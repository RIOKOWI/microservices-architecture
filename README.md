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
[arch\monolith-arch.excalidraw.png](arch\monolith-arch.excalidraw.png)

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
[arch\microcervices-arch.excalidraw.png](arch\microcervices-arch.excalidraw.png)

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
[arch\microcervices-arch.excalidraw.png](arch\microcervices-arch.excalidraw.png)
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

# Remote Procedure Invocation

## Ketika Service butuh Data Service Lain
[arch\remote-procedure-invocation.excalidraw.png](arch\remote-procedure-invocation.excalidraw.png)

## Komunikasi Antar Service
- Idealnya komunikasi dilakukan melalui RPI (Remote Procedure Invocation) atau RPC (Remote Procedure Call)
- Tidak direkomendasikan komunikasi dilakukan via database

## Contoh Remote Procedure Invocation
- RESTful API (HTTP)
- gRPC
- Apache Thrift 
- SOAP
- Java RMI
- Corba (Common Object Request Broker Architecture)
- dan lain-lain

## Ketika Service butuh Data Service Lain
[arch\remote-procedure-invocation.excalidraw.png](arch\remote-procedure-invocation.excalidraw.png)


## Keuntungan Menggunakan RPI
- Sederhana dan Mudah
- Biasanya digunakan untuk komunikasi Request - Reply
- Biasanya digunakan untuk proses Sync (yang butuh menunggu jawaban)


# Messaging
## Ketika Service butuh Data Service Lain
[arch\messagging.excalidraw.png](arch\messagging.excalidraw.png)

## Komunikasi Menggunakan RPI
[arch\messagging.excalidraw.png](arch\messagging.excalidraw.png)

## Masalah di Komunikasi RPI
- Proses lama (pada Email Service dan SMS Service)
- Mengirim data yang sama berkali-kali (pada Finance Service dan Report Service)
- Membuat Paralel Process sangat rumit

## Komunikasi dengan Cara Messaging 
- Messaging biasanya digunakan untuk komunikasi Async
- Async artinya komunikasi dilakukan tanpa harus menunggu selesai di proses
- Dalam async, kadang tidak perlu peduli balasan dari service yang dituju
- Biasanya komunikasi Messaging membutuhkan Message Channel sebagai jembatan untuk mengirim dan menerima data
- Direkomendasikan menggunakan aplikasi Message Broker untuk melakukan management Message Channel

## Komunikasi Menggunakan Messaging
[arch\messagging.excalidraw.png](arch\messagging.excalidraw.png)

## Contoh Message Broker
- Redis (PubSub)
- Apache Kafka
- RabbitMQ
- NSQ
- Google PubSub
- Amazon Web Service SQS
- dan lain-lain

## Keuntungan Menggunakan Messaging
- Proses lebih cepat karena tidak harus menunggu response
- Service pengirim data tidak perlu peduli terhadap penerima data

## Rekomendasi
- get data pakai rpi
- post data secara async pakai messaging

# Type of Microservices
## Tipe Microservices
- Stateless Microservice
- Persistence Microservice
- Aggregation Microservices

## Stateless Microservices
- Biasanya tidak memiliki database
- Digunakan untuk melakukan tugas sederhana
- Biasa digunakan juga sebagai utility untuk microservice lain
- Tidak bergantung dengan microservice lain

## Contoh Stateless Microservices
[arch\type-of-microservice.excalidraw.png](arch\type-of-microservice.excalidraw.png)


## Persistence Microservices
- Biasanya memiliki database 
- Bisa juga disebut sebagai Master Data Microservice
- Biasa digunakan untuk mengolah data di database (CRUD)

## Contoh Persistence Microservices
[arch\type-of-microservice.excalidraw.png](arch\type-of-microservice.excalidraw.png)

## Aggregation Microservices
- Tergantung dengan microservice lain
- Biasa digunakan sebagai pusat business logic aplikasi
- Boleh memiliki database ataupun tidak
- Tidak bisa berdiri sendiri

## Contoh Aggregation Microservices
[https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g7c2be31d00_0_40#slide=id.g7c2be31d00_0_40](https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g7c2be31d00_0_40#slide=id.g7c2be31d00_0_40)

## Contoh Kasus
[https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g7c2be31d00_0_45#slide=id.g7c2be31d00_0_45](https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/edit?slide=id.g7c2be31d00_0_45#slide=id.g7c2be31d00_0_45)
































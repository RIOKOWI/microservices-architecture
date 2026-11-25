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

## SOURCE
[https://www.youtube.com/watch?v=CHBfpPMILaQ&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=2](https://www.youtube.com/watch?v=CHBfpPMILaQ&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=2)

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

## SOURCE
[https://www.youtube.com/watch?v=W96gPBQ0blE&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=3](https://www.youtube.com/watch?v=W96gPBQ0blE&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=3)

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

## SOURCE
[https://www.youtube.com/watch?v=W4G-cr5m5Do&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=4](https://www.youtube.com/watch?v=W4G-cr5m5Do&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=4)

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

## SOURCE
[https://www.youtube.com/watch?v=jYuo2_DMasI&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=5](https://www.youtube.com/watch?v=jYuo2_DMasI&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=5)

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

## SOURCE
[https://www.youtube.com/watch?v=Pw34eg_6ve4&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=6](https://www.youtube.com/watch?v=Pw34eg_6ve4&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=6)

---

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

## SOURCE
[https://www.youtube.com/watch?v=Rsi8mxVX70M&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=7](https://www.youtube.com/watch?v=Rsi8mxVX70M&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=7)

---

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

## SOURCE
[https://www.youtube.com/watch?v=IgJ8RBsRGoM&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=8](https://www.youtube.com/watch?v=IgJ8RBsRGoM&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=8)

---

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
[arch\type-of-microservice.excalidraw.png](arch\type-of-microservice.excalidraw.png)

## Contoh Kasus
[arch\type-of-microservice.excalidraw.png](arch\type-of-microservice.excalidraw.png)

## SOURCE
[https://www.youtube.com/watch?v=SFkPLgpFiT4&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=9](https://www.youtube.com/watch?v=SFkPLgpFiT4&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=9)

---

# Service Orchestration
## Service Orchestration
- Sebelumnya kita sudah bahas tentang tipe Aggregation Microservices
- Cara Aggregation Microservices berkomunikasi dengan Microservices lain, jika menggunakan Remote Procedure Invocation, maka dinamakan Service Orchestration Pattern
- Dalam Service Orchestration Pattern, Aggregation Microservices bertugas untuk mengatur alur business logic sistem.

## Contoh Service Orchestration
[arch\orchestration.excalidraw.png](arch\orchestration.excalidraw.png)

## Keuntungan Service Orchestration
- Mudah dibuat, karena kode business logic akan terpusat di Aggregation Microservices
- Mudah dimengerti, karena kode business logic akan terpusat di Aggregation Microservices

## Kekurangan Service Orchestration
- Aggregation Microservices terlalu ketergantungan dengan Microservices lain
- Aggregation Microservices akan lebih lambat karena harus terkoneksi dengan Microservices lain
- Aggregation Microservices akan lebih mudah error jika di Microservices lain terdapat masalah
- Jika perlu Microservices baru, perlu dilakukan perubahan di Aggregation Microservices


## SOURCE
[https://www.youtube.com/watch?v=WTLGEsmKves&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=10](https://www.youtube.com/watch?v=WTLGEsmKves&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=10)


---

# Service Choreography
## Service Choreography
- Service Choreography berbeda dengan Service Orchestration. 
- Dalam Service Choreography, komunikasi Aggregation Service dengan Microservices lainnya menggunakan Messaging.
- Dalam Service Orchestration, Aggregation Microservice adalah service yang sangat kompleks dan mengerti semua alur business logic, sedangkan berbeda dengan Service Choreography, semua Microservices dituntut untuk menjadi pintar, tidak hanya diperintah oleh Aggregation Microservices.

## Contoh Service Choreography
[arch\choreography.excalidraw.png](arch\choreography.excalidraw.png)

## Keuntungan Service Choreography
- Aggregation Microservices tidak tergantung dengan Microservices lainnya
- Aggregation Microservice akan lebih cepat, karena tidak perlu berkomunikasi dengan Microservices lainnya
- Jika ada Microservice baru, Aggregation Microservice tidak perlu melakukan perubahan lagi

## Kekurangan Service Choreography
- Lebih sulit di-debug ketika terjadi masalah
- Business logic akan terdistribusi di semua Microservices, sehingga sulit untuk dimengerti secara keseluruhan
- bergantung banget dengan message broker, pilihlah message broker yang bagus dan scalable

## Rekomendasi
- kalo tim masih sedikit belum ada yang senior pake service orchestration dan sebaliknya

## SOURCE
[https://www.youtube.com/watch?v=zgu2r3_2i_E&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=11](https://www.youtube.com/watch?v=zgu2r3_2i_E&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=11)

---

# API  Gateway
## Mengekspos Microservices
[arch\api-gateway.excalidraw.png](arch\api-gateway.excalidraw.png)

## Masalah Mengekspos Microservices
- Semua service bisa diakses dari luar
- Jika butuh Autentikasi, harus diimplementasikan di semua service
- Rawan terjadi kebocoran data

## API Gateway
- API Gateway adalah aplikasi yang bertugas sebagai gerbang dari luar ke dalam
- Luar adalah akses dari internet, dan Dalam adalah aplikasi microservices
- API Gateway bertugas sebagai proxy server ke semua aplikasi microservices
- Aplikasi microservices hanya bisa diakses dari luar melalui API Gateway

## API Gateway
- API Gateway adalah aplikasi yang bertugas sebagai gerbang dari luar ke dalam
- Luar adalah akses dari internet, dan Dalam adalah aplikasi microservices
- API Gateway bertugas sebagai proxy server ke semua aplikasi microservices
- Aplikasi microservices hanya bisa diakses dari luar melalui API Gateway

## API Gateway
[arch\api-gateway.excalidraw.png](arch\api-gateway.excalidraw.png)

## Keuntungan API Gateway
- Lebih aman karena satu gerbang
- Service tidak perlu mengimplementasikan proses Autentikasi, cukup dilakukan di API Gateway
- API Gateway juga bisa digunakan sebagai load balancer
- Bisa digunakan sebagai rate limiter
- Bisa digunakan sebagai pengaman sehingga error dari service tidak terekspos

## Contoh API Gateway
- Nginx
- Apache HTTPD
- Kong
- Netflix Zuul
- Spring Cloud Gateway

## SOURCE
[https://www.youtube.com/watch?v=6qzD87wQTDA&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=12](https://www.youtube.com/watch?v=6qzD87wQTDA&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=12)


--- 

# Authentication & Authorization
## Bagaimana Mengamankan Microservices?
[arch\auth.excalidraw.png](arch\auth.excalidraw.png)

## Authentication dan Authorization
Authentication :
- Memvalidasi kredensial  untuk memverifikasi pemilik identitas
- Contoh proses Authentication adalah proses login menggunakan username dan password, dan banyak yang lainnya.

Authorization :
- Authorization adalah proses yang dilakukan setelah proses Authentication
- Memvalidasi apakah pemilik identitas memiliki hak akses untuk mengakses resource yang diminta
- Contoh proses Authorization adalah Access-Control List, dan banyak yang lainnya.

## Auth Service
[arch\auth.excalidraw.png](arch\auth.excalidraw.png)

## Integrasi dengan Auth Service
[arch\auth.excalidraw.png](arch\auth.excalidraw.png)

## API Gateway sebagai Middleware
[arch\auth.excalidraw.png](arch\auth.excalidraw.png)

## Teknologi Pendukung
- Secure Cookie
- Oauth
- JSON Web Token
- Basic Auth
- API Key / Secret Key

## SOURCE
[https://www.youtube.com/watch?v=JZ8CW5tgXuY&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=13](https://www.youtube.com/watch?v=JZ8CW5tgXuY&list=PL-CtdCApEFH-MtoBwQ0F3xNG21yjt5Kvs&index=13)

--- 























































---

## SLIDE
[https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/](https://docs.google.com/presentation/d/1lKnpXhljmYwKgdnb1K8GDrpCYuao_ZHHGn24gX_um2M/)





























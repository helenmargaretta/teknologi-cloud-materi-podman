# Pengantar Podman

## Apa itu Podman?

Podman adalah sebuah alat manajemen container yang memungkinkan pengguna untuk menjalankan dan mengelola container serta image container. Sama seperti Docker, Podman menggunakan konsep yang sama dalam hal pengelolaan container, tetapi tanpa perlu menjalankan daemon yang terus-menerus seperti pada Docker.

Podman dikembangkan oleh Red Hat sebagai bagian dari proyek libpod, dengan tujuan untuk menyediakan alternatif open-source dari Docker yang lebih fleksibel dan aman. Salah satu fitur utamanya adalah kemampuan untuk menjalankan container rootless, artinya container dapat dijalankan tanpa hak akses root, sehingga meningkatkan keamanan.

## Fitur Utama Podman

1. **Daemonless (Tanpa Daemon)**  
   Tidak seperti Docker yang bergantung pada daemon yang berjalan di latar belakang, Podman adalah alat daemonless. Ini berarti setiap container dijalankan sebagai proses anak dari proses yang menjalankan Podman itu sendiri.

2. **Rootless Containers**  
   Podman memungkinkan pengguna non-root untuk menjalankan container, yang membuatnya lebih aman. Dengan demikian, Anda dapat menjalankan container tanpa memberikan hak akses root, yang mengurangi risiko keamanan.

3. **Kompatibilitas dengan Docker**  
   Podman memiliki kompatibilitas yang sangat tinggi dengan Docker. Sebagian besar perintah Docker dapat dijalankan di Podman dengan sedikit atau tanpa modifikasi. Podman juga mendukung penggunaan file `Dockerfile` untuk membangun container image.

4. **Mengelola Pods**  
   Podman juga mendukung konsep **pods**, yang diambil dari Kubernetes. Sebuah pod adalah grup container yang berbagi jaringan dan namespace. Ini membuat Podman menjadi alat yang bagus untuk mensimulasikan beban kerja Kubernetes di mesin lokal.

## Perbandingan Podman dan Docker

| Fitur            | Podman                                      | Docker                                 |
|------------------|---------------------------------------------|----------------------------------------|
| Arsitektur       | Daemonless, proses per container             | Berbasis daemon, satu proses mengelola semua container |
| Rootless         | Ya                                           | Tidak secara default                   |
| Kompatibilitas   | Kompatibel dengan CLI Docker                 | N/A                                    |
| Pod Management   | Mendukung konsep pods seperti di Kubernetes  | Tidak mendukung pods secara langsung   |

## Instalasi Podman

### Di Linux (Ubuntu)

1. Update repository:
   ```bash
   sudo apt update

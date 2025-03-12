# 🐳 Daftar Perintah Docker Lengkap

Berikut adalah daftar lengkap perintah **Docker** yang dikelompokkan berdasarkan fungsinya.

---

## 🚀 1. Perintah Dasar Docker
| Perintah | Deskripsi |
|----------|-----------|
| `docker version` | Menampilkan versi Docker yang terinstal |
| `docker info` | Menampilkan informasi detail tentang instalasi Docker |
| `docker help` | Menampilkan daftar perintah Docker yang tersedia |

---

## 📦 2. Perintah untuk Container
### 🔹 Menjalankan Container
| Perintah | Deskripsi |
|----------|-----------|
| `docker run [image]` | Menjalankan container dari image |
| `docker run -d [image]` | Menjalankan container di background (detached) |
| `docker run -it [image]` | Menjalankan container secara interaktif dengan terminal |
| `docker run --name [name] [image]` | Menjalankan container dengan nama tertentu |
| `docker run -p [host_port]:[container_port] [image]` | Menjalankan container dengan mapping port |
| `docker run -v [host_path]:[container_path] [image]` | Menjalankan container dengan volume (bind mount) |

### 🔹 Melihat Container
| Perintah | Deskripsi |
|----------|-----------|
| `docker ps` | Menampilkan container yang sedang berjalan |
| `docker ps -a` | Menampilkan semua container (termasuk yang sudah berhenti) |
| `docker ps -q` | Menampilkan hanya ID container yang sedang berjalan |
| `docker top [container]` | Menampilkan proses yang berjalan di dalam container |

### 🔹 Menghentikan & Menghapus Container
| Perintah | Deskripsi |
|----------|-----------|
| `docker stop [container]` | Menghentikan container |
| `docker start [container]` | Menjalankan ulang container |
| `docker restart [container]` | Merestart container |
| `docker kill [container]` | Menghentikan container secara paksa |
| `docker rm [container]` | Menghapus container |
| `docker rm $(docker ps -aq)` | Menghapus semua container yang sudah berhenti |

### 🔹 Masuk ke Container
| Perintah | Deskripsi |
|----------|-----------|
| `docker attach [container]` | Terhubung ke container yang sedang berjalan |
| `docker exec -it [container] bash` | Masuk ke dalam shell container (bash) |
| `docker logs [container]` | Melihat log container |
| `docker logs -f [container]` | Melihat log secara real-time |

### 🔹 Mengcopy File ke/Dari Container
| Perintah | Deskripsi |
|----------|-----------|
| `docker cp [container]:[path_in_container] [host_path]` | Mengcopy file dari container ke host |
| `docker cp [host_path] [container]:[path_in_container]` | Mengcopy file dari host ke container |

---

## 📸 3. Perintah untuk Image
### 🔹 Menarik & Membuat Image
| Perintah | Deskripsi |
|----------|-----------|
| `docker pull [image]` | Menarik image dari Docker Hub |
| `docker build -t [name] .` | Membuat image dari Dockerfile |
| `docker commit [container] [repository:tag]` | Membuat image dari container yang sedang berjalan |

### 🔹 Melihat & Menghapus Image
| Perintah | Deskripsi |
|----------|-----------|
| `docker images` | Menampilkan semua image yang tersedia |
| `docker rmi [image]` | Menghapus image |
| `docker rmi $(docker images -q)` | Menghapus semua image |

---

## 📂 4. Perintah untuk Volume
| Perintah | Deskripsi |
|----------|-----------|
| `docker volume create [name]` | Membuat volume baru |
| `docker volume ls` | Menampilkan daftar volume |
| `docker volume inspect [name]` | Menampilkan detail volume |
| `docker volume rm [name]` | Menghapus volume |

---

## 🌐 5. Perintah untuk Jaringan (Network)
| Perintah | Deskripsi |
|----------|-----------|
| `docker network create [name]` | Membuat jaringan Docker |
| `docker network ls` | Menampilkan daftar jaringan Docker |
| `docker network inspect [name]` | Menampilkan detail jaringan |
| `docker network connect [network] [container]` | Menghubungkan container ke jaringan |
| `docker network disconnect [network] [container]` | Memutuskan container dari jaringan |
| `docker network rm [name]` | Menghapus jaringan |

---

## 🛠️ 6. Perintah untuk Docker Compose
| Perintah | Deskripsi |
|----------|-----------|
| `docker-compose up` | Menjalankan semua service dalam file `docker-compose.yml` |
| `docker-compose up -d` | Menjalankan service di background |
| `docker-compose down` | Menghentikan dan menghapus container serta jaringan |
| `docker-compose ps` | Menampilkan status container dalam Compose |
| `docker-compose logs` | Menampilkan log dari Compose |
| `docker-compose build` | Membangun ulang image dalam Compose |
| `docker-compose stop` | Menghentikan semua service dalam Compose |
| `docker-compose restart` | Merestart semua service dalam Compose |

---

## 🔎 7. Perintah untuk Resource Utilization
| Perintah | Deskripsi |
|----------|-----------|
| `docker stats` | Menampilkan penggunaan CPU, memori, dan jaringan dari container yang sedang berjalan |
| `docker system df` | Menampilkan penggunaan disk oleh Docker |
| `docker system prune` | Membersihkan semua container, image, dan network yang tidak digunakan |

---

## 🧪 8. Perintah untuk Troubleshooting
| Perintah | Deskripsi |
|----------|-----------|
| `docker inspect [container/image]` | Menampilkan detail tentang container atau image |
| `docker events` | Menampilkan event real-time dari Docker |
| `docker logs [container]` | Menampilkan log container |
| `docker logs -f [container]` | Menampilkan log secara real-time |

---

## 📥 9. Perintah untuk Export dan Import
| Perintah | Deskripsi |
|----------|-----------|
| `docker save -o [file.tar] [image]` | Mengekspor image ke file `.tar` |
| `docker load -i [file.tar]` | Mengimpor image dari file `.tar` |
| `docker export -o [file.tar] [container]` | Mengekspor container ke file `.tar` |
| `docker import [file.tar] [name]` | Mengimpor file `.tar` sebagai image baru |

---

## 🎯 10. Perintah untuk Label dan Tag
| Perintah | Deskripsi |
|----------|-----------|
| `docker tag [source_image] [target_image]` | Menandai image dengan nama baru |
| `docker label [container/image] [key=value]` | Memberikan label ke container atau image |

---

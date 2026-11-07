# Day-1-FC27_Stefany-Angely

## Identitas Peserta

* **Nama Lengkap:** Stefany Angely
* **Program Studi:** Teknik Multimedia Digital
* **Jurusan:** Teknik Informatika dan Komputer
* **Kegiatan:** Workshop "From AI to GitHub: Building with AI, Managing Change with GitHub" (Day 1)
* **Narasumber:** Nugi Farhan (Senior Product Designer)

## Deskripsi Repository

Repository ini berisi dokumentasi kegiatan workshop Day 1 yang membahas pemanfaatan AI untuk membuat aplikasi dan pengelolaan perubahan kode menggunakan Git dan GitHub. Isinya mencakup rangkuman materi, poin penting yang dipelajari, dan pendapat pribadi saya tentang workshop.

## Tujuan Repository

1. Mendokumentasikan materi dan kegiatan workshop Day 1 secara rapi dan terstruktur.
2. Menjadi latihan pertama membuat dan mengelola repository di GitHub.
3. Menjadi catatan belajar yang bisa dibuka kembali kapan saja.
4. Memenuhi tugas workshop yang ditetapkan panitia.

## Informasi Kegiatan Workshop

Workshop Day 1 bertujuan agar peserta mampu:

* Menjelaskan bagaimana prompt AI yang lebih detail menghasilkan hasil yang lebih baik.
* Membedakan Git dan GitHub.
* Mengidentifikasi repository, commit, branch, dan pull request.
* Melakukan version controlling.

Proyek yang dikerjakan adalah **Student Task Planner**, yaitu sebuah aplikasi web sederhana untuk mencatat tugas dan deadline mahasiswa.

---

# Dokumentasi Workshop

## 1. Rangkuman Materi

### A. Prompt Engineering

* **Pengertian prompt:** instruksi atau masukan yang diberikan kepada model AI untuk mendapatkan hasil tertentu. Bentuknya bisa berupa pertanyaan sederhana, kata kunci, instruksi yang rumit, atau potongan kode.
* **Prompt engineering:** cara merancang instruksi agar AI memberikan jawaban yang tepat, relevan, dan layak digunakan.
* **Context is key:** prompt tanpa konteks (contoh: "Create student task planner") menghasilkan jawaban yang umum dan kurang terarah, sedangkan prompt dengan konteks yang jelas menghasilkan hasil yang jauh lebih sesuai kebutuhan.
* **Struktur prompt yang baik:**
  - **Role:** peran yang diminta dari AI.
  - **Task:** tujuan atau tugas yang harus dikerjakan.
  - **Context:** requirements dan constraints (batasan teknologi, tingkat kesulitan, dan sebagainya).
  - **Format:** bentuk output yang diinginkan.
* **Taktik menulis prompt yang baik:**
  - Gunakan kata kerja aksi untuk menentukan tindakan yang diinginkan.
  - Tentukan panjang dan format output.
  - Sebutkan target audiens.
  - Sertakan fakta dan data yang relevan.
  - Rujuk sumber atau dokumen tertentu.
  - Definisikan istilah dan konsep kunci.
* **Keuntungan prompt engineering:**
  - Meningkatkan performa model AI.
  - Mengurangi bias dan respon yang offensive.
  - Meningkatkan kontrol dan predictability.
  - Memberikan pengalaman pengguna yang lebih baik.

### B. Git

* Git adalah **version control system** yang melacak siapa, kapan, dan apa saja yang diubah dalam suatu file.
* Git diciptakan oleh **Linus Torvalds pada tahun 2005**.
* **Alur kerja Git:**
  - **Working directory:** salinan satu versi proyek yang sedang dikerjakan di komputer.
  - **Staging area (index):** tempat menyimpan informasi perubahan yang akan dimasukkan ke commit berikutnya.
  - **Git directory (repository):** tempat Git menyimpan metadata dan object database proyek. Bagian inilah yang disalin saat melakukan clone.

### C. Git vs GitHub

| Git | GitHub |
|-----|--------|
| Sistem version control terdistribusi (DVCS) untuk melacak dan mengelola perubahan kode secara lokal | Platform berbasis web untuk menyimpan repository Git secara online dan mendukung kolaborasi |

### D. Perintah Dasar Git

```bash
git init
git add .
git commit -m "pesan commit"
git remote add origin <url>
git push origin main
git pull origin main
```

| Perintah | Fungsi |
|----------|--------|
| `git init` | Memulai repository baru |
| `git add .` | Memindahkan file ke staging area |
| `git commit -m` | Menyimpan perubahan ke repository |
| `git remote add` | Menghubungkan repository lokal dengan repository online |
| `git push origin main` | Mengirim perubahan ke GitHub |
| `git pull origin main` | Mengambil dan menggabungkan perubahan dari GitHub |

Variasi `git add`:

* `git add --all` dan `git add -A` berfungsi sama, yaitu menambahkan semua perubahan ke staging area.
* `git add .` menambahkan semua file di direktori saat ini beserta isinya.
* `git add *` menambahkan file yang dimodifikasi atau baru, tetapi tidak file yang dihapus.

### E. Setup Git dan VS Code

1. Install Git, lalu cek dengan `git --version`.
2. Atur identitas Git:

```bash
git config --global user.name "Nama Kamu"
git config --global user.email "emailkamu@example.com"
```

3. Cek konfigurasi dengan `git config --global --list`.
4. Install VS Code, lalu cek dengan `code --version`.
5. Tambahkan repository ke Git dengan `git init` atau `git clone "url"`.

### F. Koneksi ke GitHub dengan SSH Key

1. Buat SSH key dengan `ssh-keygen -t ed25519 -C "email@domain.com"`.
2. Tekan Enter untuk lokasi file default, lalu isi passphrase atau kosongkan.
3. Jalankan SSH agent dan tambahkan key ke agent.
4. Salin public key, lalu tambahkan di pengaturan SSH and GPG keys di GitHub.
5. Verifikasi koneksi dengan `ssh -T git@github.com`.

Catatan: Ed25519 adalah skema tanda tangan digital berbasis kurva eliptik yang aman, cepat, dan tahan terhadap serangan implementasi kriptografi umum.

### G. Proyek Student Task Planner

Alur kerja yang dipraktikkan:

1. Gunakan platform AI (Claude, Antigravity, ChatGPT).
2. Tulis prompt untuk membuat web/aplikasi.
3. Tambahkan proyek ke Git dengan `git init`.
4. Commit dan push ke GitHub.
5. Lakukan perubahan.
6. Commit dan push lagi ke GitHub.

## 2. Poin Penting dan Pengetahuan Baru

* Prompt yang detail/spesifik dan berkonteks menghasilkan output AI yang lebih baik daripada prompt yang singkat dan umum.
* Struktur prompt **Role, Task, Context, Format** membantu menulis instruksi yang jelas.
* Hasil dari AI tetap harus diverifikasi dan jangan langsung dianggap benar.
* Git dan GitHub adalah dua hal yang berbeda yaitu Git bekerja secara lokal, sedangkan GitHub menyimpan repository secara online.
* Perubahan di Git melewati tiga tahap yaitu working directory, staging area, lalu repository.
* Alur dasar yang harus dihafal: `git add`, `git commit`, `git push`.
* SSH key membuat koneksi ke GitHub lebih aman dan praktis karena tidak perlu memasukkan password setiap kali push.
* Commit yang rutin membuat setiap perubahan tercatat sehingga mudah ditelusuri dan dikembalikan jika terjadi kesalahan.

## 3. Pendapat Pribadi tentang Day 1 Proyek Workshop

Menurut saya workshop hari ini sangat informatif, langkah-langkahnya dijelaskan dengan sederhana dan jelas sehingga mudah diikuti oleh kami yang masih pemula.

---

*Dokumentasi ini dibuat oleh Stefany Angely sebagai tugas Workshop Day 1.*

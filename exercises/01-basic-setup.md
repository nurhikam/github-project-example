# Latihan 1: Setup Basic Project

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan latihan ini, Anda akan bisa:

- Membuat GitHub Project baru
- Memahami interface dasar GitHub Project
- Menambahkan issues ke project
- Mengatur status items di Board view

## 📚 Teori Singkat

GitHub Project menggunakan konsep "Items" yang bisa berupa:

- **Issues**: Task atau bug yang perlu dikerjakan
- **Pull Requests**: Code changes yang perlu direview
- **Draft Issues**: Notes atau ideas yang belum menjadi issue formal

Board view menggunakan konsep Kanban dengan kolom-kolom status.

## 🛠️ Langkah-langkah

### Step 1: Buat Project Baru

1. Buka repository Anda di GitHub
2. Klik tab **Projects** di bagian atas
3. Klik tombol **New project**
4. Pilih **Board** sebagai template
5. Beri nama: "My First GitHub Project"
6. Klik **Create**

### Step 2: Kenali Interface

Setelah project dibuat, Anda akan melihat:

- **View selector** (kiri atas): Switch antara Board, Table, Roadmap
- **Columns**: Todo, In Progress, Done (default)
- **+ Add item**: Button untuk menambah item baru
- **⋮ Menu**: Settings dan options

### Step 3: Buat Issues Pertama

1. Klik **+ Add item** di kolom "Todo"
2. Ketik: "Setup project documentation"
3. Tekan Enter
4. Klik item yang baru dibuat
5. Klik **Convert to issue**
6. Pilih repository Anda
7. Tambahkan deskripsi:

   ```
   ## Task
   Create comprehensive documentation for the project

   ## Acceptance Criteria
   - [ ] README.md completed
   - [ ] CONTRIBUTING.md added
   - [ ] LICENSE file added
   ```

8. Klik **Create**

### Step 4: Tambah Lebih Banyak Issues

Buat 5 issues berikut (gunakan langkah yang sama):

**Issue 1: Setup CI/CD Pipeline**

```
## Description
Setup GitHub Actions for automated testing and deployment

## Tasks
- [ ] Create workflow file
- [ ] Configure test runner
- [ ] Setup deployment steps
```

**Issue 2: Design Database Schema**

```
## Description
Design the initial database schema for the application

## Requirements
- User table
- Product table
- Order table
- Relations between tables
```

**Issue 3: Create Login Page**

```
## Description
Implement user authentication with login page

## Features
- Email/password login
- Remember me checkbox
- Forgot password link
- Form validation
```

**Issue 4: Fix Mobile Responsiveness**

```
## Description
Several pages are not mobile-friendly

## Pages to Fix
- [ ] Homepage
- [ ] Product listing
- [ ] Checkout page
```

**Issue 5: Write Unit Tests**

```
## Description
Add unit tests for core functionality

## Coverage Target
- Minimum 80% code coverage
- Test all critical paths
```

### Step 5: Organize Issues

1. Drag **"Setup project documentation"** ke kolom **In Progress**
2. Drag **"Write Unit Tests"** ke kolom **Done** (anggap sudah selesai)
3. Sisanya tetap di **Todo**

### Step 6: Tambah Labels

1. Buka salah satu issue
2. Klik **Labels** di sidebar
3. Tambahkan label yang sesuai:
   - `documentation` untuk issue dokumentasi
   - `ci/cd` untuk pipeline
   - `database` untuk schema
   - `feature` untuk login page
   - `bug` untuk mobile responsiveness
   - `testing` untuk unit tests

### Step 7: Assign Issues

1. Assign diri Anda ke 2-3 issues
2. Ini menunjukkan siapa yang bertanggung jawab

## ✅ Checklist Penyelesaian

- [ ] Project berhasil dibuat dengan nama "My First GitHub Project"
- [ ] Minimal 5 issues telah dibuat
- [ ] Issues tersebar di 3 kolom (Todo, In Progress, Done)
- [ ] Setiap issue memiliki deskripsi yang jelas
- [ ] Labels telah ditambahkan ke issues
- [ ] Beberapa issues telah di-assign

## 🎓 Konsep yang Dipelajari

- ✅ Membuat GitHub Project
- ✅ Membuat dan mengkonversi draft issues
- ✅ Drag & drop untuk mengatur status
- ✅ Menambahkan labels dan assignees
- ✅ Interface Board view

## 📝 Quiz

1. Apa perbedaan antara "Draft issue" dan "Issue"?
2. Berapa kolom default yang ada di Board view?
3. Bagaimana cara memindahkan item antar kolom?

<details>
<summary>Lihat Jawaban</summary>

1. Draft issue adalah note/idea yang belum formal. Issue adalah task yang tercatat di repository dengan nomor unik.
2. 3 kolom: Todo, In Progress, Done
3. Drag and drop dengan mouse, atau click item dan pilih status baru

</details>

## 🚀 Next Steps

Lanjut ke [Latihan 2: Custom Fields & Filters](02-custom-fields.md) untuk belajar cara menambahkan field custom dan membuat filter yang powerful!

## 💡 Tips

- Gunakan keyboard shortcut `C` untuk create item baru dengan cepat
- Double-click item untuk membuka detail view
- Gunakan markdown di deskripsi untuk formatting yang lebih baik

---

**Selamat! Anda telah menyelesaikan latihan pertama! 🎉**

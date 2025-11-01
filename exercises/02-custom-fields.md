# Latihan 2: Custom Fields & Filters

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan latihan ini, Anda akan bisa:

- Membuat custom fields untuk tracking detail
- Menggunakan berbagai tipe field (Select, Number, Date, Text)
- Membuat dan menyimpan filters
- Mengelompokkan items berdasarkan field

## 📚 Teori Singkat

Custom Fields memungkinkan Anda menambahkan metadata tambahan ke items:

- **Select**: Pilihan dropdown (Priority, Team, etc)
- **Number**: Nilai numerik (Story Points, Hours)
- **Date**: Tanggal (Due Date, Start Date)
- **Text**: Text bebas (Notes, Tags)
- **Iteration**: Sprint atau iteration planning

## 🛠️ Langkah-langkah

### Step 1: Tambah Field Priority

1. Buka project Anda dari Latihan 1
2. Klik **+ New field** di bagian atas (atau ⋮ menu → Fields)
3. Pilih **Select**
4. Name: `Priority`
5. Tambahkan options:
   - 🔴 High
   - 🟡 Medium
   - 🟢 Low
6. Pilih warna untuk setiap option
7. Klik **Save**

### Step 2: Set Priority untuk Issues

Kembali ke Board view dan set priority:

- Setup project documentation → Medium
- Setup CI/CD Pipeline → High
- Design Database Schema → High
- Create Login Page → Medium
- Fix Mobile Responsiveness → High
- Write Unit Tests → Low

**Cara set:**

1. Click pada item
2. Find field "Priority" di sidebar
3. Select value yang sesuai

### Step 3: Tambah Field Estimate

1. Klik **+ New field**
2. Pilih **Number**
3. Name: `Story Points`
4. Description: "Estimation in story points"
5. Klik **Save**

Set story points untuk setiap issue:

- Setup project documentation → 3
- Setup CI/CD Pipeline → 8
- Design Database Schema → 5
- Create Login Page → 5
- Fix Mobile Responsiveness → 8
- Write Unit Tests → 3

### Step 4: Tambah Field Due Date

1. Klik **+ New field**
2. Pilih **Date**
3. Name: `Due Date`
4. Klik **Save**

Set due dates (relative dari hari ini):

- Setup project documentation → 3 hari dari sekarang
- Setup CI/CD Pipeline → 1 minggu dari sekarang
- Design Database Schema → 5 hari dari sekarang
- Create Login Page → 1 minggu dari sekarang
- Fix Mobile Responsiveness → 2 hari dari sekarang (urgent!)
- Write Unit Tests → 2 minggu dari sekarang

### Step 5: Tambah Field Team

1. Klik **+ New field**
2. Pilih **Select**
3. Name: `Team`
4. Options:
   - 🎨 Frontend
   - ⚙️ Backend
   - 🗄️ Database
   - 🚀 DevOps
   - 📝 Documentation
5. Klik **Save**

Assign teams:

- Setup project documentation → Documentation
- Setup CI/CD Pipeline → DevOps
- Design Database Schema → Database
- Create Login Page → Frontend
- Fix Mobile Responsiveness → Frontend
- Write Unit Tests → Backend

### Step 6: Switch ke Table View

1. Click dropdown view selector (biasanya "Board")
2. Pilih **Table**
3. Sekarang Anda bisa melihat semua fields dalam format tabel!

Perhatikan bahwa Anda bisa:

- Sort berdasarkan kolom (click header)
- Edit values inline
- Resize kolom
- Hide/show kolom (⋮ pada header kolom)

### Step 7: Buat Filter "High Priority"

1. Click **Filter** icon (🔍) di toolbar
2. Click **+ Add filter**
3. Select: `Priority` → `is` → `High`
4. Sekarang hanya high priority items yang terlihat
5. Click **Save view** → Name: "High Priority Items"

### Step 8: Buat Filter "This Week"

1. Clear filter sebelumnya
2. Click **+ Add filter**
3. Select: `Due Date` → `is within` → `next 7 days`
4. Click **Save view** → Name: "Due This Week"

### Step 9: Buat Filter "Frontend Team"

1. Clear filter sebelumnya
2. Click **+ Add filter**
3. Select: `Team` → `is` → `Frontend`
4. Click **Save view** → Name: "Frontend Tasks"

### Step 10: Group by Priority

1. Kembali ke Board view
2. Click **Group by** dropdown
3. Select **Priority**
4. Sekarang Board Anda akan menampilkan kolom per priority level!

Coba juga:

- Group by Team
- Group by Assignee
- Group by Status (default)

## ✅ Checklist Penyelesaian

- [ ] Field "Priority" dibuat dengan 3 options (High, Medium, Low)
- [ ] Field "Story Points" dibuat dan terisi
- [ ] Field "Due Date" dibuat dan terisi
- [ ] Field "Team" dibuat dengan 5 options
- [ ] Semua issues memiliki nilai untuk setiap custom field
- [ ] Table view berhasil digunakan
- [ ] 3 saved filters berhasil dibuat
- [ ] Mencoba grouping berdasarkan berbagai field

## 🎓 Konsep yang Dipelajari

- ✅ Membuat custom fields berbagai tipe
- ✅ Mengisi values untuk custom fields
- ✅ Menggunakan Table view untuk bulk editing
- ✅ Membuat dan menyimpan filters
- ✅ Grouping items berdasarkan field values

## 📝 Quiz

1. Apa perbedaan antara field tipe "Select" dan "Text"?
2. Bagaimana cara membuat filter yang kompleks dengan multiple conditions?
3. Apakah custom fields bisa diedit setelah dibuat?

<details>
<summary>Lihat Jawaban</summary>

1. Select memiliki pilihan terbatas yang sudah ditentukan, Text bisa diisi bebas
2. Click "+ Add filter" multiple kali untuk menambah kondisi (AND logic)
3. Ya, klik ⋮ pada field header → Edit field

</details>

## 🎨 Variasi Latihan

Coba buat custom fields lain:

- **Status** (Custom): Planning, Design, Development, Testing, Deployed
- **Complexity**: Simple, Moderate, Complex
- **Sprint**: Sprint 1, Sprint 2, Sprint 3
- **Environment**: Dev, Staging, Production
- **Bug Severity**: Critical, Major, Minor, Trivial

## 🚀 Next Steps

Lanjut ke [Latihan 3: Automation](03-automation.md) untuk belajar cara mengotomasi workflow Anda!

## 💡 Tips

- Gunakan emoji di field options untuk visual appeal 🎨
- Field "Iteration" khusus untuk sprint planning
- Single-select vs Multi-select: pilih sesuai kebutuhan
- Date fields bisa menunjukkan overdue items otomatis

---

**Great job! Custom fields membuat project management lebih powerful! 💪**

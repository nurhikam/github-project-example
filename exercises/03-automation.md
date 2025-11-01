# Latihan 3: Automation

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan latihan ini, Anda akan bisa:

- Mengaktifkan built-in workflows
- Membuat automation rules custom
- Mengotomasi status updates
- Mengotomasi field values berdasarkan events

## 📚 Teori Singkat

GitHub Project Automation memungkinkan Anda:

**Built-in Workflows:**

- Auto-add items when created
- Auto-archive items when closed
- Auto-update status based on PR state

**Custom Workflows:**

- Trigger: Event yang memicu automation
- Action: Apa yang terjadi saat triggered

**Common Events:**

- Item added to project
- Item closed
- Item reopened
- Pull request merged
- Pull request review status

## 🛠️ Langkah-langkah

### Step 1: Akses Workflow Settings

1. Buka project Anda
2. Click **⋮** (menu tiga titik) di kanan atas
3. Pilih **Workflows**
4. Anda akan melihat built-in workflows dan bisa membuat custom

### Step 2: Aktifkan "Auto-add to project"

1. Find workflow: **Item added to project**
2. Klik **Edit**
3. Set trigger: `Issues` dan `Pull requests`
4. Set condition:
   - Repository: `[your-repository]`
   - Optional: Add label filter (e.g., only add items with label `project`)
5. Action: Otomatis, item akan masuk ke project
6. Klik **Save**

**Test:**

- Buat issue baru di repository
- Issue tersebut otomatis muncul di project!

### Step 3: Aktifkan "Auto-archive when done"

1. Find workflow: **Item closed**
2. Klik **Edit**
3. Set trigger: When item is closed
4. Action: Set status to `Done` and archive
5. Klik **Save**

**Test:**

- Close salah satu issue di repository
- Item otomatis pindah ke Done dan ter-archive!

### Step 4: Automation - PR Merged to Done

1. Click **New workflow** (atau **Create workflow**)
2. Name: "PR Merged → Done"
3. Trigger: **Pull request merged**
4. Action: **Set status to Done**
5. Klik **Save**

### Step 5: Automation - New Item Priority

1. Click **New workflow**
2. Name: "New Items → Low Priority"
3. Trigger: **Item added to project**
4. Action: **Set Priority to Low**
5. Klik **Save**

Sekarang semua item baru otomatis mendapat priority "Low" sebagai default.

### Step 6: Automation - High Priority Alert

1. Click **New workflow**
2. Name: "High Priority → In Progress"
3. Trigger: **Priority changed to High**
4. Action: **Set status to In Progress**
5. Klik **Save**

**Test:**

- Buat draft issue baru
- Set priority ke "High"
- Otomatis pindah ke "In Progress"!

### Step 7: Automation - PR Status Updates

1. Click **New workflow**
2. Name: "PR Draft → Todo"
3. Trigger: **Pull request opened as draft**
4. Action: **Set status to Todo**
5. Klik **Save**

6. Click **New workflow** lagi
7. Name: "PR Ready → In Progress"
8. Trigger: **Pull request marked as ready for review**
9. Action: **Set status to In Progress**
10. Klik **Save**

### Step 8: Test All Automations

**Test 1: Create new issue**

```
Title: Test Automation
Description: This issue tests our automation rules
```

- ✅ Auto-added to project
- ✅ Priority set to "Low"

**Test 2: Change priority**

- Change priority to "High"
- ✅ Status changes to "In Progress"

**Test 3: Close issue**

- Close the test issue
- ✅ Status changes to "Done"
- ✅ Item archived

### Step 9: Review Automation Activity

1. Go to project
2. Click **⋮** → **Workflows**
3. Review each workflow
4. Check "Activity" tab untuk melihat automation history

### Step 10: Complex Automation (Optional)

Untuk automation yang lebih kompleks, gunakan GitHub Actions:

Create `.github/workflows/project-automation.yml`:

```yaml
name: Project Automation

on:
  issues:
    types: [opened, labeled]

jobs:
  add-to-project:
    runs-on: ubuntu-latest
    steps:
      - name: Add issue to project
        if: contains(github.event.issue.labels.*.name, 'bug')
        uses: actions/add-to-project@v0.5.0
        with:
          project-url: https://github.com/users/[username]/projects/[project-number]
          github-token: ${{ secrets.PROJECT_TOKEN }}
```

## ✅ Checklist Penyelesaian

- [ ] Auto-add to project workflow aktif
- [ ] Auto-archive when closed workflow aktif
- [ ] Custom workflow untuk PR merged dibuat
- [ ] Custom workflow untuk priority dibuat
- [ ] Custom workflow untuk PR status dibuat
- [ ] Semua workflows telah di-test
- [ ] Memahami trigger dan action concepts

## 🎓 Konsep yang Dipelajari

- ✅ Built-in workflows vs custom workflows
- ✅ Trigger dan action system
- ✅ Event-based automation
- ✅ Testing automation rules
- ✅ Automation activity monitoring

## 📝 Quiz

1. Apa perbedaan antara built-in workflow dan custom workflow?
2. Berapa maksimal workflows yang bisa dibuat di satu project?
3. Apakah automation bisa di-undo jika salah?

<details>
<summary>Lihat Jawaban</summary>

1. Built-in sudah disediakan GitHub dengan common use cases, custom dibuat sesuai kebutuhan spesifik
2. Tidak ada limit, tapi sebaiknya jaga agar tetap manageable
3. Ya, Anda bisa manual mengubah status/field yang ter-update otomatis

</details>

## 🎨 Ideas Automation Lainnya

```
Automation Ideas:
├─ When label "bug" added → Set Priority to High
├─ When Sprint field changed → Set Status to Todo
├─ When Assignee added → Set Status to In Progress
├─ When Due Date passed → Add label "overdue"
├─ When all tasks completed → Set Status to Done
└─ When reopened → Remove from archive
```

## ⚠️ Best Practices

1. **Keep it simple**: Jangan buat terlalu banyak automation
2. **Test thoroughly**: Selalu test automation dengan dummy data
3. **Document**: Catat apa fungsi setiap automation
4. **Monitor**: Check activity log secara berkala
5. **Be careful**: Automation yang salah bisa membuat kekacauan

## 🚀 Next Steps

Lanjut ke [Latihan 4: Multiple Views](04-multiple-views.md) untuk belajar cara membuat dan menggunakan berbagai views!

## 💡 Tips

- Gunakan automation untuk repetitive tasks
- Combine automation dengan labels untuk powerful workflows
- GitHub Actions bisa dipakai untuk automation yang lebih kompleks
- Review automation rules secara berkala dan disable yang tidak terpakai

---

**Awesome! Automation menghemat banyak waktu! ⚡**

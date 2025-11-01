# Latihan 4: Multiple Views

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan latihan ini, Anda akan bisa:

- Membuat multiple views untuk berbagai perspektif
- Menggunakan Board, Table, dan Roadmap views
- Mengoptimalkan setiap view untuk use case tertentu
- Switch antara views dengan efisien

## 📚 Teori Singkat

GitHub Project mendukung 3 tipe view utama:

**📊 Board View (Kanban)**

- Visual workflow dengan kolom
- Drag & drop untuk update status
- Best untuk: Daily standup, Sprint board

**📋 Table View (Spreadsheet)**

- Tabular data dengan semua fields
- Bulk editing dan sorting
- Best untuk: Data analysis, Bulk updates

**🗓️ Roadmap View (Timeline)**

- Gantt chart style timeline
- Date-based visualization
- Best untuk: Sprint planning, Release planning

Anda bisa membuat MULTIPLE views dengan konfigurasi berbeda!

## 🛠️ Langkah-langkah

### Step 1: Review Current Views

1. Buka project Anda
2. Check view selector (dropdown di kiri atas)
3. Anda mungkin sudah punya:
   - Board (default)
   - High Priority Items (dari Latihan 2)
   - Due This Week (dari Latihan 2)
   - Frontend Tasks (dari Latihan 2)

### Step 2: Buat Sprint Board View

1. Click **New view**
2. Layout: **Board**
3. Name: "🏃 Sprint Board"
4. Klik **Create**
5. Configure:
   - Group by: **Status**
   - Filter: `Due Date` is within `next 14 days`
   - Sort by: `Priority` descending
6. Hide columns yang tidak perlu:
   - Hide "Assignees" (right-click column header)
7. Click **Save changes**

### Step 3: Buat Backlog View

1. Click **New view**
2. Layout: **Table**
3. Name: "📝 Backlog"
4. Configure:
   - Show columns: Title, Status, Priority, Story Points, Team
   - Filter: `Status` is `Todo`
   - Sort by: `Priority` descending, then `Story Points` descending
   - Group by: None
5. Click **Save changes**

### Step 4: Buat Team Views

**View 1: Frontend Team**

1. Click **New view**
2. Layout: **Board**
3. Name: "🎨 Frontend"
4. Configure:
   - Group by: **Status**
   - Filter: `Team` is `Frontend`
   - Show fields: Priority, Due Date, Story Points
5. Click **Save changes**

**View 2: Backend Team**

1. Click **New view**
2. Layout: **Board**
3. Name: "⚙️ Backend"
4. Configure:
   - Group by: **Status**
   - Filter: `Team` is `Backend`
5. Click **Save changes**

**View 3: DevOps Team**

1. Click **New view**
2. Layout: **Board**
3. Name: "🚀 DevOps"
4. Configure:
   - Group by: **Status**
   - Filter: `Team` is `DevOps`
5. Click **Save changes**

### Step 5: Buat Roadmap View

1. Click **New view**
2. Layout: **Roadmap**
3. Name: "🗓️ Release Roadmap"
4. Configure:
   - Date field: **Due Date**
   - Zoom level: Week
   - Group by: **Team**
5. Click **Save changes**

Sekarang Anda bisa melihat timeline semua tasks!

### Step 6: Buat Priority Matrix View

1. Click **New view**
2. Layout: **Table**
3. Name: "🎯 Priority Matrix"
4. Configure:
   - Show columns: Title, Priority, Story Points, Due Date, Status
   - Group by: **Priority**
   - Sort by: `Due Date` ascending
   - Filter: None (show all)
5. Click **Save changes**

### Step 7: Buat Completed Work View

1. Click **New view**
2. Layout: **Table**
3. Name: "✅ Completed"
4. Configure:
   - Filter: `Status` is `Done`
   - Sort by: `Closed Date` descending
   - Show columns: Title, Team, Story Points, Assignees
5. Click **Save changes**

### Step 8: Buat Overdue Items View

1. Click **New view**
2. Layout: **Table**
3. Name: "⚠️ Overdue"
4. Configure:
   - Filter:
     - `Due Date` is before `today`
     - AND `Status` is not `Done`
   - Sort by: `Due Date` ascending
   - Highlight: Make text red if possible
5. Click **Save changes**

### Step 9: Customize View for Daily Standup

1. Click **New view**
2. Layout: **Board**
3. Name: "☕ Daily Standup"
4. Configure:
   - Group by: **Assignee**
   - Filter:
     - `Status` is `In Progress`
     - OR `Status` is `Todo` with `Due Date` is today
   - Show fields: Priority, Due Date only
5. Click **Save changes**

### Step 10: Organize Your Views

Drag views untuk reorder di view selector:

```
1. ☕ Daily Standup (most used)
2. 🏃 Sprint Board
3. 📝 Backlog
4. 🗓️ Release Roadmap
5. 🎯 Priority Matrix
6. 🎨 Frontend
7. ⚙️ Backend
8. 🚀 DevOps
9. ✅ Completed
10. ⚠️ Overdue
```

## ✅ Checklist Penyelesaian

- [ ] Minimal 8 views berbeda dibuat
- [ ] Sprint Board view dengan filter 14 hari
- [ ] Backlog table view untuk planning
- [ ] Team-specific views (Frontend, Backend, DevOps)
- [ ] Roadmap view dengan timeline
- [ ] Priority Matrix untuk overview
- [ ] Completed work view untuk retrospective
- [ ] Overdue view untuk tracking delayed items
- [ ] Daily Standup view untuk team sync

## 🎓 Konsep yang Dipelajari

- ✅ Multiple views untuk berbagai perspektif
- ✅ Optimasi layout per use case
- ✅ Advanced filtering dan grouping
- ✅ View organization dan navigation
- ✅ Timeline visualization dengan Roadmap

## 📝 Quiz

1. Kapan sebaiknya menggunakan Board vs Table view?
2. Apa kegunaan utama Roadmap view?
3. Berapa maksimal views yang bisa dibuat?

<details>
<summary>Lihat Jawaban</summary>

1. Board untuk visual workflow dan quick status updates, Table untuk detail analysis dan bulk editing
2. Roadmap untuk timeline planning, melihat dependencies, dan release planning
3. Tidak ada limit, tapi sebaiknya hanya buat yang benar-benar digunakan

</details>

## 🎨 View Ideas Lainnya

```
View Ideas:
├─ Bug Tracking Board (filter: label=bug)
├─ Feature Development (filter: label=feature)
├─ This Month Roadmap (filter: due date this month)
├─ High Effort Tasks (filter: story points > 5)
├─ Unassigned Work (filter: assignee is empty)
├─ Quick Wins (filter: priority=high AND story points < 3)
├─ Blocked Items (filter: label=blocked)
└─ All Active Work (filter: status != done)
```

## 🎯 Use Cases per View Type

### Board View Best For:

- Daily standups
- Sprint planning
- Quick status updates
- Team collaboration
- Visual workflow

### Table View Best For:

- Backlog grooming
- Bulk editing
- Data analysis
- Export planning
- Detailed review

### Roadmap View Best For:

- Release planning
- Quarter planning
- Dependency tracking
- Timeline visualization
- Stakeholder communication

## 🚀 Next Steps

Lanjut ke [Latihan 5: Roadmap & Planning](05-roadmap.md) untuk deep dive ke timeline planning!

## 💡 Tips

- Gunakan emoji di nama view untuk easy recognition 🎨
- Archive views yang tidak terpakai
- Share specific view URL ke team members
- Bookmark frequently used views
- Use consistent naming convention

---

**Excellent! Multiple views memberikan flexibility yang luar biasa! 👏**

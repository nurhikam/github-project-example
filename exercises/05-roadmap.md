# Latihan 5: Roadmap & Planning

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan latihan ini, Anda akan bisa:

- Membuat roadmap untuk sprint/quarter planning
- Menggunakan iterations/sprints
- Memvisualisasikan dependencies dan timeline
- Melakukan capacity planning
- Tracking milestone dan deadlines

## 📚 Teori Singkat

**Roadmap View** adalah timeline visualization yang menunjukkan:

- Start dan end dates
- Duration dan progress
- Dependencies antara tasks
- Team capacity
- Milestone markers

**Iterations** adalah timeboxed periods (sprints) untuk agile planning:

- Sprint 1, Sprint 2, etc.
- Fixed duration (1-4 weeks)
- Clear start/end dates
- Velocity tracking

## 🛠️ Langkah-langkah

### Step 1: Setup Iterations Field

1. Go to project settings (⋮ → Settings)
2. Click **+ New field**
3. Type: **Iteration**
4. Name: "Sprint"
5. Configure iterations:
   - Duration: 2 weeks
   - Start date: Next Monday
   - Number of iterations: 6 (3 months ahead)
6. Click **Create**

Your sprints akan otomatis dibuat:

- Sprint 1: [Date] - [Date]
- Sprint 2: [Date] - [Date]
- Sprint 3: [Date] - [Date]
- etc.

### Step 2: Assign Items to Sprints

1. Go to Table view
2. Add "Sprint" column if not visible
3. Assign items to sprints:

**Sprint 1 (Current):**

- Fix Mobile Responsiveness (8 pts)
- Setup project documentation (3 pts)
- Write Unit Tests (3 pts)
  Total: 14 points

**Sprint 2:**

- Design Database Schema (5 pts)
- Create Login Page (5 pts)
  Total: 10 points

**Sprint 3:**

- Setup CI/CD Pipeline (8 pts)
  Total: 8 points

### Step 3: Add Start Dates

1. Add "Start Date" field (if not exists)
2. Type: Date
3. Fill start dates for all items:
   - Use sprint start dates as reference
   - Stagger starts to show dependencies

### Step 4: Create Roadmap View

1. Click **New view**
2. Layout: **Roadmap**
3. Name: "🗺️ Sprint Roadmap"
4. Configure:
   - Date field: **Start Date**
   - End date field: **Due Date**
   - Zoom: Week view
   - Group by: **Sprint**
5. Save

### Step 5: Visualize by Team

1. Duplicate the roadmap view
2. Name: "👥 Team Roadmap"
3. Change configuration:
   - Group by: **Team**
   - Keep date fields same
4. Save

Now you can see team capacity and workload!

### Step 6: Add Milestones

Create milestone issues:

**Milestone 1: MVP Launch**

- Due Date: End of Sprint 2
- Description: "Minimum Viable Product ready for testing"
- Label: `milestone`
- Link related issues

**Milestone 2: Production Ready**

- Due Date: End of Sprint 3
- Description: "Production deployment with CI/CD"
- Label: `milestone`

**Milestone 3: Full Feature Release**

- Due Date: End of Sprint 6
- Description: "All planned features completed"
- Label: `milestone`

### Step 7: Create Milestone View

1. New Roadmap view
2. Name: "🎯 Milestones"
3. Filter: `Label` contains `milestone`
4. Group by: None
5. Zoom out to see full timeline

### Step 8: Capacity Planning

Calculate team capacity:

**Per Sprint (2 weeks):**

```
Developer capacity:
- 10 working days
- 8 hours/day
- 80% efficiency
= 64 hours = ~20 story points (at 3 hours/point)
```

**Team capacity:**

```
Frontend (2 devs): 40 points/sprint
Backend (2 devs): 40 points/sprint
DevOps (1 dev): 20 points/sprint
Total: 100 points/sprint
```

Create capacity tracking table:

| Sprint   | Planned | Team Capacity | Status     |
| -------- | ------- | ------------- | ---------- |
| Sprint 1 | 14 pts  | 100 pts       | ✅ Healthy |
| Sprint 2 | 10 pts  | 100 pts       | ✅ Healthy |
| Sprint 3 | 8 pts   | 100 pts       | ✅ Healthy |

### Step 9: Quarter Planning View

1. New Roadmap view
2. Name: "📅 Q4 2025 Roadmap"
3. Configure:
   - Zoom: Month view
   - Filter: `Sprint` is not empty
   - Group by: **Team**
   - Show: All sprints dalam quarter

### Step 10: Dependencies Visualization

Buat issues dengan dependencies:

**Issue: Backend API (Sprint 2)**

- Blocks: Create Login Page
- Blocks: Fix Mobile Responsiveness

**Issue: Database Schema (Sprint 1)**

- Blocks: Backend API

Add notes in descriptions:

```markdown
## Dependencies

⬅️ Depends on: #[issue-number]
➡️ Blocks: #[issue-number], #[issue-number]
```

View dependencies di Roadmap - GitHub akan show connections!

## ✅ Checklist Penyelesaian

- [ ] Iterations/Sprint field created dengan 6 sprints
- [ ] Semua items assigned ke sprints
- [ ] Start dates dan due dates terisi
- [ ] Sprint Roadmap view created
- [ ] Team Roadmap view created
- [ ] 3 milestones created dan tracked
- [ ] Milestone view created
- [ ] Capacity planning dilakukan
- [ ] Quarter planning view created
- [ ] Dependencies didokumentasikan

## 🎓 Konsep yang Dipelajari

- ✅ Iteration/Sprint planning
- ✅ Timeline visualization
- ✅ Team capacity management
- ✅ Milestone tracking
- ✅ Dependencies mapping
- ✅ Quarter planning

## 📝 Quiz

1. Apa perbedaan antara Iteration dan regular date field?
2. Bagaimana cara menghitung team capacity?
3. Mengapa dependencies penting di roadmap?

<details>
<summary>Lihat Jawaban</summary>

1. Iteration adalah recurring timeboxed periods, date field adalah single dates
2. Working days × hours/day × efficiency rate ÷ hours per point
3. Dependencies menunjukkan task order dan membantu identify bottlenecks

</details>

## 🎨 Advanced Roadmap Techniques

### Gantt-Style Planning

```
[Database Schema]─────→[Backend API]─────→[Login Page]
     Week 1-2              Week 3-4          Week 5-6
```

### Swimlane by Priority

Group by priority untuk melihat critical path:

- 🔴 High priority track
- 🟡 Medium priority track
- 🟢 Low priority track

### Release Planning

```
Quarter Roadmap:
├─ Q1: Foundation (Sprints 1-6)
├─ Q2: Feature Development (Sprints 7-12)
├─ Q3: Polish & Testing (Sprints 13-18)
└─ Q4: Launch & Scale (Sprints 19-24)
```

## 📊 Velocity Tracking

Track completed story points per sprint:

| Sprint      | Planned | Completed | Velocity |
| ----------- | ------- | --------- | -------- |
| Sprint 1    | 14      | 12        | 86%      |
| Sprint 2    | 10      | 10        | 100%     |
| Sprint 3    | 8       | 8         | 100%     |
| **Average** |         |           | **95%**  |

Use this untuk improve estimation di sprints berikutnya.

## 🚀 Next Steps

Lanjut ke [Latihan 6: Team Collaboration](06-team-collaboration.md) untuk best practices kerja tim!

## 💡 Tips

- Review roadmap di sprint planning
- Update progress daily
- Adjust dates based on actual velocity
- Use color coding untuk quick identification
- Zoom in/out untuk different time perspectives
- Screenshot roadmap untuk stakeholder updates

## ⚠️ Common Pitfalls

❌ Over-planning - Jangan planning terlalu jauh
❌ Rigid dates - Be flexible dengan timeline
❌ Ignoring dependencies - Selalu consider blockers
❌ Unrealistic capacity - Buffer untuk unexpected work
❌ No buffer time - Always include slack time

## 🎯 Best Practices

✅ Rolling wave planning (detail near term, high-level far term)
✅ Regular roadmap reviews (weekly)
✅ Clear milestone definition
✅ Realistic velocity assumptions
✅ Buffer untuk bugs dan interruptions (20-30%)
✅ Communicate changes promptly

---

**Fantastic! Roadmap planning makes complex projects manageable! 🎉**

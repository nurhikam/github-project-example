# GitHub Project Cheat Sheet

Quick reference untuk GitHub Project management.

## 🚀 Quick Start

```bash
1. Go to repository → Projects tab
2. Click "New project"
3. Choose template or start blank
4. Add items (issues/PRs)
5. Organize and track!
```

## ⌨️ Keyboard Shortcuts

| Shortcut           | Action          |
| ------------------ | --------------- |
| `C`                | Create new item |
| `E`                | Edit item       |
| `/`                | Focus search    |
| `?`                | Show shortcuts  |
| `Cmd/Ctrl + K`     | Command palette |
| `Cmd/Ctrl + Enter` | Save item       |
| `Esc`              | Close dialog    |

## 📊 Views

### Board View

```
✅ Best for: Daily workflow, standups
🎯 Group by: Status, Assignee, Priority
🔄 Actions: Drag & drop items
```

### Table View

```
✅ Best for: Bulk editing, analysis
🎯 Show: All fields as columns
🔄 Actions: Sort, filter, edit inline
```

### Roadmap View

```
✅ Best for: Timeline planning
🎯 Show: Start/end dates
🔄 Actions: Adjust timelines, see dependencies
```

## 🏷️ Custom Fields

| Type          | Use Case       | Example                |
| ------------- | -------------- | ---------------------- |
| **Select**    | Fixed options  | Priority, Team, Status |
| **Number**    | Numeric values | Story Points, Hours    |
| **Date**      | Deadlines      | Due Date, Start Date   |
| **Text**      | Free text      | Notes, Tags            |
| **Iteration** | Sprints        | Sprint 1, Sprint 2     |

## 🤖 Automation Triggers

```
✨ Item Events
- Item added to project
- Item closed
- Item reopened
- Status changed
- Priority changed

🔀 PR Events
- Pull request opened
- PR marked ready for review
- PR merged
- PR closed
- Review submitted

🏷️ Label Events
- Label added
- Label removed
```

## 🔍 Filters

### Filter Syntax

```
Field operator Value

Examples:
Status is "In Progress"
Priority is not "Low"
Assignee is @me
Due Date is within "next 7 days"
Story Points > 5
Labels contains "bug"
```

### Operators

- `is` / `is not`
- `contains` / `does not contain`
- `is within` / `is not within`
- `>` / `<` / `>=` / `<=`
- `is empty` / `is not empty`

### Multiple Filters

Use AND logic:

```
Priority is "High"
AND Status is not "Done"
AND Due Date is within "next 7 days"
```

## 📋 Best Practices

### Issue Writing

```markdown
✅ Clear, descriptive title
✅ Detailed description
✅ Acceptance criteria
✅ Labels & priority
✅ Story points estimate
✅ Assignee
```

### Sprint Planning

```
1. Review backlog
2. Estimate items (story points)
3. Check team capacity
4. Commit to sprint goal
5. Don't over-commit (70-80% capacity)
```

### Daily Standup

```
Each member answers:
1. What did I do yesterday?
2. What will I do today?
3. Any blockers?

Time limit: 15 minutes
```

### PR Reviews

```
⏱️ Review within 24 hours
💬 Constructive feedback
✅ Check tests passing
📝 Verify docs updated
🎨 Check code style
```

## 📊 Metrics to Track

| Metric         | Description             | Target     |
| -------------- | ----------------------- | ---------- |
| **Velocity**   | Story points per sprint | Consistent |
| **Lead Time**  | Idea to production      | < 2 weeks  |
| **Cycle Time** | Start to finish         | < 5 days   |
| **Throughput** | Items per week          | Increasing |
| **WIP**        | Work in progress        | Low        |
| **Bug Rate**   | Bugs per release        | Decreasing |

## 🎯 Priority Matrix

```
           │ High Impact │ Low Impact │
───────────┼─────────────┼────────────┤
  Urgent   │     P0      │     P1     │
───────────┼─────────────┼────────────┤
Not Urgent │     P2      │     P3     │
───────────┴─────────────┴────────────┘
```

## 🏃 Agile Ceremonies

### Sprint Planning (2 hours)

```
📅 When: Start of sprint
👥 Who: Full team
🎯 Goal: Plan sprint work
📊 Output: Sprint backlog
```

### Daily Standup (15 min)

```
📅 When: Every day
👥 Who: Dev team
🎯 Goal: Sync & blockers
📊 Output: Updated board
```

### Sprint Review (1 hour)

```
📅 When: End of sprint
👥 Who: Team + stakeholders
🎯 Goal: Demo completed work
📊 Output: Feedback
```

### Sprint Retro (1 hour)

```
📅 When: After review
👥 Who: Dev team
🎯 Goal: Continuous improvement
📊 Output: Action items
```

## 🔗 Quick Links

- [GitHub Projects Docs](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Agile Manifesto](https://agilemanifesto.org/)
- [Scrum Guide](https://scrumguides.org/)

## 💡 Pro Tips

```
✨ Use emoji for visual recognition
🎨 Color code priority levels
📊 Review metrics weekly
🤖 Automate repetitive tasks
📝 Document everything
🎯 Keep sprint goals SMART
🔄 Iterate and improve
👥 Communicate proactively
```

## 🚨 Common Mistakes

```
❌ Too many WIP items
❌ No clear acceptance criteria
❌ Skipping retrospectives
❌ Not updating status
❌ Over-planning
❌ Ignoring blockers
❌ No documentation
❌ Skipping code reviews
```

## ✅ Success Indicators

```
✅ Velocity consistent
✅ All items have owner
✅ Board updated daily
✅ PRs reviewed quickly
✅ Few blockers
✅ Team morale high
✅ Stakeholders happy
✅ Quality maintained
```

---

**Save this cheat sheet untuk quick reference! 📌**

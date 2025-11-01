# Template: Scrum Board

## 📋 Overview

Template untuk Scrum team dengan sprint-based development.

## 🎯 Use Case

- 2-week sprints
- Daily standups
- Sprint ceremonies (planning, review, retro)
- Velocity tracking

## 🏗️ Project Structure

### Views

1. **Sprint Board** (Board)

   - Group by: Status
   - Filter: Current sprint only
   - Columns: Backlog, Todo, In Progress, In Review, Done

2. **Product Backlog** (Table)

   - All unassigned items
   - Sort by: Priority, Story Points
   - Columns: Title, Priority, Story Points, Epic

3. **Sprint Planning** (Table)

   - Filter: Next sprint candidates
   - Group by: Epic
   - Show capacity calculation

4. **Sprint Burndown** (Roadmap)
   - Track daily progress
   - Story points remaining

### Custom Fields

```
Priority: Select
- 🔴 Critical
- 🟠 High
- 🟡 Medium
- 🟢 Low

Story Points: Number
- Fibonacci: 1, 2, 3, 5, 8, 13

Sprint: Iteration
- 2 weeks each
- 6 sprints ahead

Epic: Select
- User Management
- Payment Integration
- Reporting
- Mobile App

Status: Select
- 📋 Backlog
- 📝 Todo
- 🏃 In Progress
- 👀 In Review
- ✅ Done

Team Member: Assignee
- Auto-assigned

Definition of Done: Checklist
- [ ] Code complete
- [ ] Tests written
- [ ] PR reviewed
- [ ] Docs updated
- [ ] Deployed to staging
```

## 🤖 Automations

```
1. New issue → Add to backlog
2. Assigned → Move to Todo
3. PR opened → Move to In Review
4. PR merged → Move to Done
5. Sprint changed → Update due date
6. Status Done → Archive after 30 days
```

## 📊 Sprint Ceremonies

### Planning (Monday, 2 hours)

- Review backlog
- Estimate items
- Commit to sprint goals
- Assign tasks

### Daily Standup (10 AM, 15 min)

- Use Sprint Board view
- Round-robin updates
- Identify blockers

### Review (Friday, 1 hour)

- Demo completed work
- Stakeholder feedback
- Update backlog

### Retrospective (Friday, 1 hour)

- What went well
- What to improve
- Action items

## 📈 Metrics to Track

- Velocity (story points per sprint)
- Sprint completion rate
- Cycle time
- Lead time
- Defect rate

## 🚀 Getting Started

1. Create new project
2. Add custom fields above
3. Create views
4. Setup automations
5. Import backlog
6. Start first sprint!

## 💡 Tips

- Keep sprint goals SMART
- Don't over-commit
- Protect sprint scope
- Daily backlog grooming
- Celebrate small wins

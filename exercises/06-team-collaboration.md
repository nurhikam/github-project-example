# Latihan 6: Team Collaboration

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan latihan ini, Anda akan bisa:

- Mengelola project dengan multiple team members
- Setup proper permissions dan access control
- Best practices untuk standup dan sprint ceremonies
- Effective communication dalam project
- Tracking team performance

## 📚 Teori Singkat

Collaboration yang efektif membutuhkan:

**Clear Ownership:**

- Assignees untuk setiap task
- Clear DRI (Directly Responsible Individual)
- Team field untuk group ownership

**Communication:**

- Comments di issues
- @mentions untuk notifications
- Status updates
- Blockers dan dependencies

**Ceremonies:**

- Daily standup (15 min)
- Sprint planning (2 hours)
- Sprint review (1 hour)
- Sprint retrospective (1 hour)

## 🛠️ Langkah-langkah

### Step 1: Team Members Setup

**Add collaborators to repository:**

1. Go to repository Settings
2. Collaborators & teams
3. Add team members:
   - @developer1 (Frontend)
   - @developer2 (Backend)
   - @devops-engineer (DevOps)
   - @designer (Design)

**Add to project:**

1. Open project
2. Settings → Access
3. Invite same members
4. Set permissions:
   - Admin: Project lead
   - Write: All developers
   - Read: Stakeholders

### Step 2: Setup Team Views

Create personal views untuk setiap team member:

**View 1: My Work**

```
Name: 🙋 My Work
Filter: Assignee is @me
Sort: Priority (desc), Due Date (asc)
Layout: Board
Group by: Status
```

**View 2: My Team**

```
Name: 👥 My Team (Frontend)
Filter: Team is Frontend
Layout: Board
Group by: Assignee
Show: Only active sprint
```

**View 3: Needs Review**

```
Name: 👀 Needs Review
Filter: Status is "In Review"
Sort: Created date (oldest first)
Layout: Table
```

### Step 3: Daily Standup View

Create optimized view untuk daily standup:

```
Name: ☕ Daily Standup
Layout: Board
Group by: Assignee
Filter: Status is "In Progress" OR Status is "Todo"
Columns shown:
- Title
- Priority
- Blockers (custom text field)
Show: Sprint = current sprint only
```

**Standup format:**
Setiap member update:

1. What I did yesterday
2. What I'll do today
3. Any blockers

Update Blockers field untuk visibility!

### Step 4: Sprint Planning Process

**Pre-Planning:**

1. Product Owner prepare backlog
2. Estimates sudah ada (story points)
3. Priorities sudah clear

**During Planning:**

1. Open "📝 Backlog" view
2. Review top priority items
3. Discuss dan clarify requirements
4. Assign to current sprint
5. Assign owners (drag to assignee columns)
6. Check capacity: target ~70-80% of max velocity

**Create Planning View:**

```
Name: 📋 Sprint Planning
Layout: Table
Filter: Status is "Todo" OR Sprint is empty
Sort: Priority (desc), Story Points (desc)
Columns: Title, Priority, Story Points, Team, Estimate, Sprint
```

### Step 5: Sprint Review Process

**Setup Review View:**

```
Name: ✅ Sprint Review
Layout: Table
Filter: Sprint is "Current Sprint" AND Status is "Done"
Sort: Team, Title
Columns: Title, Assignee, Story Points, Demo Link
```

**Add Demo Link Field:**

1. New field: Text
2. Name: "Demo Link"
3. Developers add link to demo/screenshots

**Review agenda:**

1. Demo completed work (5 min per item)
2. Celebrate wins
3. Note any incomplete work
4. Discuss what to carry over

### Step 6: Sprint Retrospective

**Setup Retro Board:**

Create separate discussion in repository:

```
Title: Sprint [X] Retrospective
Category: General

## What went well? 👍

## What could be improved? 🔧

## Action items 🎯
- [ ] Action 1
- [ ] Action 2
```

Link dari project:

- Add "Retro Notes" text field
- Link to discussion

### Step 7: Blocker Management

**Add Blocker Field:**

1. New field: Select
2. Name: "Blocker Status"
3. Options:
   - 🚫 Blocked
   - ⚠️ At Risk
   - ✅ Clear

**Create Blocked Items View:**

```
Name: 🚨 Blocked Items
Filter: Blocker Status is "Blocked"
Layout: Table
Sort: Priority (desc)
Highlight: Red color
Columns: Title, Assignee, Blockers (text), Team
```

**Blocker protocol:**

1. Mark as blocked immediately
2. Add details in Blockers field
3. @mention person who can unblock
4. Discuss in standup
5. Update when resolved

### Step 8: PR Review Workflow

**Setup PR Review Process:**

1. Developer create PR → auto-add to project
2. PR status "In Review"
3. Assign reviewer
4. Reviewer checks:
   - Code quality
   - Tests passing
   - Documentation
5. Approve atau Request Changes
6. When merged → auto-move to Done

**Create Review Queue:**

```
Name: 📑 Review Queue
Filter: Type is "Pull Request" AND Status is "In Review"
Sort: Created (oldest first)
Layout: Table
Columns: Title, Author, Reviewers, Labels
```

### Step 9: Team Performance Tracking

**Create Metrics View:**

```
Name: 📊 Team Metrics
Layout: Table
Group by: Team
Columns: Title, Status, Story Points, Assignee, Sprint
```

**Track metrics:**

- Velocity per sprint
- Completion rate
- Average cycle time
- PR review time
- Bug count

**Create dashboard (in README or Wiki):**

```markdown
## Sprint [X] Metrics

### Velocity

- Planned: 14 points
- Completed: 12 points
- Velocity: 86%

### By Team

- Frontend: 5/6 tasks ✅
- Backend: 4/4 tasks ✅
- DevOps: 3/4 tasks ⚠️

### Quality

- Bugs found: 2
- PRs merged: 8
- Average review time: 4 hours
```

### Step 10: Communication Guidelines

**Document team agreements:**

Create `COLLABORATION.md`:

```markdown
# Team Collaboration Guidelines

## Communication Channels

- 💬 Slack: Quick questions, daily chat
- 📋 GitHub Issues: Task discussions
- 📝 GitHub Discussions: Decisions, RFCs
- 📧 Email: External stakeholders

## Response Times

- Slack: Within 2 hours
- Issue comments: Within 24 hours
- PR reviews: Within 1 business day
- Urgent: Use @mention + Slack ping

## Working Hours

- Core hours: 10 AM - 3 PM (must be available)
- Flexible start: 8-10 AM
- Flexible end: 4-6 PM

## Standup

- Time: 10 AM daily
- Duration: 15 minutes max
- Format: Round-robin
- View: Daily Standup board

## Code Review

- Max PR size: 400 lines
- Self-review first
- Add description & screenshots
- Tag specific reviewers
- Respond to feedback within 24h

## Sprint Ceremonies

- Planning: Monday 9 AM (2 hours)
- Review: Friday 2 PM (1 hour)
- Retro: Friday 3 PM (1 hour)
- Backlog grooming: Wednesday 2 PM (1 hour)

## Issue Management

- Always add: Priority, Team, Story Points
- Assign before starting work
- Update status when moving
- Comment on progress/blockers
- Link related PRs

## Meetings

- Default: 30 min max
- Always have agenda
- Share screen for demos
- Take notes in GitHub
- Action items → Issues
```

## ✅ Checklist Penyelesaian

- [ ] Team members added dengan proper permissions
- [ ] Personal "My Work" view untuk setiap role
- [ ] Daily Standup view configured
- [ ] Sprint Planning process documented
- [ ] Sprint Review view created
- [ ] Retrospective template prepared
- [ ] Blocker management system setup
- [ ] PR Review workflow defined
- [ ] Team metrics tracking implemented
- [ ] Collaboration guidelines documented

## 🎓 Konsep yang Dipelajari

- ✅ Team member management
- ✅ Access control dan permissions
- ✅ Ceremony optimization
- ✅ Blocker handling
- ✅ PR review workflow
- ✅ Performance tracking
- ✅ Communication protocols

## 📝 Quiz

1. Berapa lama ideal untuk daily standup?
2. Siapa yang sebaiknya menjadi admin di project?
3. Bagaimana cara menangani task yang blocked?

<details>
<summary>Lihat Jawaban</summary>

1. 15 minutes max - keep it focused and timely
2. Project lead atau scrum master - minimal number of admins
3. Mark status, document blocker, @mention resolver, discuss in standup

</details>

## 🎯 Team Health Indicators

### Green (Healthy) 🟢

- Velocity consistent (±10%)
- No long-term blockers
- PRs reviewed < 24 hours
- All sprint goals met
- Team morale high

### Yellow (At Risk) 🟡

- Velocity dropped >10%
- Some blockers >2 days
- PRs pending >48 hours
- Sprint goals partially met
- Some team concerns

### Red (Critical) 🔴

- Velocity dropped >25%
- Multiple blockers >5 days
- PRs abandoned
- Sprint goals mostly missed
- Team burnout signals

## 🚀 Advanced Collaboration

### Async-First Culture

- Document decisions
- Record demos
- Written updates
- Clear handoffs
- Comprehensive commit messages

### Cross-Team Dependencies

```
Team A (Frontend)
    ↓ needs API from
Team B (Backend)
    ↓ needs schema from
Team C (Database)
```

Track di Roadmap dengan dependencies!

### Remote Team Tips

- Overlap hours untuk real-time collab
- Record all meetings
- Written communication default
- Video for complex topics
- Regular 1-on-1s

## 💡 Tips

- 🎯 Keep standup focused - parking lot for deep dives
- 📝 Document everything in GitHub - single source of truth
- 🔄 Regular retros - continuous improvement
- 🎉 Celebrate wins - team morale matters
- 🚫 Unblock fast - don't let blockers linger
- 📊 Track metrics - data-driven decisions
- 💬 Over-communicate - better than under-communicating

## ⚠️ Common Issues

| Issue              | Solution                            |
| ------------------ | ----------------------------------- |
| Long standups      | Enforce time limit, park deep dives |
| Unclear ownership  | Always assign tasks clearly         |
| PR bottlenecks     | Round-robin reviews, time limits    |
| Scope creep        | Strict sprint commitment            |
| Untracked work     | Everything goes through project     |
| Communication gaps | Standard protocols, documentation   |

---

**Outstanding! Strong collaboration is key to project success! 🌟**

## 📚 Additional Resources

- [Agile Manifesto](https://agilemanifesto.org/)
- [Scrum Guide](https://scrumguides.org/)
- [GitHub Flow](https://guides.github.com/introduction/flow/)
- [Remote Work Best Practices](https://github.com/remoteintech/remote-jobs)

**Selamat! Anda telah menyelesaikan semua latihan! 🎊**

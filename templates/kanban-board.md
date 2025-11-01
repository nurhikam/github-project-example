# Template: Kanban Board

## 📋 Overview

Template untuk continuous flow development dengan Kanban methodology.

## 🎯 Use Case

- Continuous delivery
- No fixed sprints
- Work-in-progress (WIP) limits
- Pull-based system
- Support/maintenance teams

## 🏗️ Project Structure

### Views

1. **Kanban Board** (Board)

   - Group by: Status
   - WIP limits per column
   - Columns: Backlog, Ready, Doing, Review, Done

2. **WIP Dashboard** (Table)

   - Show items in progress
   - Group by: Assignee
   - Track cycle time

3. **Throughput** (Table)
   - Completed items
   - Group by: Week
   - Calculate metrics

### Custom Fields

```
Priority: Select
- 🚨 Urgent
- 🔴 High
- 🟡 Medium
- 🟢 Low
- ❄️ Backlog

Size: Select
- XS (< 2 hours)
- S (2-4 hours)
- M (1-2 days)
- L (3-5 days)
- XL (> 5 days)

Type: Select
- 🐛 Bug
- ✨ Feature
- 📝 Documentation
- 🔧 Maintenance
- 🚀 Enhancement

Cycle Time: Number
- Auto-calculated (days)

Lead Time: Number
- Auto-calculated (days)

Blocked: Select
- ✅ No
- 🚫 Yes
```

## 🎯 WIP Limits

```
Column          | WIP Limit | Current
----------------|-----------|--------
Backlog         | Unlimited | -
Ready           | 10        | 7
Doing           | 5         | 3
Review          | 3         | 1
Done            | -         | -
```

## 🤖 Automations

```
1. New issue → Add to Backlog
2. Assigned + Ready → Move to Doing
3. PR opened → Move to Review
4. PR merged → Move to Done
5. Blocked status → Add 🚫 label
6. Urgent priority → Notify team
```

## 📊 Kanban Metrics

### Lead Time

Time from request to delivery

- Target: < 5 days

### Cycle Time

Time from start to finish

- Target: < 3 days

### Throughput

Items completed per week

- Target: > 10 items/week

### WIP

Work in progress

- Keep low for faster flow

## 🔄 Pull System

**Rules:**

1. Don't start new work if WIP limit reached
2. Pull from Ready when capacity available
3. Finish what you start before pulling new
4. Help unblock others first
5. Swarm on blocked items

## 🚦 Status Definitions

**Backlog**

- Not yet prioritized
- Needs refinement
- No time commitment

**Ready**

- Clearly defined
- Estimated
- No dependencies
- Ready to start

**Doing**

- Currently being worked on
- Assigned to someone
- Within WIP limit

**Review**

- Code complete
- PR open
- Awaiting feedback

**Done**

- Merged to main
- Deployed
- Verified

## 🚀 Getting Started

1. Create Kanban board
2. Set WIP limits
3. Add backlog items
4. Prioritize ready queue
5. Start pulling work!

## 💡 Tips

- Respect WIP limits
- Focus on flow, not utilization
- Visualize blockers immediately
- Regular board review
- Continuous improvement
- Measure and optimize

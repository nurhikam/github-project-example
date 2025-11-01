# Frequently Asked Questions (FAQ)

## 🎯 Getting Started

### Q: Apa perbedaan GitHub Projects classic vs new Projects?

**A:** New Projects (beta) adalah rebuild complete dengan features:

- Multiple views (Board, Table, Roadmap)
- Custom fields unlimited
- Better automation
- Cross-repository support
- More flexible

Classic Projects lebih simple tapi limited. **Rekomendasi: gunakan new Projects.**

### Q: Apakah GitHub Projects gratis?

**A:** Ya! GitHub Projects gratis untuk:

- Public repositories
- Personal accounts
- Organization accounts
- GitHub Free tier

Premium features (advanced insights) tersedia di GitHub Team/Enterprise.

### Q: Berapa maksimal project yang bisa dibuat?

**A:** Tidak ada hard limit, tapi best practice:

- 1 project per product/team
- Multiple views dalam 1 project
- Jangan terlalu banyak project (sulit maintain)

## 🏗️ Project Setup

### Q: Haruskah saya membuat project di repository atau organization level?

**A:**

- **Repository level**: Untuk project specific ke satu repo
- **Organization level**: Untuk cross-repo projects atau team planning

Tip: Organization level lebih flexible.

### Q: Bagaimana cara migrate dari Trello/Jira ke GitHub Projects?

**A:**

1. Export data dari Trello/Jira (CSV)
2. Format sesuai GitHub issues
3. Bulk create issues via API atau scripts
4. Add to project
5. Configure views & fields

Tools: GitHub CLI, custom scripts, atau manual.

### Q: Apakah bisa import issues dari repository lain?

**A:** Ya! Di organization-level project, Anda bisa add items dari multiple repositories.

## 📊 Views & Customization

### Q: Berapa maksimal views yang bisa dibuat?

**A:** Tidak ada limit praktis, tapi rekomendasi:

- 5-10 views per project
- Setiap view punya purpose jelas
- Archive views yang tidak terpakai

### Q: Apakah bisa share specific view ke team member?

**A:** Ya! Copy URL dari view specific, share link tersebut. Permission mengikuti project access.

### Q: Bagaimana cara membuat custom status columns?

**A:**

1. Di Board view, add field "Status" (jika belum ada)
2. Edit field → add custom status options
3. Configure automation untuk status transitions

## 🤖 Automation

### Q: Apakah automation gratis?

**A:** Ya, built-in automation gratis. Untuk advanced automation, bisa gunakan GitHub Actions (minutes limit per month).

### Q: Bagaimana cara automation kompleks yang tidak tersedia built-in?

**A:** Gunakan GitHub Actions:

```yaml
name: Project Automation
on:
  issues:
    types: [opened, labeled]
jobs:
  add-to-project:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/add-to-project@v0.5.0
```

### Q: Apakah automation bisa di-undo?

**A:** Ya, automation hanya update fields/status. Anda bisa manual revert changes.

## 👥 Team Collaboration

### Q: Bagaimana cara invite team members?

**A:**

1. Project settings → Manage access
2. Invite by username/email
3. Set permission (Admin/Write/Read)

### Q: Apa perbedaan permission levels?

**A:**

- **Admin**: Full control (delete, settings, etc)
- **Write**: Add/edit items, change views
- **Read**: View only, no edits

### Q: Apakah bisa assign multiple people ke satu task?

**A:** Ya, issue support multiple assignees. Best practice: 1 DRI (main assignee) + helpers.

### Q: Bagaimana cara mention someone di issue?

**A:** Gunakan `@username` di comment atau description. Mereka akan dapat notification.

## 📈 Planning & Estimation

### Q: Apa itu story points?

**A:** Story points adalah relative estimation complexity:

- 1 point = Very simple (< 2 hours)
- 3 points = Simple (half day)
- 5 points = Medium (1 day)
- 8 points = Complex (2-3 days)
- 13+ points = Very complex (break down!)

### Q: Bagaimana cara calculate team velocity?

**A:**

```
Velocity = Total story points completed per sprint

Example:
Sprint 1: 15 points
Sprint 2: 18 points
Sprint 3: 16 points
Average velocity: 16.3 points/sprint
```

### Q: Berapa lama ideal sprint duration?

**A:**

- **1 week**: Fast-paced, frequent feedback
- **2 weeks**: Most common, balanced
- **3-4 weeks**: Longer planning, less overhead

Rekomendasi: **2 weeks** untuk kebanyakan team.

### Q: Bagaimana cara set WIP limits?

**A:**

1. Calculate: Team size × 1.5
2. Example: 4 devs = WIP limit 6
3. Monitor dan adjust based on flow
4. Goal: Finish what you start

## 🐛 Issues & Troubleshooting

### Q: Issue tidak muncul di project setelah dibuat?

**A:** Check:

- Automation "auto-add" active?
- Repository correct?
- Label filter di automation?
- Manual add via "+ Add item"

### Q: Tidak bisa drag items di Board view?

**A:** Check:

- Permission level (need Write access)
- Browser compatibility (try Chrome/Edge)
- Clear cache
- Check if item archived

### Q: Custom field tidak muncul?

**A:**

- Field hidden? Check field visibility settings
- View tidak show field? Add column di Table view
- Permission issue? Check access level

### Q: Automation tidak jalan?

**A:** Debug steps:

1. Check automation enabled
2. Verify trigger conditions match
3. Check activity log (Workflows → Activity)
4. Test dengan dummy issue
5. Review automation rules

## 📊 Reporting & Metrics

### Q: Bagaimana cara export data dari project?

**A:**

- Table view → Menu → Export CSV
- Atau gunakan GitHub API untuk programmatic access
- GitHub Insights untuk visual reports (Enterprise)

### Q: Apakah ada built-in burndown chart?

**A:** Tidak built-in, tapi bisa:

- Create custom using GitHub Actions
- Export data → Excel/Sheets → create chart
- Third-party tools (Zenhub, etc)

### Q: Bagaimana track team productivity?

**A:** Key metrics:

- Velocity (story points/sprint)
- Cycle time (start to done)
- Throughput (items/week)
- Quality (bug rate, PR review time)

## 🔄 Integration

### Q: Apakah GitHub Projects terintegrasi dengan Slack?

**A:** Ya, via GitHub Slack app:

- Notifications untuk project updates
- Subscribe ke project feed
- Quick actions dari Slack

### Q: Apakah bisa integrate dengan external tools?

**A:** Ya, via:

- GitHub API (GraphQL/REST)
- Webhooks untuk events
- GitHub Actions untuk automation
- Zapier/Integromat untuk no-code

### Q: Bagaimana sync GitHub Projects dengan Jira?

**A:**

- Third-party tools: Unito, Exalate
- Custom API integration
- Manual sync (not recommended)

## 💰 Pricing & Limits

### Q: Apakah ada limit jumlah items di project?

**A:** Tidak ada official hard limit, tapi performance consideration:

- < 1000 items: Excellent
- 1000-5000 items: Good
- 5000+ items: Consider splitting

### Q: Fitur apa saja yang premium?

**A:** Free tier sudah sangat complete. Premium (Team/Enterprise):

- Advanced security features
- Audit logs
- SAML SSO
- Advanced insights

## 🎓 Best Practices

### Q: Apa best practice untuk issue titles?

**A:**

```
✅ Good:
- "Add user authentication API endpoint"
- "Fix: Login button not working on mobile"
- "Improve dashboard load time"

❌ Bad:
- "Fix bug"
- "Update"
- "Changes"
```

### Q: Seberapa detail description harus ditulis?

**A:** Include:

- Context/background
- Requirements/acceptance criteria
- Technical details jika relevant
- Screenshots/mockups jika UI
- Links ke related resources

Rule: Someone baru bisa understand dan work on it.

### Q: Kapan sebaiknya close issue?

**A:** Close when:

- Work completed
- Code merged to main
- Tested in production
- Stakeholders confirmed

Don't close jika:

- Still have open subtasks
- Not deployed yet
- Waiting for verification

---

## 🤔 Pertanyaan Lain?

Jika pertanyaan Anda belum terjawab:

1. Check [GitHub Documentation](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
2. Open GitHub Discussion di repository ini
3. Search existing discussions

---

**FAQ ini akan diupdate secara berkala! 📝**

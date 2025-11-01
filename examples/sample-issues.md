# Contoh Issues untuk Latihan

Gunakan issues berikut untuk mempraktikkan GitHub Project management.

## 🎨 Frontend Issues

### Issue 1: Redesign Homepage

```markdown
**Title:** Redesign Homepage Layout

**Labels:** frontend, design, enhancement

**Description:**
Redesign homepage untuk improve user experience dan conversion rate.

## Requirements

- Modern, clean design
- Mobile responsive
- Fast loading (< 2s)
- Clear CTA buttons

## Design Assets

- Figma link: [URL]
- Brand guidelines: [URL]

## Acceptance Criteria

- [ ] Design approved by stakeholders
- [ ] Implemented in React
- [ ] Responsive on all devices
- [ ] Performance tested
- [ ] A/B test setup

**Story Points:** 8
**Priority:** High
**Team:** Frontend
```

### Issue 2: Implement Dark Mode

```markdown
**Title:** Add Dark Mode Support

**Labels:** frontend, feature, accessibility

**Description:**
Add dark mode toggle untuk better user experience, especially at night.

## Features

- Toggle switch in navbar
- Persist preference in localStorage
- Smooth theme transition
- All pages supported

## Technical Details

- CSS variables for colors
- System preference detection
- Theme context provider

## Acceptance Criteria

- [ ] Toggle implemented
- [ ] All components support dark mode
- [ ] Preference persisted
- [ ] Smooth transitions

**Story Points:** 5
**Priority:** Medium
**Team:** Frontend
```

## ⚙️ Backend Issues

### Issue 3: User Authentication API

```markdown
**Title:** Implement User Authentication API

**Labels:** backend, security, feature

**Description:**
Create secure authentication endpoints with JWT tokens.

## Endpoints

- POST /api/auth/register
- POST /api/auth/login
- POST /api/auth/refresh
- POST /api/auth/logout

## Requirements

- JWT token-based auth
- Bcrypt password hashing
- Refresh token rotation
- Rate limiting

## Acceptance Criteria

- [ ] All endpoints implemented
- [ ] Unit tests (>80% coverage)
- [ ] Integration tests
- [ ] API documentation
- [ ] Security audit passed

**Story Points:** 13
**Priority:** Critical
**Team:** Backend
```

### Issue 4: Database Optimization

```markdown
**Title:** Optimize Database Queries

**Labels:** backend, performance, database

**Description:**
Slow queries affecting application performance. Need optimization.

## Slow Queries Identified

- User listings: 2.5s → target <500ms
- Product search: 3.1s → target <1s
- Order history: 1.8s → target <500ms

## Optimization Strategies

- Add indexes
- Query optimization
- Caching layer
- Connection pooling

## Acceptance Criteria

- [ ] All queries meet target time
- [ ] Indexes added appropriately
- [ ] Redis cache implemented
- [ ] Performance tests pass

**Story Points:** 8
**Priority:** High
**Team:** Backend
```

## 🐛 Bug Issues

### Issue 5: Login Form Validation Error

```markdown
**Title:** [BUG] Login form accepts invalid email

**Labels:** bug, frontend, high-priority

**Description:**
Login form tidak validate email format dengan benar.

## Steps to Reproduce

1. Go to /login
2. Enter "notanemail" in email field
3. Click submit
4. Form submits (should show error)

## Expected Behavior

Show error: "Please enter a valid email address"

## Actual Behavior

Form submits dan returns API error

## Environment

- Browser: Chrome 96
- OS: Windows 10
- Version: 1.2.3

## Root Cause

Missing client-side validation for email format

## Fix

Add email regex validation before submit

**Priority:** High
**Severity:** Medium
```

### Issue 6: Memory Leak in Dashboard

```markdown
**Title:** [BUG] Memory leak on dashboard page

**Labels:** bug, performance, critical

**Description:**
Dashboard page memory usage increases over time, eventually crashes browser.

## Steps to Reproduce

1. Open dashboard
2. Leave tab open for 30+ minutes
3. Monitor memory usage in DevTools
4. Memory keeps increasing

## Expected Behavior

Stable memory usage

## Actual Behavior

Memory increases from 50MB to 500MB+ over 30 min

## Investigation

- Event listeners not cleaned up
- WebSocket connections not closed
- Chart data accumulating

## Fix Plan

- Add cleanup in useEffect
- Close connections on unmount
- Limit chart data points

**Priority:** Critical
**Severity:** High
**Affected Users:** ~1000 daily users
```

## 📝 Documentation Issues

### Issue 7: API Documentation

```markdown
**Title:** Complete API Documentation

**Labels:** documentation, api

**Description:**
Create comprehensive API documentation untuk external developers.

## Requirements

- All endpoints documented
- Request/response examples
- Error codes explained
- Authentication flow
- Rate limits

## Tools

- OpenAPI/Swagger
- Postman collection
- README.md

## Acceptance Criteria

- [ ] All endpoints documented
- [ ] Examples for each endpoint
- [ ] Error handling documented
- [ ] Postman collection created
- [ ] Developer feedback incorporated

**Story Points:** 5
**Priority:** Medium
**Team:** Documentation
```

## 🚀 DevOps Issues

### Issue 8: CI/CD Pipeline Setup

```markdown
**Title:** Setup GitHub Actions CI/CD Pipeline

**Labels:** devops, infrastructure, automation

**Description:**
Automate testing dan deployment dengan GitHub Actions.

## Pipeline Stages

1. Lint & Format check
2. Unit tests
3. Integration tests
4. Build
5. Deploy to staging
6. Deploy to production (manual approval)

## Requirements

- Run on every PR
- Deploy staging on merge to main
- Production deployment with approval
- Notifications on failure

## Acceptance Criteria

- [ ] Workflow file created
- [ ] All tests run automatically
- [ ] Staging auto-deploy works
- [ ] Production manual deploy works
- [ ] Slack notifications configured

**Story Points:** 8
**Priority:** High
**Team:** DevOps
```

## 📊 Data Issues

### Issue 9: Analytics Dashboard

```markdown
**Title:** Build Analytics Dashboard

**Labels:** feature, data, frontend

**Description:**
Create analytics dashboard untuk track key metrics.

## Metrics to Track

- Daily active users
- User retention
- Feature usage
- Performance metrics
- Error rates

## Requirements

- Real-time data
- Customizable date ranges
- Export to CSV
- Chart visualizations
- Mobile responsive

## Tech Stack

- React + Chart.js
- REST API or GraphQL
- Redis for caching

## Acceptance Criteria

- [ ] All metrics displayed
- [ ] Charts interactive
- [ ] Date range filter works
- [ ] Export functionality
- [ ] Performance optimized

**Story Points:** 13
**Priority:** Medium
**Team:** Frontend + Backend
```

## 🧪 Testing Issues

### Issue 10: E2E Test Suite

```markdown
**Title:** Implement E2E Test Suite

**Labels:** testing, quality

**Description:**
Create comprehensive end-to-end tests untuk critical user flows.

## Flows to Test

- User registration & login
- Product browse & search
- Add to cart & checkout
- Order history view
- Profile management

## Tools

- Playwright or Cypress
- Visual regression testing
- CI integration

## Acceptance Criteria

- [ ] All critical flows tested
- [ ] Tests run in CI
- [ ] Visual regression setup
- [ ] Test reports generated
- [ ] Documentation written

**Story Points:** 13
**Priority:** Medium
**Team:** QA + DevOps
```

---

## 💡 Tips Menggunakan Sample Issues

1. **Copy-paste** issues ini ke repository Anda
2. **Customize** sesuai project Anda
3. **Add labels** yang appropriate
4. **Assign** ke team members
5. **Link** related issues
6. **Track** progress di project board

## 🎯 Latihan

1. Buat 5 issues dari contoh di atas
2. Assign priority dan story points
3. Tambahkan ke project
4. Organize di board view
5. Track sampai completion

---

**Selamat berlatih! 🚀**

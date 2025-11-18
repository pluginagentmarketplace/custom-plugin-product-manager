# Product Roadmap Planning

Create a compelling, executable product roadmap that aligns stakeholders and guides your team.

## 🗺️ Roadmap Types

### Strategic Roadmap (12 months)
**Purpose:** Long-term vision and strategic direction

**Includes:**
- Quarterly themes and initiatives
- Major feature areas
- Business outcomes
- Not detailed with tasks

**Audience:** Executives, board, customers

**Example:**
```
Q1: Build Foundation (User management, Core features)
Q2: Expand Capability (Advanced features, integrations)
Q3: Optimize & Scale (Performance, infrastructure)
Q4: Market Leadership (Differentiation, market expansion)
```

### Tactical Roadmap (3 months)
**Purpose:** Detailed execution plan for team

**Includes:**
- User stories (30-50)
- Feature breakdown
- Sprint planning
- Dependencies and risks

**Audience:** Engineering, design, product team

### Initiative/Theme Roadmap
**Purpose:** Organize by business initiatives

**Includes:**
- Strategic initiatives
- Features per initiative
- Timeline per initiative
- Success metrics

## 📊 Prioritization Frameworks

### 1. RICE Scoring (Recommended)

**Formula:** (Reach × Impact × Confidence) / Effort

**Scoring Guide:**
- **Reach** - How many users (1-100+)
- **Impact** - Per-user impact (3=massive, 2=high, 1=medium, 0.5=small)
- **Confidence** - Confidence level (0.5-1.0)
- **Effort** - Engineer-weeks to build

**Example Calculation:**
```
Feature A: (50 × 3 × 0.8) / 5 = 24
Feature B: (100 × 2 × 0.9) / 8 = 22.5
Feature C: (200 × 1 × 0.6) / 10 = 12

→ Prioritize: A > B > C
```

### 2. MoSCoW Method

Categorize features by importance:
- **MUST** - Critical for launch/business
- **SHOULD** - Important but not critical
- **COULD** - Nice to have
- **WON'T** - Explicitly not doing now

### 3. Value vs Effort Matrix

Create 2×2 matrix:
```
        Low Effort        High Effort
High    QUICK WINS       STRATEGIC
Value   (do first)       (plan carefully)

Low     FILL-INS         AVOID
Value   (when time)      (don't do)
```

### 4. Kano Model

Categorize by customer perception:
- **Basic Factors** - Must have or dissatisfied
- **Performance Factors** - More = more satisfaction
- **Delighters** - Unexpected, causes delight

## 🎯 Strategic Roadmap Example

### Q1 2025: Establish Market Leadership
**Business Goal:** 50% user growth, 80% NPS

**Key Initiatives:**
1. **Enterprise Features**
   - SSO/SAML integration
   - Advanced permissions
   - Audit logging
   - Impact: 10-15% new enterprise customers
   - Timeline: 8 weeks

2. **Mobile Experience**
   - iOS app MVP
   - Android app MVP
   - Push notifications
   - Impact: 30% engagement increase
   - Timeline: 10 weeks

3. **Performance & Scale**
   - Database optimization
   - Caching layer
   - CDN implementation
   - Impact: 50% faster load times
   - Timeline: 6 weeks

### Q2 2025: Expand Integration Ecosystem
**Business Goal:** Become center of workflow, 3x API usage

**Key Initiatives:**
1. **API Enhancement**
2. **Zapier/Make Integration**
3. **Webhook System**
4. etc.

## 📋 Detailed Quarterly Plan Template

```
📌 Q1 2025: Theme Name

Business Goal
- Clear outcome (revenue, users, NPS, etc.)
- Specific target (e.g., +50% growth)

Key Success Metrics
- Metric 1: Target value
- Metric 2: Target value

Major Features/Initiatives
1. Feature/Initiative (8 weeks)
   - Description
   - Success criteria
   - Dependencies
   - Risks

2. Feature/Initiative (6 weeks)
   - ...

3. Feature/Initiative (4 weeks)
   - ...

Resource Plan
- Team size
- Key roles needed
- External dependencies

Dependencies & Risks
- Other teams
- External factors
- Mitigation strategies

Post-Quarter Review
- Learnings
- What worked
- What to improve
```

## 🏃 Sprint Planning (2-week sprints)

### Sprint Structure

**Sprint Goal:** One clear objective

**Features/Stories:**
- 3-5 major features
- Each with 2-5 user stories
- Total: 20-30 story points

**Team Capacity:** Engineer-days × team size

### Example Sprint

```
Sprint Goal: Enable user self-service account management

Features:
1. Password reset (5 sp)
   - Request reset flow (3)
   - Email notification (2)

2. Update profile (5 sp)
   - Profile form (3)
   - Image upload (2)

3. Billing info (8 sp)
   - Payment method update (5)
   - Billing history (3)

Total: 18 sp (good for 3 engineer team)
```

## 🔗 Dependencies & Risk Management

### Dependency Mapping

Identify:
- **Hard dependencies** - Must complete first
- **Soft dependencies** - Good to complete first
- **Blocking dependencies** - Waiting on other teams
- **External dependencies** - Third-party factors

### Risk Register

For each risk:
- **Risk:** What could go wrong
- **Probability:** High/Medium/Low
- **Impact:** High/Medium/Low
- **Mitigation:** How to prevent
- **Owner:** Who monitors

**Example:**
```
Risk: Key engineer leaves
Probability: Low (retention plan in place)
Impact: High (2-month delay)
Mitigation: Cross-training, documentation
```

## 📊 Roadmap Communication

### For Executives
- Focus on business outcomes
- Show quarterly themes
- Highlight competitive differentiation
- Show metrics and success criteria

### For Customers
- Focus on user benefits
- Show timeline (quarter not specific date)
- Highlight most requested features
- Be conservative (under-promise, over-deliver)

### For Engineering
- Detailed specs and requirements
- Dependency list
- Technical risks
- Resource needs

## 🚀 Roadmap Best Practices

✓ **Be Realistic** - Add 30% buffer for unknowns
✓ **Stay Flexible** - Roadmap is living document
✓ **Communicate Often** - Share updates weekly
✓ **Track Progress** - Weekly burndown, blockers
✓ **Get Buy-in** - Engineering and stakeholder alignment
✓ **Prioritize Ruthlessly** - Can't do everything
✓ **Focus on Outcomes** - Not just features
✓ **Plan Beyond Roadmap** - What's next after this quarter?

## 📈 Roadmap Review Process

**Weekly:**
- Progress on current sprint
- Blockers and risks
- Next week adjustments

**Monthly:**
- Progress toward quarterly goals
- Mid-quarter adjustments
- Upcoming sprint preview

**Quarterly:**
- Success metrics evaluation
- Learnings and retrospective
- Next quarter planning
- Stakeholder review

## 🎯 Roadmap Tools

Popular options:
- **Jira** - Developer-focused
- **Asana** - General project management
- **Monday.com** - Visual planning
- **Productboard** - Product-specific
- **Roadmunk** - Roadmap specialist
- **Google Sheets** - Simple, free

## ✅ Roadmap Checklist

- ✓ 12-month strategic vision
- ✓ Quarterly themes and goals
- ✓ Prioritization framework applied
- ✓ Features/stories detailed
- ✓ Timeline with dependencies
- ✓ Resource allocation plan
- ✓ Success metrics defined
- ✓ Risk mitigation strategies
- ✓ Executive alignment
- ✓ Team buy-in and understanding
- ✓ Customer communication plan
- ✓ Weekly progress tracking

---

**Ready to build your roadmap?** Start with the Roadmap & Prioritization Agent!

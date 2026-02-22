# ICEE — The Israel Center for Excellence through Education
# המרכז הישראלי למצוינות בחינוך

## What This Is
Operations and CRM system for the organization's fundraising & resource development division. The end user is a fundraising manager who needs tools to manage multiple parallel fundraising tracks, donor pipelines, team coordination, and grant tracking.

## Context
The user (Zvi) is building this system for a colleague at ICEE. The system will run on her computer, shared via Git. She is non-technical — the interface must be simple and the system largely autonomous.

## Work Tracks

### Track 1: Chicago Campaign (שיקגו)
**Goal**: Raise funds from American donors through a Chicago-based campaign.

**Components**:
- **Content production**: Presentations, video production, marketing materials (currently in progress with a graphic designer — system should NOT generate content yet, only organize/upgrade existing)
- **Team coordination**: Two key people — "Bo Asher" (בו אשר) and a new donor Zvi brought in. They are the two main arms who go out and bring interested people.
  - Regular joint calls need to be scheduled
  - Materials need to be supplied to them
  - They need to be activated/reminded every 3-4 days ("what happened with X?")
  - They write to her when they need something — this is not a new system, it's managing existing communication
- **US contact person**: A woman coming for 6 months (fixed-term) to find potential donors
  - She does background research on prospects
  - All contacts and background info must be stored in a **prospect database** (survives after she leaves)
  - Every meeting with a prospect needs documentation
  - System should send reminders: "You said there's a meeting with Michael X — what happened?"
- **Email monitoring**: System should read emails and identify:
  - School activity reports (from "Noa" / נועה) that could be useful for the team
  - Monthly school reports — flag what could work for fundraising
  - Suggest the format for forwarding info to team (paragraph + image, etc.)
- **Meeting flow**: Lead identified → outreach → interest confirmed → schedule Zoom (initially) → possibly in-person later. Scheduling is usually with a secretary. She does the pitch herself (too sensitive to automate), but system should suggest calendar slots and draft the scheduling email.

### Track 2: Alumni Track (דרך הבוגרים) — Israel
**Goal**: 50 meetings → 10 committed donors within 3 months.

**Components**:
- **Pitch development**: Building a value proposition with a small group of well-connected alumni (group already exists, conversations ongoing). Need to consolidate them into a joint call.
- **LinkedIn scanning**: Some alumni said "go through my LinkedIn contacts, tell me who you want to meet." System should scan LinkedIn profiles for:
  - Companies with sufficient capital
  - CSR departments or donation committees
  - Individuals known for philanthropy
  - Interest in Israeli society's future through education and excellence education
- **Lead pipeline**: Alumni → prospect identification → outreach → meeting → conversion
- **Meeting management**: Calendar integration for scheduling (suggestion only — she decides). Track status of each prospect through the pipeline.

### Track 3: Foundations & Philanthropy (קרנות ופילנתרופיה) — Israel
**Goal**: Systematic grant seeking and application tracking.

**Components**:
- **Opportunity scanning**: Monitor for calls for proposals (קולות קוראים) related to education, excellence, and related topics. Simple web scraping.
- **Grant writing support**: Help draft applications
- **Application tracking**: Track submitted applications and their status (e.g., "3 submissions to Avin (אבין) awaiting response")
- **Follow-up reminders**: Alert when it's time to check on pending applications

## Cross-Track Needs

### Task Management
- She currently uses a scattered system (WhatsApp messages, notebook, various docs)
- Needs voice-to-task capability (like the Telegram bot Zvi built for himself)
- Tasks should be organized chronologically AND by topic
- Daily view of what needs to happen today

### Data Consolidation
- Information scattered across: OneNote/Notebook, email, documents, proposals she co-wrote with "Efrat" (אפרת)
- System should have access to specific folders only (NOT full computer)
- All data must be centralized so it can be retrieved and used

### Calendar Integration
- Read access to her calendar
- Suggest meeting times — never book automatically
- Track meeting follow-ups

## Technical Constraints
- System runs on her computer (shared via Git from Zvi's dev environment)
- She uses Outlook (wants to migrate to Gmail — not done yet)
- Budget: ~$200/month (Claude subscription level) is acceptable if valuable
- Specific folder access only — privacy-conscious, has personal data on computer
- She is non-technical — needs simple interface, guided workflows

## What NOT to Build Yet
- Content generation (she's in the middle of a design process with a graphic designer)
- Automated meeting booking (too sensitive — she does pitches herself)
- Full email automation (suggest drafts, don't send)

## Open Questions
1. What's her email provider? (Outlook now, Gmail migration pending)
2. Which specific folders should the system access?
3. What format is the existing task list / WhatsApp export?
4. Does she want the Telegram voice interface or a different input method?
5. LinkedIn scanning — does she have LinkedIn Premium / Sales Navigator?
6. What CRM-like data already exists? Spreadsheets? Contacts?

## Implementation Priority (suggested)
1. **Task management + voice input** — immediate daily value, low complexity
2. **Prospect/donor database** — critical for Chicago track (the 6-month person is time-limited)
3. **Email monitoring & flagging** — passive value, runs in background
4. **Grant tracking** — simple status tracker
5. **LinkedIn scanning** — requires research into API/scraping feasibility
6. **Calendar integration** — depends on email provider migration
